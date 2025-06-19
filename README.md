
#### Multiclass Classification of Tifinagh Characters
This project implements a Multilayer Perceptron (MLP) neural network for the multiclass classification of handwritten Tifinagh characters using the AMHCD dataset.
###  Dataset
• Name: Amazigh Handwritten Character Database (AMHCD)
• Source: Kaggle - benaddym/amazigh-handwritten-character-database-amhcd • Size: 33 classes × 780 images = 25,740 images
• Format: RGB images written by 60 writers (diverse in age, gender, profession)
###  Model Architecture
• Input: 32×32 RGB images → Flattened to 3072 features • Hidden Layers:
• Dense(64), ReLU
• Dense(32), ReLU
• Output: Dense(33), Softmax
• Loss Function: Categorical Cross-Entropy • Optimizer: Adam
• Regularization: L2
• Additional:
• Data Augmentation (rotation, translation) • K-Fold Cross Validation
# Filtrage-des-images-en-python

Ce travail s'inscrit dans mon parcours académique en matière de "Traitement et codage d'images et de vidéos" en 2ème année d'Ingénierie des Données et Systèmes Décisionnels.

Ce script Python est une application des filtres passe-haut et des filtres passe-bas avec une visualisation des résultats.

## Introduction:
Nous entendons par filtrage la réduction et l'élimination des distorsions introduites (bruit)
par le système ayant servi à acquérir l'image. Ceci est afin d'obtenir une image qui soit la plus
proche possible de l'image idéale qui aurait été obtenue si le système d'acquisition était parfait.
Durant ce Tp, vous allez survoler certains filtres d’images allant des filtres linéaires (passe-
bas et passe-haut) jusqu’aux filtres non linéaires tels que le filtre médian.

## Ce script comporte:
- Bruitage d'une image
- Filtrage moyenneur
- Filtrage médian
- Filtrage gaussian
- Filtrage par convolution
- Application des Filtre prédéfinis Sobel, Prewitt et Canny

#######################################################################################

This work is part of my academic journey in the subject "Image and Video Processing & Coding" in the 2nd year of Data Engineering and Decision Systems.

This Python script is an application of high-pass and low-pass filters with visualization of the results.

Introduction:
Filtering refers to the reduction and elimination of distortions (noise) introduced by the system used to acquire the image. This is done to obtain an image that is as close as possible to the ideal image that would have been obtained if the acquisition system were perfect. During this lab, you will explore various image filters, ranging from linear filters (low-pass and high-pass) to nonlinear filters such as the median filter.

This script includes:
- Adding noise to an image
- Average filtering
- Median filtering
- Gaussian filtering
- Convolution filtering
- Application of predefined filters Sobel, Prewitt, and Canny

### Installation
  # (Optional) Create virtual environment
  python -m venv venv
  source venv/bin/activate  # or .\venv\Scripts\activate on Windows
  
### Results
   Metric
Accuracy
Loss
Cross-Validation
###  References
[1] Benaddy, M., et al. Amazigh Handwritten Character Database (AMHCD). Kaggle, 2020.\ https://
www.kaggle.com/datasets/benaddym/amazigh-handwritten-character-database-amhcd