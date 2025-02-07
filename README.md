# 📊 Monet Paintings Generation

This project uses Generative Adversarial Networks (GANs) to generate images in the style of Claude Monet. The goal is to transform photographs into beautiful paintings that resemble Monet's iconic style using deep learning techniques.

## 📁 Project Structure

data/ # Dataset used for training and testing the models. 
  monet_jpg/ # Monet images in JPG format 
  photo_jpg/ # Real-life photographs in JPG format 
  monet_tfrec/ # Monet images in TFRecord format 
  photo_tfrec/ # Real-life photographs in TFRecord format 
notebooks/ # Jupyter notebook

## 🧠 Problem Statement

The task is to use GANs to generate Monet-style paintings from real-life photographs. By training a GAN to generate new images in the style of Monet, we aim to create artwork that closely mimics his unique color palettes, brush strokes, and stylistic features.

We aim to:

- Build a generator to create images in Monet's style.
- Use a discriminator to distinguish between real Monet images and generated ones.
- Use loss functions such as **Cycle Consistency** and **Identity Loss** to improve image quality and maintain the key features of original photographs.

## ⚙️ Key Features

- **Dual Generator Architecture**: We use two generators:
  - One that converts Monet-style images to real photos (Monet → Photo).
  - Another that converts real photos to Monet-style images (Photo → Monet).
  
- **Cycle Consistency**: To preserve important features of the original images, the model uses cycle consistency loss (i.e., a photo-to-Monet-to-photo cycle) to ensure transformations are reversible.

- **Identity Loss**: This loss ensures that if a photo is passed through the photo-to-Monet generator, it stays identical to the original photograph.

- **Stable Training with LS-GAN**: We use Least Squares GAN (LS-GAN) for stable training and realistic image generation.

- **ResNet Blocks**: The generator is built with ResNet blocks for improved learning and stable training, making the output images smoother and more natural.

## 🔍 Results

The model successfully generates Monet-style paintings from real photographs. The generated images exhibit strong stylistic features resembling Monet’s iconic brushwork and color choices.

Sample results:

- **Input**: A real-life photo.
- **Output**: A Monet-styled painting created from the photo.

### Example Generated Image

![__results___50_1-1](https://github.com/user-attachments/assets/5e786bba-4197-40de-a9f8-d68540904c53)



## 🛠️ Tools & Libraries

The project leverages the following tools and libraries:

- **PyTorch**: For building and training the GAN model.
- **torchvision**: For image transformations and dataset handling.
- **PIL**: For image loading and preprocessing.
- **matplotlib**: For visualizing generated images.
- **numpy**: For handling numerical data.

**Dependencies**:

- Python 3.7+
- torch==1.10.0
- torchvision==0.11.1
- matplotlib==3.4.3
- numpy==1.21.0
- tqdm==4.62.3

