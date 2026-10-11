# GANs and StyleGAN

## 📌 Overview

Generative Adversarial Networks (GANs) are deep learning models consisting of two neural networks: a **Generator**, which creates synthetic data, and a **Discriminator**, which distinguishes real data from generated data.

This project explores different GAN architectures and implements a simplified StyleGAN-inspired model using PyTorch and the Fashion-MNIST dataset.

## 🎯 Objectives

- Understand different GAN architectures.
- Generate synthetic fashion images.
- Study StyleGAN architecture and style-based generation.
- Perform latent-space interpolation and style mixing.

## 🧠 Types of GANs

- **Vanilla GAN:** Basic generator and discriminator using fully connected layers.
- **Conditional GAN (cGAN):** Generates data based on labels or conditions.
- **DCGAN:** Uses CNNs for improved image generation.
- **SRGAN:** Generates high-resolution images from low-resolution inputs.
- **CycleGAN:** Performs image-to-image translation without paired data.
- **StyleGAN:** Generates images with controllable styles at different synthesis stages.
- **LAPGAN:** Generates images progressively using a multi-resolution pyramid.

## 🎨 StyleGAN Architecture

StyleGAN maps random latent noise into an intermediate latent space and uses style information to control image generation.

**Main components:**
- **Mapping Network:** Converts latent vector \(z\) into style vector \(w\).
- **Learned Constant:** Initializes the synthesis network.
- **Synthesis Network:** Uses convolutional layers and upsampling to generate images.
- **AdaIN:** Applies style-dependent scaling and bias to feature maps.
- **Discriminator:** Classifies images as real or fake.

### Architecture Flow

```text
Latent Vector (z)
       |
       v
 Mapping Network
     z -> w
       |
       v
 Learned Constant
       |
       v
 Synthesis Blocks
 (Upsampling + Conv
      + AdaIN)
       |
       v
 Generated Image
       |
       v
 Discriminator
 (Real or Fake)
```

## 🧪 Experiments

### 1. Image Generation
Train the generator and discriminator on Fashion-MNIST to generate synthetic grayscale clothing images.

### 2. Latent-Space Interpolation
Interpolate between two latent vectors to observe gradual changes in generated images.

### 3. Style Mixing
Combine style vectors from two latent inputs at different synthesis stages to demonstrate style-based control.

## ⚙️ Configuration

| Parameter | Value |
|---|---|
| Dataset | Fashion-MNIST |
| Training images | 5,000 |
| Image size | 32 × 32 |
| Latent dimension | 32 |
| Batch size | 128 |
| Epochs | 10 |
| Optimizer | Adam |
| Framework | PyTorch |

## 🛠️ Technologies

- Python
- PyTorch
- Torchvision
- NumPy
- Matplotlib
- Jupyter Notebook

## 🚀 How to Run

```bash
git clone <your-repository-url>
cd GAN-StyleGAN
pip install torch torchvision numpy matplotlib jupyter
jupyter notebook
```

Open `STYLEGAN.ipynb` and run the cells in order.

## 📊 Expected Results

- Generated fashion images.
- Generator and discriminator training losses.
- Latent-space interpolation visualizations.
- Style-mixing visualizations.

## ⚠️ Limitations

This is a simplified StyleGAN-inspired model, not the complete official StyleGAN architecture. Its low-resolution images, limited dataset, and short training duration may affect image quality.

## 🔮 Future Improvements

- Train for more epochs.
- Use larger datasets and higher image resolutions.
- Compare results with DCGAN and official StyleGAN.
- Evaluate generated image quality.

## ✅ Conclusion

This project demonstrates GAN fundamentals and explores style-based image generation through training, latent-space interpolation, and style mixing using Fashion-MNIST.
