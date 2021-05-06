# Simple image classification
Image classification on self-made dataset using pretrained networks.

### Installation
Before running the notebooks, install pytorch for CPU. How to do that can be found at [the official website](https://pytorch.org/). At the time of writing this,
it is sufficient to execute

```
pip3 install torch==1.8.1+cpu torchvision==0.9.1+cpu torchaudio==0.8.1 -f https://download.pytorch.org/whl/torch_stable.html
```
It is assumed that the reader is familiar with (and has installed) Jupyter notebooks. The projects also makes use of matplotlib library.

### Dataset
The dataset is self-made (that is, self-collected). It consists of 5 classes of desserts, each of the classes has 32 examples. For practical reasons, only
resized images are in the repository. However, the raw data is available [here](https://1drv.ms/u/s!AiQ5a2cXVytToEkoMe9Pshk2WSoG?e=HJ0LTb). I do not
claim the ownership on any of the pictures.

### Resources
- Pytorch finetuning / feature extraction [tutorial](https://pytorch.org/tutorials/beginner/finetuning_torchvision_models_tutorial.html)
