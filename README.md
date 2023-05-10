# Anime Face Generator using GANs
### Contributors: Timothy Colaneri, Borano Llana.
---

CSC561 Final Project: Anime Face Generator using GANs.

### Description
This project contains the implementation of a Deep Convolutional Generative Adversarial Network (DCGAN[^1]) model that aims to generate images of Anime character faces.

### Libraries used/other dependencies:
```python
!pip install datasets
!pip install torch
!pip install torchvision
!pip install numpy
!pip install matplotlib
```

### Dataset:
[Anime Face Dataset](https://huggingface.co/datasets/DrishtiSharma/Anime-Face-Dataset)

Load the dataset into your own workspace:
```python
from datasets import load_dataset
dataset = load_dataset("DrishtiSharma/Anime-Face-Dataset")
```

### Files:
*Source code*: `'main-colab.ipynb'`.<br>
*Generator model(trained)*: `'best_model_gen.pt'`.<br>
*Discriminator model(trained)*: '`best_model_dis.pt'`<br>

To load them into your workspace, you will need to copy the respective model architecture into your own code then load the pre-trained models like so:
```python
generator = torch.load("./best_model_gen.pt")
discriminator = torch.load("./best_model_dis.pt")
```
To have a gradio showcase of our generator model run in your machine: <br>
Add the notebook named `'trial.ipynb'` as well as the saved torch tensor `'best_model_gen.pt'` to the same directory and follow the instructions written within the notebook.

<br><br>
## References
[^1]: [DCGAN Tutorial.](https://pytorch.org/tutorials/beginner/dcgan_faces_tutorial.html)
