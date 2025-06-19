
## Multiclass Classification of Tifinagh Characters Using a Neural Network
### Introduction
Handwritten character recognition remains a significant challenge in computer vision, particularly for underrepresented scripts such as Tifinagh, used by Amazigh communities. Unlike well-studied Latin or Arabic scripts, the geometric and non-cursive nature of Tifinagh demands specialized approaches.
This project implements a multiclass neural network — a Multilayer Perceptron (MLP) — to classify Tifinagh characters by adapting binary classification techniques to a setting with 33 distinct classes.

The Amazigh Handwritten Character Database (AMHCD) provides 28,182 grayscale images (64×64 pixels), resized to 32×32 and flattened into 1024-dimensional vectors. The MLP uses two hidden layers (64 and 32 neurons), ReLU activation functions, and a softmax output layer. The goal is to achieve high accuracy through L2 regularization and the use of the Adam optimizer, contributing to the development of OCR systems for Tifinagh script.
## Méthodologie
### Jeu de données
The AMHCD dataset contains 28,182 grayscale images of handwritten Tifinagh characters (64×64 pixels), spread across 33 classes, each representing a Tifinagh letter [1]. The data was collected from 60 writers, offering a wide variety of handwriting styles.
Images were resized to 32×32 pixels, normalized to the [0,1] range, and flattened into 1024-feature vectors.

A specific normalization was applied to the letter ‘ya’ (ⴰ) to distinguish it from ‘yar’ (ⵔ) by adding white space to reduce confusion due to their similar circular shape [1].

Stratified sampling was used to split the dataset into:

60% training

20% validation

20% testing
### Model Architecture
The MLP is structured as follows:

Input layer: 1024 neurons (flattened 32×32 image)

Hidden Layer 1: 64 neurons, ReLU

Hidden Layer 2: 32 neurons, ReLU

Output layer: 33 neurons, Softmax

## Preprocessing & Training
Images were preprocessed using OpenCV (resizing and normalization).

Labels were one-hot encoded using OneHotEncoder.

Training was conducted over 100 epochs, with a batch size of 32, a learning rate of 0.01, and L2 regularization to reduce overfitting.
optimizer = Adam(learning_rate=0.01, beta_1=0.9, beta_2=0.999)
 
## Evaluation
The model was evaluated using:

Overall Accuracy: Ratio of correctly classified images.

Classification Report: Per-class precision, recall, and F1-score.

Confusion Matrix: Visualizing classification errors.

Loss & Accuracy Curves: To track model convergence.

## Implementation
The implementation was done in Python, using the following libraries:

NumPy

OpenCV

scikit-learn

Matplotlib

Seaborn

### Results
The final MLP achieved a test accuracy of approximately 85% after 100 epochs.
The classification report showed strong performance across most classes, though confusions were noted between ‘ya’ (ⴰ) and ‘yar’ (ⵔ) due to their similar round shapes [1].

The confusion matrix (Figure 1) highlights these errors.

The training and validation curves (Figure 2) show stable convergence with no significant overfitting.

The Adam optimizer helped speed up convergence, and L2 regularization improved generalization by reducing weight magnitude.
### Reference
[1] Benaddy, M., et al. Amazigh Handwritten Character Database (AMHCD), Kaggle, 2020.
🔗 https://www.kaggle.com/datasets/benaddym/amazigh-handwritten-character-database-amhcd



`   

