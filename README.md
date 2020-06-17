# SemanticSegmentation
This network was trained on the cityscapes dataset for autonomous vehicles. It achieves a pixel level accuracy, and is able to classify incoming images into over 30 different classes useful for self driving vehices. The output of the network can be seen below.

![](/Images/Results_Validation.png)
Results On Validation Set

![](/Images/Results_Generic.png)

Results On Generic Image

The complete list of relevant classes is detailed [here](https://github.com/mcordts/cityscapesScripts/blob/master/cityscapesscripts/helpers/labels.py).

The network architecture for semantic segmentation can be seen below, and involves a downsampling and upsampling phase. Google's [mobilenetV2](https://arxiv.org/abs/1801.04381) was leveraged for the encoding aspect of this network, while the decoding makes use of [pix2pix](https://phillipi.github.io/pix2pix/). 
![](/Images/NetworkOverview.png)

Mobilenet was selected for the encoding as it has accurate feature extraction while being very lightweight. This makes it an excellent choice for mobile devices, but was chosen for this project as the end goal for this was always to be deployed on a peripheral device of an autonomous vehicle.
