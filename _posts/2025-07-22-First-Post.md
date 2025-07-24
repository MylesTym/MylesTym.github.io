---
title: Generating 'handwritten' Digits Using Autoencoder and MNIST data
date: 2025-07-22
image: /assets/autoencoder.png
blurb: A modular and extensible Python project implementing convolutional autoencoders using TensorFlow and Keras for image denoising and dimensionality reduction.
---

# Autoencoder Generator


A modular and extensible Python project implementing convolutional autoencoders using TensorFlow and Keras for image denoising and dimensionality reduction.

---

## Project Overview

This project demonstrates the design and training of convolutional autoencoders with configurable latent dimensions. It emphasizes noise-robust learning by training models on noisy input data to reconstruct clean images. The architecture is structured for clarity and flexibility, supporting experimentation with different encoder and decoder configurations.

---

## Highlights

- **Custom Autoencoder Architecture:** Clean, modular implementation of encoder and decoder networks using TensorFlow Keras.  
- **Noise Augmentation:** Incorporates Gaussian noise to training data to improve denoising capabilities.  
- **Reconstruction Visualization:** Tools to compare original, noisy, and reconstructed images to evaluate model effectiveness.  
- **Extensible Design:** Easily adaptable codebase for experimenting with alternative architectures or datasets.

---

## Technologies Used

- Python 3.x  
- TensorFlow 2.x  
- NumPy  
- Matplotlib  

---

## Project Structure Overview

- `autoencoder.py`: Defines the Autoencoder model class with separate encoder and decoder.  
- `data_preprocessing.py`: Contains utilities for loading datasets and applying noise.  
- `train.py`: Script managing the training loop and model evaluation.  
- `notebooks/`: Jupyter notebooks with example experiments and visualizations.

---

## Repository

[GitHub Repository](https://github.com/MylesTym/Autoencoder_generator)

---

## Contact

For inquiries or collaborations, please contact me at [your.email@example.com].

---

*This project reflects practical skills in deep learning model development, data augmentation techniques, and Python programming relevant to image processing and unsupervised learning.*
