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
The dataset is self-made (that is, self-collected). It consists of 5 classes of desserts, each of the classes has 31 examples. The desserts are:
apple pie, babovka, cheesecake, maulwurfkuchen and muffin. I've decided to do dessert classification, as it didn't seem too hard (it is not that hard
to tell cheesecake from muffin) but also not trivial. To see that that's the case I encourage the reader to look into the the data preprocessing notebook
to see what the data looks like, ideally also look into the data directory itself.

For practical reasons, only resized images are in the repository. However, the raw data is available
[here](https://1drv.ms/u/s!AiQ5a2cXVytToEkoMe9Pshk2WSoG?e=HJ0LTb). All images are resized to 224x224 as a part of preprocessing - the reason for that is
that all of the pretrained models were trained on images of that size. 

I do not claim the ownership on any of the pictures.

### Memory requirements
In the main notebook all the pretrained networks are used at once, leading to potential RAM usage of several GB. If the user cannot afford to spend
that much RAM at once, he / she can comment out all but one entry in `model_names` list variable - this will make the application only use that one
particular model.

### Time requirements
Keep in mind that the training of all models (as specified in the notebook) takes tens of minutes on CPU (would be faster on GPU; if the user is
capable of installing PyTorch for GPU, he might prefer to do that, as it would severy reduce the training time).

### Resources
- Pytorch finetuning / feature extraction [tutorial](https://pytorch.org/tutorials/beginner/finetuning_torchvision_models_tutorial.html)
