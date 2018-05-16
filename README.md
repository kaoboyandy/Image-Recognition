
# Image Recognition With VGG16

### This Github is an implementation of VGG16, a deep Convolutional Neural Network (CNN), using Keras framework. 

#### The implementation fitted 200 epochs with 1024 batch size and achieve a final validation accuracy of 92% in classifying various cat and dog photos 



This winning model of 2014 ImageNet Challenge investigate the effect of the convolutional network depth on its accuracy in the large-scale image recognition setting. The contributor, Karen Simonyan and Andrew Zisserman of the University of Oxford, thoroghly investigated networks of increasing depth using an architecture with very small (3×3) convolution filters, which shows that a significant improvement on the prior-art configurations can be achieved by pushing the depth to 16–19 weight layers.  

__[Original Paper: Very Deep Convolutional Networks for Large Scale Image Recognition](https://arxiv.org/pdf/1409.1556v6.pdf)__

<br>


![image.png](attachment:image.png)

<br>
<br>
## Main Points
<br>


- The use of only 3x3 sized filters is quite different from AlexNet’s 11x11 filters in the first layer and ZF Net’s 7x7 filters. The authors’ reasoning is that the combination of two 3x3 conv layers has an effective receptive field of 5x5. This in turn simulates a larger filter while keeping the benefits of smaller filter sizes. One of the benefits is a decrease in the number of parameters. Also, with two conv layers, we’re able to use two ReLU layers instead of one.


- 3 conv layers back to back have an effective receptive field of 7x7.


- As the spatial size of the input volumes at each layer decrease (result of the conv and pool layers), the depth of the volumes increase due to the increased number of filters as you go down the network.


- Interesting to notice that the number of filters doubles after each maxpool layer. This reinforces the idea of shrinking spatial dimensions, but growing depth.


- Worked well on both image classification and localization tasks. The authors used a form of localization as regression (see page 10 of the paper for all details).


- Built model with the Caffe toolbox.


- Used scale jittering as one data augmentation technique during training.


- Used ReLU layers after each conv layer and trained with batch gradient descent.


- Trained on 4 Nvidia Titan Black GPUs for two to three weeks. 



__[Credit for this amazing blog by Adit Deshpande](https://adeshpande3.github.io/adeshpande3.github.io/The-9-Deep-Learning-Papers-You-Need-To-Know-About.html)__

