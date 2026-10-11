OVERVIEW:
Generative Adversarial Networks (GANs) are deep learning models made up of two parts:

a Generator that produces synthetic data, and

a Discriminator that distinguishes real data from generated data.

This project explores several GAN architectures and implements a simplified StyleGAN-inspired model in PyTorch using the Fashion-MNIST dataset.

 GOALS:
Explore different GAN architectures.

Generate synthetic fashion images.

Understand StyleGAN’s style-based generation process.

Perform latent-space interpolation and style mixing experiments.

🧠 GAN Variants
Vanilla GAN – basic generator and discriminator with fully connected layers.

Conditional GAN (cGAN) – generates data conditioned on labels.

DCGAN – uses CNNs for better image generation.

SRGAN – super-resolution GAN for high-res outputs.

CycleGAN – image-to-image translation without paired datasets.

StyleGAN – enables controllable styles at different synthesis stages.

LAPGAN – progressive generation using a multi-resolution pyramid.

🎨 StyleGAN Architecture
StyleGAN maps latent noise into an intermediate space and uses style vectors to control image generation.

Key components:

Mapping Network: Converts latent vector 
𝑧
 into style vector 
𝑤
.

Learned Constant: Provides a fixed input tensor for synthesis.

Synthesis Network: Upsampling + convolution layers with AdaIN.

AdaIN: Applies style-dependent scaling and bias.

Discriminator: Classifies outputs as real or fake.

Flow Diagram

Latent Vector (z)
       ↓
 Mapping Network (z → w)
       ↓
 Learned Constant
       ↓
 Synthesis Blocks (Upsample + Conv + AdaIN)
       ↓
 Generated Image
       ↓
 Discriminator (Real/Fake)
 
🧪 Experiments

Image Generation – train GAN on Fashion-MNIST to produce synthetic clothing images.

Latent-Space Interpolation – interpolate between latent vectors to observe smooth transitions.

Style Mixing – combine style vectors at different synthesis stages for controllable outputs.

⚙️ Setup
Parameter	Value
Dataset	Fashion-MNIST
Training images	5,000
Image size	32 × 32
Latent dimension	32
Batch size	128
Epochs	10
Optimizer	Adam
Framework	PyTorch


🛠️ Tech Stack
Python

PyTorch

Torchvision

NumPy

Matplotlib

Jupyter Notebook

🚀 How to Run
bash
git clone <your-repository-url>
cd GAN-StyleGAN
pip install torch torchvision numpy matplotlib jupyter
jupyter notebook
Open STYLEGAN.ipynb and run the cells sequentially.

📊 Results
Generated Fashion-MNIST images.

Training loss curves for generator and discriminator.

Latent-space interpolation visualizations.

Style-mixing outputs.

⚠️ Limitations

This is a simplified StyleGAN-inspired model.
Low-resolution outputs.
Limited dataset size.
Short training duration.

🔮 Future Work

Train for more epochs.
Use larger datasets and higher resolutions.
Compare with DCGAN and official StyleGAN.
Evaluate image quality metrics.

✅ Conclusion
This project demonstrates GAN fundamentals and highlights style-based image generation through training, interpolation, and style mixing on Fashion-MNIST.
