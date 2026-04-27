# Generative-Adversarial-Networks

A learning repository exploring different flavors of Generative Adversarial Networks (GANs) across images, audio, and text-to-image generation. Each subproject is a self-contained Jupyter notebook (designed to run on Google Colab) that trains a GAN on a particular dataset / task.

## What's a GAN?

A GAN pits two neural networks against each other: a **generator** that fabricates samples and a **discriminator** that tries to tell fake samples from real ones. Trained together in a zero-sum game, the generator learns to produce outputs that are increasingly hard to distinguish from real data.

## Tech stack

- Python 3
- TensorFlow / Keras
- Jupyter notebooks (run on Google Colab; some load data from Google Drive)
- [Magenta](https://magenta.tensorflow.org/) for the music GAN experiment

## Repository layout

```
Image GANs/
  Fashion GAN/             # GAN trained on Fashion-MNIST (Keras)
  Handwritten Digits GAN/  # GAN trained on MNIST handwritten digits
  Cartoon Images GAN/      # Face/cartoon image GAN; includes a trained
                           # generator (face_generator_100.h5) and sample outputs
Music GANs/
  GANSynth/                # Music generation with Magenta's GANSynth,
                           # plus a sample remix mp3
Style GANs/
  links.txt                # Reference links (StyleGAN2, style transfer notebooks)
Text to Image/
  read.txt                 # Reference links (DALL-E, text-to-art articles)
```

The `Style GANs` and `Text to Image` folders are reference / link collections rather than runnable code.

## How to run

The notebooks are written for Google Colab:

1. Open any `.ipynb` file in Google Colab.
2. If the notebook mounts Google Drive (`from google.colab import drive`), authorize access when prompted.
3. Enable a GPU runtime (Runtime -> Change runtime type -> GPU) for reasonable training times.
4. Run the cells top to bottom.

To run locally instead, install the dependencies (TensorFlow / Keras, NumPy, Matplotlib, tqdm, and Magenta for the music notebook) and launch Jupyter.

## Notes

This is a learning repo — code is exploratory and notebook-first, not packaged as a library.
