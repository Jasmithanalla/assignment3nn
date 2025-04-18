# Homeassignment3
# README - Home Assignment 3 (Neural Networks and Deep Learning)

## Student Information
*Name:* Jasmitha Nalla
*Course:* CS5720 Neural Networks and Deep Learning  
*Semester:* Spring 2025  
*University:* University of Central Missouri  
*Student ID :* 700779225



---

## Assignment Overview
This assignment consists of four tasks involving Autoencoders and Recurrent Neural Networks (RNNs). The tasks include implementing a basic autoencoder, a denoising autoencoder, a character-based text generation model using LSTMs, and a sentiment classification model using an LSTM network.

---

## Q1: Implementing a Basic Autoencoder

### Description:
An autoencoder is a neural network used to reconstruct its input. In this task:
- The MNIST dataset is used.
- The encoder compresses input images into a latent space (dimension = 32).
- The decoder reconstructs images from this compressed representation.

### Steps:
1. Load the MNIST dataset.
2. Define an autoencoder using fully connected Dense layers.
  Ans:This autoencoder is suitable for input data like flattened 28x28 images (e.g., MNIST).

Autoencoder Architecture
Encoder:

Input layer: 784 units (for 28x28 images)

Hidden layer: 32 units (compressed representation)

Decoder:

Hidden layer: 32 units

Output layer: 784 units (reconstructed image

3. Train the model using binary cross-entropy loss.
4. Visualize original vs. reconstructed images.
5. Experiment with different latent space sizes (16, 64) to analyze reconstruction quality.


---

## Q2: Implementing a Denoising Autoencoder

### Description:
A denoising autoencoder is trained to remove noise from images. This task modifies the previous autoencoder by:
- Adding Gaussian noise to input images.
- Training the model to reconstruct clean images.
- Comparing results between the standard and denoising autoencoders.

### Steps:
1. Modify the autoencoder to accept noisy input images.
2. Train the model while keeping the output as clean images.
3. Compare reconstruction quality of noisy vs. clean images.
4. Explain a real-world application of denoising autoencoders (e.g., medical imaging).
  Ans: Denoising autoencoders are widely used in medical imaging to improve image quality by removing noise and artifacts, which is crucial for accurate diagnosis and analysis.

Example: Denoising in Chest X-Ray and Brain MRI Imaging

How it works:
In medical imaging, images such as X-rays, MRIs, or ultrasound scans often suffer from noise due to low-dose acquisition, patient movement, or limitations of imaging equipment. Denoising autoencoders are trained by intentionally corrupting clean medical images with noise and teaching the model to reconstruct the original, clean images from these noisy inputs

---

## Q3: Implementing an RNN for Text Generation

### Description:
This task involves training an LSTM-based RNN to predict the next character in a text dataset.

### Steps:
1. Load a text dataset (e.g., Shakespeare Sonnets).
2. Convert text into sequences (one-hot encoding or embeddings).
3. Define an LSTM-based model.
  Ans: A Long Short-Term Memory (LSTM) model is a type of recurrent neural network (RNN) designed to effectively learn and remember long-term dependencies in sequential data, such as time series, text, or speech. Unlike traditional RNNs, LSTMs use a specialized architecture with memory cells and gating mechanisms to address issues like the vanishing gradient problem, enabling them to retain information over many time steps
4. Train the model to predict the next character.
5. Generate new text and explain the effect of temperature scaling on randomness.

---

## Q4: Sentiment Classification Using RNN

### Description:
An LSTM-based model is used to classify IMDB movie reviews as positive or negative.

### Steps:
1. Load the IMDB dataset.
2. Preprocess text data (tokenization, padding sequences).
3. Train an LSTM model for binary classification.
4. Generate a confusion matrix and classification report.
5. Discuss the importance of the precision-recall tradeoff in sentiment analysis.
Ans:The precision-recall tradeoff is a fundamental consideration in sentiment analysis, directly impacting how well a model balances the cost of false positives and false negatives when classifying text as positive, negative, or neutral.

---

## Conclusion
This assignment demonstrated autoencoder-based image reconstruction, denoising techniques, character-based text generation using RNNs, and sentiment analysis using LSTMs. Each model was trained and evaluated based on performance metrics.
