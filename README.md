# Character Recognition Using Neural Network

This project demonstrates a simple neural network implemented in Python for recognizing characters (A-H) based on input image data. The model uses a two-layer feedforward network (input-to-hidden and hidden-to-output) and trains using the backpropagation algorithm.

## Overview
The project recognizes characters (A-H) by training a neural network with:
- Input Layer: 144 neurons (12x12 grayscale image).
- Hidden Layer: 16 neurons.
- Output Layer: 8 neurons (corresponding to each character).

### Key Features
- Sigmoid activation function.
- Backpropagation for weight updates.
- Mean Squared Error (MSE) as the loss function.

## How It Works
1. **Weight Initialization:**
   - `w_i_h`: Weights connecting the input layer to the hidden layer.
   - `w_h_o`: Weights connecting the hidden layer to the output layer.

2. **Forward Pass:**
   - Compute activations for the hidden layer using sigmoid activation.
   - Compute activations for the output layer using sigmoid activation.

3. **Error Calculation:**
   - Compute the Mean Squared Error (MSE) between predicted and true labels.

4. **Backpropagation:**
   - Update weights from output-to-hidden and hidden-to-input layers.

5. **Prediction:**
   - Based on the trained weights, classify input images into one of the 8 characters.

## Usage
### Training the Model
The training loop processes the `dataset` and `labels`:
```python
while True:
    for img, lab in zip(dataset, labels):
        # Forward pass
        # Backpropagation

    if e <= 1e-3:
        break
```
### Predicting a Character
After training, the model predicts a character for a given input image:
```python
char = 'A' # Example character
index = 0  # Index for 'A'
# Compute activations and prediction
plt.imshow(dataset[index].reshape(12, 12), cmap='Greys')
plt.title(f'The predicted character is: {recognize(o)}')
```

## Output
The program outputs the predicted character for a given input image. For example:

- Input: A 12x12 grayscale image of the character 'A'.
- Output: A plot displaying the image and the predicted character.


