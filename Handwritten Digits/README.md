"""
# MNIST Digit Classifier - Neural Network

## Overview
Simple 3-layer neural network that achieves 95.3% accuracy on the MNIST handwritten digit dataset.

## Quick Start
1. Install: `pip install tensorflow numpy matplotlib`
2. Run: `python mnist_model.py`

## Model Architecture
- **Layers**: 3 (28 → 8 → 10 neurons)
- **Activations**: Sigmoid (hidden), Softmax (output)
- **Parameters**: 22,302 total
- **Input**: 784 pixels (flattened 28x28 images)
- **Output**: 10 classes (digits 0-9)

## Performance
- **Test Accuracy**: 95.30%
- **Test Loss**: 0.1642
- **Training Time**: ~30 seconds (CPU)

### Making Predictions
```python
predictions = model.predict(X_test[0:1])
digit = np.argmax(predictions[0])