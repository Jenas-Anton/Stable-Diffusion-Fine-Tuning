# Stable Diffusion FineTuning 

This repository contains code and resources for fine-tuning and utilizing machine learning models. The project focuses on training models using customized datasets, providing tools for model evaluation, and generating images.

![image](https://github.com/user-attachments/assets/21cb8fcd-3444-4fee-b8d2-877211ac46fb)




# Table of Contents
- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Introduction 
This project demonstrates how to set up and fine-tune a Stable Diffusion model using Hugging Face's `diffusers` and `transformers` libraries. The setup includes efficient memory usage techniques, optional GPU acceleration with xformers, and a user-friendly interface via `gradio`. This workflow enables you to train custom models and generate high-quality images leveraging JAX or PyTorch.This also works on google collab for free. 

## Installation
To set up the environment, install the necessary dependencies as outlined below:

1. Install the required Python libraries:
   ```bash
   pip install -U git+https://github.com/huggingface/diffusers.git
   pip install accelerate tensorboard transformers ftfy gradio
   pip install "ipywidgets>=7,<8"
   pip install bitsandbytes
   ```
2. For faster and more memory-efficient training, install `xformers`:
   ```bash
   pip install -U --pre triton
   # GPU specific installation:
   pip install <xformers precompiled package for your GPU>
   ```
3. Optionally, if you encounter GPU compatibility issues, use the following for specific GPU types:
   
```bash
pip install -q https://github.com/TheLastBen/fast-stable-diffusion/raw/main/precompiled/<your GPU type>/xformers-0.0.13.dev0-py3-none-any.whl
```


## Usage


This project consists of two main notebooks for training and generating images:

### Training a Dataset (Using `dreambooth_1.ipynb`)

1. **Setup**: Use the `dreambooth_1.ipynb` notebook to train a custom model using DreamBooth. 
   - Ensure your dataset images are pre-processed and formatted as JPEG files.
   - If your dataset is hosted on Hugging Face, upload it to a Hugging Face dataset using the required format (JPEG).
   - Open the `dreambooth_1.ipynb` notebook and follow the steps to:
     - Install required libraries.
     - Configure model and dataset paths.
     - Run the training process with your dataset.

   ```bash
   # Install necessary dependencies (from the notebook)
   pip install diffusers transformers gradio ftfy accelerate jaxlib jax

2. Running the Training: After configuring, run the notebook to fine-tune the Stable Diffusion model on your dataset
3. Uploading Images:

- You must upload your dataset images to a Hugging Face dataset.
- The images should be in JPEG format.
- You can upload the dataset manually or via a Hugging Face script as demonstrated in the notebook.

### Generating Images (Using `working_2.ipynb`)
Once your model is trained, you can use the `working_2.ipynb` notebook for image generation. This notebook allows you to load the model and generate images based on text prompts.

Setup:

Open the `working_2.ipynb` notebook.
1. Install necessary libraries:
```bash
pip install diffusers transformers gradio ftfy accelerate jaxlib jax
```
2. Generating Images:
- Load your trained model (you can use the one trained with `dreambooth_1.ipynb`).
- Use a text prompt to generate an image
- You can also generate images directly in the dreambooth_1.ipynb notebook after training.
3. Note on Hugging Face Datasets:
- If using a custom dataset, ensure that the images are uploaded to a Hugging Face dataset or are already part of one.
- All images in the dataset must be in JPEG format to be compatible with the training and generation processes.




## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.


