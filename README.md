
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

# The effect of zero-padding in a convolution
So far here, we’ve used zero-padding in convolutions to compute finite-sized output vectors. Technically, padding can be applied with any p > 0 . Depending on the choice p, boundary cells may be treated differently than the cells located in the middle of x. Now consider an example where n = 5, m = 3. Then, p = 0, x[0] is only used in computing one output element (for instance, y[0]), while x[1] is used in the computation of two output elements (for instance, y[0] and y[1]). So, you can see that this different treatment of elements of x can artificially put more emphasis on the middle element, x[2], since it has appeared in most computations. We can avoid this issue if we choose p = 2, in which case, each element of x will be involved in computing three elements of y. Furthermore, the size of the output y also depends on the choice of the padding strategy we use. There are three modes of padding that are commonly used in practice: full, same, and valid:
In the full mode, the padding parameter p is set to p = m — 1. Full padding increases the dimensions of the output; thus, it is rarely used in convolutional neural network architectures.
• Same padding is usually used if you want to have the size of the output the same as the input vector x. In this case, the padding parameter p is computed according to the filter size, along with the requirement that the input size and output size are the same.
• Finally, computing a convolution in the valid mode refers to the case where p = 0 (no padding).
The following figure illustrates the three different padding modes for a simple 5 x 5 pixel input with a kernel size of 3 x 3 and a stride of 1:

![image](https://user-images.githubusercontent.com/53411455/147838458-8326a4a4-2d4d-4830-85cb-7bd66146973d.png)

# Details about this project

The python code can be found this repository  as Untitled.iypnb and more details acout CNN can be found in the following blog : https://marushka.medium.com/deep-convolutional-neural-networks-4d20ac33de3c

