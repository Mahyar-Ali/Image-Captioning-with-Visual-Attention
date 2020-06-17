## Image-Captioning-with-Visual-Attention
An Image Captioning Model with Visual attention that is capable of generating captions from Images.The model
is inspired from the from the original paper on ["Image Captioning Model with Visual attention"](https://arxiv.org/pdf/1502.03044.pdf).
The dataset is obtained from the famous [MS-COCO](http://cocodataset.org/#home) dataset for captioning.

### About the Model
I trained the model on only first 30,000 training Images. The bottle-neck features extracted from the last layer of 
the ResNet model requires about 15GB of RAM. So I pickled the features and stored them in Hard Disk. The dataset is divided
into batches of size 64. One epoch take abut ~500 seconds on a Tesla K80 GPU of about 12GB RAM. I trained it for about 32
epochs and it took about ~5hours to train + 1hou to download,preprocess and pickle the dataset. So you can see that this
model can easily be further trained to increase the performance.

### Some Results
