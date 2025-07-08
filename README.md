# Quantum Machine Learning for Leukemia Classification

A quantum neural network implementation for automated leukemia detection from microscopy images using hybrid classical-quantum machine learning techniques.

## Overview

This project, developed as a potential thesis project, investigates the application of quantum computing to medical image classification, specifically for detecting leukemia cells in microscopy images. The implementation combines classical image preprocessing with quantum feature encoding and variational quantum circuits to achieve high-accuracy classification.

## Features

- **Quantum Neural Network**: 16-qubit variational quantum circuit for pattern recognition
- **Medical Image Processing**: Handles high-resolution microscopy images (450×450 pixels)
- **Hybrid Optimization**: Classical-quantum hybrid training using BFGS optimization
- **Real Dataset**: Trained on Fold_0 of the C-NMC Leukemia classification dataset
- **High Accuracy**: Achieved 100% classification accuracy on test batch

## Technical Architecture

### Quantum Components
- **Quantum Device**: PennyLane default.qubit simulator with 16 qubits
- **Encoding**: Angle encoding (RY rotations) for pixel intensity mapping
- **Variational Circuit**: Parametrized quantum circuit with trainable parameters
- **Measurement**: Pauli-Z expectation values for classification

### Classical Components
- **Image Preprocessing**: TensorFlow/Keras image augmentation and normalization
- **Data Loading**: ImageDataGenerator for batch processing
- **Optimization**: SciPy BFGS optimizer for parameter training

## Installation

```bash
# install required packages
pip install pennylane tensorflow numpy matplotlib scikit-learn scipy

# for quantum computing
pip install pennylane-default-qubit
```

## Dataset

The project uses the C-NMC Leukemia dataset:
- **Training**: 3,527 images across 2 classes
- **Validation**: 1,867 images across 2 classes
- **Image Size**: 450×450 RGB microscopy images
- **Classes**: Leukemia cells vs. Normal cells

## Results

- **Training Accuracy**: Successfully converged during optimization
- **Test Accuracy**: 100% on evaluation batch
- **Model Size**: 16 trainable quantum parameters
- **Quantum Advantage**: Demonstrated effective pattern recognition in high-dimensional medical data

## Project Structure

```
quantum-leukemia-classification/
├── qc_Cir.ipynb              # Main implementation notebook
├── README.md                 # README file
└── requirements.txt          # Python dependencies
```

## Key Technologies

- **PennyLane**: Quantum machine learning framework
- **TensorFlow/Keras**: Classical image processing and data handling
- **NumPy**: Numerical computations
- **SciPy**: Classical optimization algorithms
- **Matplotlib**: Visualization and plotting

## Future Enhancements

- [ ] Implement quantum convolutional layers
- [ ] Test on larger datasets
- [ ] Compare with classical CNN baselines
- [ ] Add quantum noise modeling
- [ ] Implement quantum transfer learning

## License

This project is for educational and research purposes.

---

**Note**: This implementation is designed for research and educational purposes. For clinical applications, extensive validation and regulatory approval would be required.