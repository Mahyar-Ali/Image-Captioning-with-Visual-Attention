## Image-Captioning-with-Visual-Attention
An Image Captioning Model with Visual attention that is capable of generating captions from Images.The model
is inspired from the from the original paper on ["Image Captioning Model with Visual attention"](https://arxiv.org/pdf/1502.03044.pdf).
The dataset is obtained from the famous [MS-COCO](http://cocodataset.org/#home) dataset for captioning.

### Libraries and Frameworks Used
- tensorflow
- matplotlib.pyplot
- sklearn.model_selection
- sklearn.utils

- numpy as np
- os
- time
- pickle

### About the Model
I trained the model on only first 30,000 training Images. The bottle-neck features extracted from the last layer of 
the ResNet model requires about 15GB of RAM. So I pickled the features and stored them in Hard Disk. The dataset is divided
into batches of size 64. One epoch take abut ~500 seconds on a Tesla K80 GPU of about 12GB RAM. I trained it for about 32
epochs and it took about ~5hours to train + 1hou to download,preprocess and pickle the dataset. So you can see that this
model can easily be further trained to increase the performance.

### Some Results
-------------------------------------------------------------------------------------
<img src="https://github.com/Mahyar-Ali/Image-Captioning-with-Visual-Attention/blob/master/images/NUST.jpeg?raw=true" alt="drawing" width="500"/>

predicted caption: a wooded area in the middle of the street with a bench near a sidewalk

</br>

---------------------------------------------------------------------------------------
<img src="https://github.com/Mahyar-Ali/Image-Captioning-with-Visual-Attention/blob/master/images/bus_street.jpg" alt="drawing" width="500"/>

predicted caption-1: a bus is in the street near a building

predicted caption-2: a bus parked in a city street 

</br>

---------------------------------------------------------------------------------------
<img src="https://github.com/Mahyar-Ali/Image-Captioning-with-Visual-Attention/blob/master/images/islamabad.jpeg?raw=true" alt="drawing" width="500"/>

predicted caption : the building in front of the hills


