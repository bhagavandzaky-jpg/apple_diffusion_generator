# 🍎 Apple Pixel Art Diffusion Generator

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white)

A specialized **Generative AI** implementation using **Diffusion Models** to create apple pixel art assets from scratch (Gaussian noise). This model was trained for over **4,700+ Epochs** to master consistent shapes, shading, and pixel-perfect structures.

---

## 📸 Training Progress & Results

Watch the transformation from pure chaotic noise to a structured digital apple. This result is the product of thousands of training iterations:

| Initial Noise | Mid-Denoising | Final AI Output |
| :---: | :---: | :---: |
| ![Noise](https://via.placeholder.com/150?text=Initial+Noise) | ![Mid](https://via.placeholder.com/150?text=Step+100) | ![Final](https://via.placeholder.com/150?text=Generated+Apple) |

> *"Purely AI-generated after 4,700+ Epochs of training."*

---

## 🚀 Instant Inference (No Training Required)

The best part? **You don't need to spend days training the model.** I have included the pre-trained weights in this repository. You can generate new pixel art instantly by loading the existing model.

### 1. Clone & Setup
```bash
git clone [https://github.com/username/apple_diffusion_generator.git](https://github.com/username/apple_diffusion_generator.git)
cd apple_diffusion_generator
pip install -r requirements.txt
###2. Run the Generator
Simply run the main script. It will automatically load the model and produce a new image:
    python main.py
###3. Manual Loading (Complete Python Code)
If you want to integrate this model into your own project, use this script to load and generate images in one go:

import tensorflow as tf
import matplotlib.pyplot as plt
import numpy as np

# 1. Load the pre-trained "brain"
model = tf.keras.models.load_model('diffusion_apple_full.keras')

# 2. Create raw noise (the base for AI to draw)
noise = np.random.normal(0, 1, (1, 32, 32, 3)) 

# 3. AI transforms noise into a Pixel Apple
generated_img = model.predict(noise)

# 4. Display the result (Normalization [-1, 1] to [0, 1])
plt.imshow((generated_img[0] + 1) / 2.0)
plt.axis('off')
plt.show()




🛠️ Model Architecture
This project features a custom U-Net Architecture optimized for 32 \times 32 pixel generation:
Residual Blocks: Enhances gradient flow for deep feature learning.
Sinusoidal Time Embeddings: Helps the model track the noise level at each step.
Linear Noise Schedule: 200 timesteps for high-fidelity reconstruction.


📂 Project Structure

.
├── main.py                    # Instant generation script (Ready to use)
├── diffusion_apple_full.keras # Pre-trained Model (Architecture + Weights)
├── requirements.txt           # Necessary libraries (TF, Matplotlib, Numpy)
├── src/                       # Complete source code & training notebooks
├── data/                      # Sample dataset used for training
└── results/                   # Gallery of AI-generated apples


👤 Author
Developed with passion by Varo
