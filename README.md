# Visualising Feature Learning in Convolutional Neural Networks

## Overview
This project explores how Convolutional Neural Networks (CNNs) learn hierarchical visual features from image data. The focus of the work is feature map visualisation, showing how internal representations evolve across convolutional layers.

The project compares two datasets of different complexity:
- **MNIST**: a grayscale handwritten digit dataset
- **CIFAR-10**: a colour image dataset of real-world objects

By applying the same CNN architecture to both datasets, this project investigates how input complexity affects learned feature representations.

## Technique and Focus
- **Technique:** Convolutional Neural Networks (CNNs)
- **Focus:** Visualising Feature Learning in CNNs

Rather than covering all aspects of CNNs, this project specifically examines how feature maps change across layers and how these internal representations differ between simple and complex datasets.

## Repository Contents
- `notebook/visualising_feature_learning_in_cnns.ipynb` — main Jupyter notebook
- `tutorial/tutorial.pdf` — final tutorial document
- `images/` — saved sample images and feature map visualisations
- `requirements.txt` — required Python packages
- `LICENSE` — repository licence

## Datasets Used

### MNIST
The MNIST dataset contains grayscale images of handwritten digits (0–9). It is widely used as a benchmark dataset for image classification.

Reference:
LeCun, Y., Bottou, L., Bengio, Y., & Haffner, P. (1998). *Gradient-Based Learning Applied to Document Recognition*. Proceedings of the IEEE.

Dataset page:
http://yann.lecun.com/exdb/mnist/

### CIFAR-10
The CIFAR-10 dataset contains 10 classes of colour images:
airplane, automobile, bird, cat, deer, dog, frog, horse, ship, and truck.

Reference:
Krizhevsky, A. (2009). *Learning Multiple Layers of Features from Tiny Images*. University of Toronto.

Dataset page:
https://www.cs.toronto.edu/~kriz/cifar.html

## Model Architecture
The same CNN structure was applied to both datasets:

- Conv2D(16, 3x3, ReLU)
- MaxPooling2D(2x2)
- Conv2D(32, 3x3, ReLU)
- MaxPooling2D(2x2)
- Flatten
- Dense(64, ReLU)
- Dense(10, Softmax)

This architecture was intentionally kept simple to make feature learning easier to interpret.

## Main Workflow
1. Load and preprocess MNIST and CIFAR-10
2. Train the CNN separately on each dataset
3. Extract feature maps from the first and second convolutional layers
4. Visualise and compare learned representations
5. Discuss how dataset complexity affects feature learning

## Key Findings
- The CNN achieved very high performance on MNIST, indicating that it learned clear and meaningful digit-related features.
- Performance on CIFAR-10 was lower, reflecting the increased complexity of natural image data.
- Feature maps from MNIST were more visually interpretable, especially in early layers.
- Feature maps from CIFAR-10 were more abstract and distributed, showing that more complex data leads to more complex learned representations.

## How to Run the Project

### 1. Clone the repository
```bash
git clone <your-repository-link>
cd visualising-feature-learning-in-cnns
