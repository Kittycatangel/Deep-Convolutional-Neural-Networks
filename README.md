
# Deep-Convolutional-Neural-Networks

# Introduction
Convolutional neural networks, or CNNs, are a family of models that were inspired by how the visual cortex of the human brain works when recognizing objects. The development of CNNs goes back to the 1990s when Yann LeCun and his colleagues proposed novel neural network architecture for classifying handwritten digits from images (Handwritten Digit Recognition with a Back-Propagation Network, Y LeCun, and others, 1989, published at Neural Information Processing Systems. (NIPS)conference). Due to the outstanding performance of CNNs for image classification tasks, they have gained a lot of attention and this led to tremendous improvements in machine learning and computer vision applications.

As you can see in the following image, a CNN computes feature maps from an input image, where each element comes from a local patch of pixels in the input image:

![image](https://user-images.githubusercontent.com/53411455/147838397-ddafd62c-b34c-4f13-ae55-9eecaf7dc449.png)

# Performing discrete convolutions
A discrete convolution (or simply convolution) is a fundamental operation in a CNN. Therefore, it’s important to understand how this operation works.

![image](https://user-images.githubusercontent.com/53411455/147838417-5adce72b-d407-4bd1-b49c-f9ca0b152b27.png)

# Cross-correlation
Cross-correlation (or simply correlation) between an input vector and a filter is denoted by y = x w and is very much like a sibling for convolution with a small difference; the difference is that in cross-correlation, the multiplication is performed in the same direction. Therefore, it is not required to rotate the filter matrix w in each dimension. Mathematically, cross-correlation is defined as follows:
![image](https://user-images.githubusercontent.com/53411455/147838440-10198aae-ab7b-4743-9a93-73706ef8ee74.png)
