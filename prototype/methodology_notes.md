I'll break down each component of the machine learning implementation in detail:

### 1. Data Preprocessing
```python
# Scale the data
scaler = MinMaxScaler()
scaled_data = scaler.fit_transform(merged_data)
scaled_data = scaled_data.astype(np.float32)  # Convert to float32 for PyTorch
```
- **MinMaxScaler**: Normalizes data to a [0,1] range using formula: `(x - min)/(max - min)`
- This scaling is crucial because:
  - Ensures all features are on the same scale
  - Helps prevent numerical instability during training
  - Makes training faster and more stable
- `astype(np.float32)`: Converts to 32-bit floating point for PyTorch compatibility

### 2. Sequence Creation
```python
def create_sequences(data, seq_length=10):
    X, y = [], []
    for i in range(len(data) - seq_length):
        X.append(data[i:(i + seq_length)])
        y.append(data[i + seq_length, 1])  # Index 1 for Close price
    return np.array(X), np.array(y)

seq_length = 10
X, y = create_sequences(scaled_data)
```
- Creates sliding windows of data for time series prediction
- For each window of `seq_length` days:
  - `X`: Contains 10 days of all features
  - `y`: Contains the next day's closing price
- Example:
  - If data is days [1,2,3,4,5,6,7,8,9,10,11]
  - First X = days [1-10], first y = day 11's close price
  - Second X = days [2-11], second y = day 12's close price

### 3. Data Reshaping and Splitting
```python
# Reshape X to match CNN input shape (batch_size, channels, sequence_length)
X = np.transpose(X, (0, 2, 1))  # Reshape to (samples, features, sequence_length)

# Split the data
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
```
- **Reshaping**: CNN expects data in format (batch_size, channels, sequence_length)
  - Channels = 5 features (Open, Close, Change, sentiment, sentiment_score)
  - Sequence_length = 10 days
- **Train-Test Split**: 
  - 80% training data, 20% testing data
  - `random_state=42` ensures reproducibility

### 4. PyTorch Data Preparation
```python
# Convert to PyTorch tensors
X_train = torch.FloatTensor(X_train)
X_test = torch.FloatTensor(X_test)
y_train = torch.FloatTensor(y_train)
y_test = torch.FloatTensor(y_test)

# Create data loaders
batch_size = 32
train_loader = DataLoader(list(zip(X_train, y_train)), batch_size=batch_size, shuffle=True)
test_loader = DataLoader(list(zip(X_test, y_test)), batch_size=batch_size)
```
- Converts NumPy arrays to PyTorch tensors
- **DataLoader**: 
  - Handles batching of data
  - `batch_size=32`: Processes 32 samples at once
  - `shuffle=True`: Randomizes training data order each epoch

### 5. CNN Architecture
```python
class CNN(nn.Module):
    def __init__(self, input_shape: int, hidden_units: int, output_shape: int):
        super().__init__()
        self.conv_block_1 = nn.Sequential(
            nn.Conv1d(in_channels=5,
                     out_channels=hidden_units,
                     kernel_size=3,
                     stride=1,
                     padding=1),
            nn.ReLU(),
            nn.BatchNorm1d(hidden_units),
            nn.MaxPool1d(kernel_size=2)
        )
```
- **Conv1d Layer**:
  - `in_channels=5`: Number of input features
  - `out_channels=hidden_units`: Number of filters/features to learn
  - `kernel_size=3`: Each filter looks at 3 time steps
  - `padding=1`: Preserves sequence length
- **ReLU**: Non-linear activation function
- **BatchNorm**: Normalizes layer outputs, helps training
- **MaxPool**: Reduces sequence length by half, captures important features

### 6. Training Loop
```python
num_epochs = 100
train_losses = []

for epoch in range(num_epochs):
    model.train()
    epoch_losses = []
    
    for X_batch, y_batch in train_loader:
        # Forward pass
        outputs = model(X_batch)
        loss = criterion(outputs.squeeze(), y_batch)
        
        # Backward pass and optimize
        optimizer.zero_grad()
        loss.backward()
        optimizer.step()
```
- **Epochs**: Complete passes through training data
- **Training Steps**:
  1. Forward pass: Make predictions
  2. Calculate loss (MSE between predictions and actual values)
  3. Backpropagation: Calculate gradients
  4. Optimizer step: Update model weights
- **optimizer.zero_grad()**: Clears previous gradients
- **loss.backward()**: Computes gradients
- **optimizer.step()**: Updates weights

### 7. Evaluation and Visualization
```python
# Convert predictions back to original scale
predictions_rescaled = scaler.inverse_transform(np.hstack([np.zeros((len(predictions), 1)), 
                                              predictions, np.zeros((len(predictions), 3))]))[: , 1]
actuals_rescaled = scaler.inverse_transform(np.hstack([np.zeros((len(actuals), 1)), 
                                          actuals, np.zeros((len(actuals), 3))]))[: , 1]

# Calculate metrics
mse = mean_squared_error(actuals_rescaled, predictions_rescaled)
r2 = r2_score(actuals_rescaled, predictions_rescaled)
```
- **Inverse Transform**: Converts predictions back to original price scale
- **Metrics**:
  - MSE: Average squared difference between predictions and actuals
  - R²: Proportion of variance in target explained by model (1 is perfect)
- **Visualization**:
  - Plots actual vs predicted prices
  - Shows training loss over time to diagnose overfitting/underfitting

This CNN model learns patterns in the time series data to predict the next day's closing price based on the previous 10 days of market data and sentiment information.


# Results (Open, sentiment_score features)

### LSTM
Test Loss (MSE): 0.003414042992517352
Mean Absolute Error (MAE): 17.91974069265318
R-squared (R2): 0.8847687026927461

### CNN
Test Loss: 0.00458742119371891
Mean Absolute Error (MAE): 22.51078424261634
R-squared (R2): 0.8906733949187364

### CNN-LSTM
Test Loss: 0.0027609667740762234
Mean Absolute Error: 0.031072668731212616
R-squared Score: 0.9099305272102356

# Results of models (using 80:20 split)
## Malta Independant
### LSTM (Without Sentiment Variable)
Test Loss (MSE): 0.0005052234046161175  
Mean Absolute Error (MAE): 31.609900023181  
R-squared (R2): 0.8499226893849482

### LSTM (With Sentiment Variable)
Test Loss (MSE): 0.00017181661678478122  
Mean Absolute Error (MAE): 14.83542593518725  
R-squared (R2): 0.9489616321833064

### CNN (Without Sentiment Variable)
Test Loss: 0.0006718079675920308  
Mean Absolute Error (MAE): 27.978281632733594  
R-squared (R2): 0.9925441399012059

### CNN (With Sentiment Variable)
Test Loss: 0.0003431527002248913  
Mean Absolute Error (MAE): 21.338293489057783  
R-squared (R2): 0.9961924779859842

### LSTM-CNN (Without Sentiment Variable)
Test Loss: 6.752867921022698e-05  
Mean Absolute Error: 0.005748416297137737  
R-squared Score: 0.9809779524803162

### LSTM-CNN (With Sentiment Variable)
Test Loss: 0.0004366027133073658  
Mean Absolute Error: 0.01857767254114151  
R-squared Score: 0.8770139217376709

## Malta Business Weekly
### LSTM (Without Sentiment Variable)
Test Loss (MSE): 0.004844771232455969  
Mean Absolute Error (MAE): 22.84890668012559  
R-squared (R2): 0.8364785544463473

### LSTM (With Sentiment Variable)
Test Loss (MSE): 0.003929056227207184  
Mean Absolute Error (MAE): 19.498368677307738  
R-squared (R2): 0.8673858845904483

### CNN (Without Sentiment Variable)
Test Loss: 0.0045250775292515755  
Mean Absolute Error (MAE): 22.37676582544003  
R-squared (R2): 0.8921590963553585

### CNN (With Sentiment Variable)
Test Loss: 0.0026346512604504824  
Mean Absolute Error (MAE): 17.783706468564006  
R-squared (R2): 0.9375191722991122

### LSTM-CNN (Without Sentiment Variable)
Test Loss: 0.0024828610476106405  
Mean Absolute Error: 0.027093494310975075  
R-squared Score: 0.9190030097961426

### LSTM-CNN (With Sentiment Variable)
Test Loss: 0.00026312240515835583  
Mean Absolute Error: 0.012569311074912548  
R-squared Score: 0.9258814454078674

# Results of models (using time series cross validation)
## Malta Independent
### LSTM (Without Sentiment)
Average Results:
Average MAE: 0.0645
Average R2 Score: -0.3523

### LSTM (With Sentiment)
Average Results:
Average MAE: 0.1590
Average R2 Score: -0.1212

### CNN (Without Sentiment)
Average Results:
Average MAE: 0.0647
Average R2 Score: -0.3268

### CNN (With Sentiment)
Average Results:
Average MAE: 0.1686
Average R2 Score: -0.2462

### CNN-LSTM (Without Sentiment)
Average Results:
Average MAE: 0.0647
Average R2 Score: -0.2970

### CNN-LSTM (WitH Sentiment)
Average Results:
Average MAE: 0.1616
Average R2 Score: -0.1008

## Malta Business Weekly
### LSTM (Without Sentiment)
Average Results:
Average MAE: 0.0786
Average R2 Score: -0.0311

### LSTM (With Sentiment)
Average Results:
Average MAE: 0.1918
Average R2 Score: -0.0367

### CNN (Without Sentiment)
Average Results:
Average MAE: 0.0876
Average R2 Score: -0.1880

### CNN (With Sentiment)
Average Results:
Average MAE: 0.1913
Average R2 Score: -0.0979

### CNN-LSTM (Without Sentiment)
Average Results:
Average MAE: 0.0805
Average R2 Score: -0.0561

### CNN-LSTM (WitH Sentiment)
Average Results:
Average MAE: 0.1973
Average R2 Score: -0.0955


# takewaay

Include technical indicators (moving averages, RSI, MACD, volatility).

Add macro factors (interest rates, economic indicators).

Include trading volume as a feature.