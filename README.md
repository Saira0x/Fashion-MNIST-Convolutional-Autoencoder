# Fashion-MNIST-Convolutional-Autoencoder


## 📌 Overview

This project implements a **Convolutional Autoencoder** on the [Fashion-MNIST]dataset. The autoencoder learns to compress 28×28 grayscale images into a low-dimensional **bottleneck representation** (128 numbers) and then reconstructs the original images from this compressed form — all without using any labels.

The goal is to understand how unsupervised feature learning works and to visualize the latent space discovered by the network.



## 🧠 Architecture

The model consists of three parts:

| Component | Layers |
|-----------|--------|
| **Encoder** | Conv2D + MaxPooling (3 blocks) → Flatten → Dense (bottleneck: 128 units) |
| **Bottleneck** | 128-dimensional latent vector |
| **Decoder** | Dense → Reshape → Conv2DTranspose + UpSampling (3 blocks) → Cropping to 28×28 |

**Total Parameters:** 859,265 (all trainable)




## 📁 Dataset

- **Training set:** 60,000 images  
- **Test set:** 10,000 images  
- **Image size:** 28×28 pixels, grayscale  
- **Classes:** T-shirt/top, Trouser, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag, Ankle boot  

All pixel values were normalized to the range `[0, 1]`.

🛠️ Dependencies
Python 3.8+

TensorFlow 2.x

NumPy

Matplotlib

scikit-learn
