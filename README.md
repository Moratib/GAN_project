(SGAN) for Predicting Cryptocurrency Prices
This repository contains the implementation of a Supervised Generative Adversarial Network (SGAN) designed to predict cryptocurrency prices during periods of conflict. The model leverages sentiment analysis and various machine learning techniques to generate and classify realistic images for analysis.

Overview
The SGAN combines the strengths of supervised learning and generative adversarial networks to improve classification performance on labeled data while simultaneously leveraging unlabeled data. This approach is particularly useful for predicting cryptocurrency prices, where labeled data can be scarce and expensive to obtain.

Key Components
1. Dataset
The dataset used for this project includes natural images, resized to dimensions of 224x224 pixels, with 8 classes. The images are preprocessed and loaded using the Dataset class, which handles both labeled and unlabeled data.

2. Model Architecture
Generator: Creates realistic images from random noise.
Discriminator: Classifies images as real or fake, and also assigns class labels to real images.


3. Training
The training process involves:

Training the discriminator on real and fake images.
Training the generator to create images that fool the discriminator.
Leveraging both labeled and unlabeled data to improve the performance of the model.


4. Implementation Details
Generator: Upsamples noise vectors to generate 224x224 images.
Discriminator: Distinguishes between real and fake images and classifies real images into one of the predefined classes.
SGAN Training: Alternates between training the discriminator and the generator to improve both components iteratively.

Results
The trained SGAN model achieves improved classification accuracy by effectively utilizing both labeled and unlabeled data. The generator learns to produce realistic images, while the discriminator becomes proficient in distinguishing real from fake and classifying real images.
