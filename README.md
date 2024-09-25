# 🎨✨ Stable Diffusion Fine-Tuning 🔧💡

Welcome to the **Stable Diffusion Fine-Tuning** repository! This project empowers you to fine-tune models using custom datasets and generate stunning images effortlessly. From installation to training, we've got you covered with easy-to-follow instructions and helpful tips. Ready to dive in? 🚀

![image](https://github.com/user-attachments/assets/21cb8fcd-3444-4fee-b8d2-877211ac46fb)


---

## 🌟 Table of Contents

- [🚀 Introduction](#-introduction)  
- [⚙️ Installation](#-installation)  
- [📚 Usage](#-usage)  
- [🤝 Contributing](#-contributing)  
- [📜 License](#-license)

---

## 🚀 Introduction

This project shows you how to fine-tune a **Stable Diffusion** model using Hugging Face's `diffusers` and `transformers` libraries. Whether you’re a beginner or an AI expert, this repository will help you train custom models with **efficient memory usage**, optional GPU acceleration with `xformers`, and an interactive interface via `gradio`. Plus, you can even run this on **Google Colab for free!** 🧑‍💻🎉

---

## ⚙️ Installation

Let's get your environment ready! 🛠️ Follow these steps to install all necessary dependencies:

1. Install the required Python libraries 🐍:  
   ```bash
   pip install -U git+https://github.com/huggingface/diffusers.git  
   pip install accelerate tensorboard transformers ftfy gradio  
   pip install "ipywidgets>=7,<8"  
   pip install bitsandbytes  

2. For faster and more memory-efficient training, install `xformers`:
``` bash
  pip install -U --pre triton  
  # GPU specific installation:  
  pip install <xformers precompiled package for your GPU>
```
3. If you face GPU compatibility issues, install precompiled versions of xformers for your specific GPU:
   ```bash
     pip install -q https://github.com/TheLastBen/fast-stable-diffusion/raw/main/precompiled/<your GPU type>/xformers-0.0.13.dev0-py3-none-any.whl  
   ```
   💡 Tip: This setup supports PyTorch and JAX for even faster training. 💪

---


## 📚 Usage
1. Training a Custom Dataset 🧑‍🏫 (with `dreambooth_1.ipynb`)
Follow these steps to fine-tune your model using DreamBooth in the dreambooth_1.ipynb notebook.

⚡ Quick Steps:

- Prepare your dataset images in JPEG format.
- Upload them to Hugging Face if needed.
- Use the dreambooth_1.ipynb notebook to:
- Install the required libraries
- Configure model and dataset paths
- Run the training process

Once everything is set, 🎉 you're ready to train! 🚀

2. Generating Images 🖼️ (with `working_2.ipynb`)
After fine-tuning your model, generate images using `the working_2`.ipynb notebook. 📸✨

---

⚙️ Setup:

- Install necessary libraries for generating images.
- Load the model you trained earlier and start generating images with text prompts. 💬🔮

---

## 🤝 Contributing
👩‍💻 Contributions are welcome! Feel free to open a pull request or an issue if you want to propose new features or improvements. Don’t forget to update relevant tests.
