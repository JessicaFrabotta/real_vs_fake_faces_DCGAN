# Real vs Fake faces DCGAN

## 📌 Ideas behind our project
Our project is articulated in three main components:

1. **Convolutional Neural Network (CNN)** – used to solve the binary classification task.  
2. **Deep Convolutional Generative Adversarial Network (DCGAN)** – used to produce some examples to validate the CNN model on additional unseen data.  
3. **Real-time System** – detects face images from a video and, for each frame, uses the CNN model to classify the identified face.

---

## 🧠 What is a CNN?
A **Convolutional Neural Network (CNN)** is a deep learning neural network designed for processing structured arrays of data such as images.  

CNNs are widely used in computer vision and have become the **state of the art** for many visual applications such as **image classification**.  

They are very effective at picking up patterns in the input image, such as:  
- Lines  
- Gradients  
- Circles  
- Eyes and faces  

It is this property that makes CNNs so powerful for computer vision.  

Other important properties of CNNs are still being explored in the project. 🚀

### 🔎 Other important properties of CNNs
- **Translation invariance**: the ability to ignore positional shifts of the target in the image.  
  *Example: a cat is still a cat regardless of whether it appears in the top or bottom half of the image.*  

- **Translation equivariance**: for a CNN the position of the object in the image should not be fixed in order to be detected.  
  *Example: a cat is still recognized as a cat even if we change its color and then its position (or vice versa). In short, if the input changes, the output also changes.*

![Real vs Fake CNN](projects_images/cnn.png)

## 🧩 Deep Convolutional Generative Adversarial Network (DCGAN)

A **Deep Convolutional Generative Adversarial Network (DCGAN)** is basically a GAN architecture that uses convolutions.  
GANs are composed of two main networks called **discriminator** and **generator**, which try to improve each other.  

In the case of DCGANs, instead of simple two-layer feed-forward networks, both generator and discriminator are implemented as **convolutional neural networks**:  

- **Generator**: takes random noise in the latent vector and maps it to the data space.  
  If we are using RGB images, this means creating an RGB image.  
  It starts with a dense/fully connected layer, followed by **transpose convolution** and the **Leaky ReLU activation function**.  

- **Discriminator**: a binary classification network that takes both real and fake images and outputs a probability of whether the given image is real or fake.

![Deep Convolutional Generative Adversarial Network](projects_images/DCGAN.png)
