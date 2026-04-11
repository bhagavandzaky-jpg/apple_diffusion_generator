# 🍎 Apple Pixel Art Diffusion Generator
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white)

An implementation of **Generative AI** using **Diffusion Models** to create apple pixel art from scratch (random noise). This model was trained for over **4,700+ Epochs** to achieve consistent shapes and colors.

## 📸 Training Progress & Results
From pure noise to a recognizable apple. Here is the output of the model:

<p align="center">
  <img src="results/output_apple.png" width="250" alt="Generated Apple Output">
  <br>
  <i>"Purely AI-generated after 4,700+ Epochs."</i>
</p>

---

## 🚀 Quick Start (Inference)
I have simplified the process. You don't need to rebuild the architecture; just load the `.keras` file and run!

1. **Clone the repository**:
   ```bash
   git clone [https://github.com/username/apple_diffusion_generator.git](https://github.com/username/apple_diffusion_generator.git)
   cd apple_diffusion_generator
2.Install dependencies:
     pip install -r requirements.txt
3.Generate your apple:
     python main.py

🛠️ Architecture
This project implements a custom U-Net architecture designed for 32 \times 32 pixel generation, featuring:
Residual Blocks: For better gradient flow during deep training.
Sinusoidal Time Embeddings: To help the model understand which noise level it is currently denoising.
Linear Noise Schedule: 200 timesteps for stable reconstruction.


📂 Project Structure



.
├── main.py                    # Minimalist script (15 lines) to generate images
├── diffusion_apple_full.keras # Pre-trained Model (Architecture + Weights)
├── requirements.txt           # Dependencies (TensorFlow, Matplotlib, Numpy)
├── src/                       # Full training source code & notebooks
├── data/                      # Sample dataset images
└── results/                   # Gallery of generated outputs

create :Varo
🌟 Support
If you find this project interesting, feel free to leave a Star!


