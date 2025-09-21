# Diffusion Model on MNIST

## Project Overview
Diffusion models are currently a leading approach in generative modeling, offering more stable training than GANs and producing higher-quality, more diverse images. This repository contains a DDPM-like (denoising diffusion probabilistic model) diffusion model  implementation on the MNIST dataset using PyTorch. The project explores the forward diffusion process (adding noise to data over timesteps) and the reverse denoising process (sampling images step by step).

## Contents
- `ddpmlike-mnist.ipynb`: Full Colab notebook with training code, mathematical analysis, and generated samples.
- Dataset: MNIST (automatically downloaded in the notebook).
- Generated samples and reconstructions are displayed within the notebook.

## Methods:
1. **Forward Process**: Implement and fully understand the idea of gradually adding Gaussian noise to images over $T$ timesteps. Using linear noise scheduler for simplicity instead of cosine scheduler in the original paper.
2. **Reverse Process**: Trains a neural network (U-Net backbone) to predict and remove noise step by step, *not yet fully understood* (time embeddings, attention), but still included for completion and to document the full diffusion pipeline.
3. **Loss Function**: Mean squared error between predicted noise and true noise.  
4. **Sampling**: Start from Gaussian noise, iteratively denoise to generate new samples.

## References
1. Ho, J., Jain, A., & Abbeel, P. (2020). Denoising Diffusion Probabilistic Models. [arXiv:2006.11239](https://arxiv.org/abs/2006.11239)
2. [Outlier](https://www.youtube.com/@outliier). Diffusion Models | Paper Explanation | Math Explained. [Youtube](https://youtu.be/HoKDTa5jHvg?si=VVZqbMv-soDSaooo)
3. [Outlier](https://www.youtube.com/@outliier). Diffusion Models From Scratch | Score-Based Generative Models Explained | Math Explained. [Youtube](https://youtu.be/B4oHJpEJBAA?si=EjUQV8j6XvN4HGw1)
4. [DeepFindr](https://www.youtube.com/@DeepFindr). Diffusion models from scratch in PyTorch. [Youtube](https://www.youtube.com/watch?v=a4Yfz2FxXiY&t=178s)
