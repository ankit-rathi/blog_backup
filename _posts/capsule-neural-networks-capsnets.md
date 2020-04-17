Title: Capsule Neural Networks (CapsNets)
Date: 2018-05-19 06:53
Author: ankitrathi
Category: Uncategorized
Tags: Machine Learning
Slug: capsule-neural-networks-capsnets
Status: published

![](http://ankitrathi.files.wordpress.com/2018/05/80f7f-1kehpvd7lrzoxadqsgpaugw.jpeg)

CNNs (convolutional neural networks) are one of the reasons deep learning is so popular today, they can do amazing things that people used to think computers would not be capable of doing for a long, long time. But they have their limits and some fundamental drawbacks and that is why Capsules neural networks are picking up pace, which introduce a new building block that can be used to overcome these limits & drawbacks of CNNs. Capsule networks (CapsNets) are a hot new neural net architecture that may well have a profound impact on deep learning, in particular for computer vision.

**What is Capsule Neural Networks?**

A Capsule Neural Network (CapsNet) is a machine learning system that is a type of artificial neural network (ANN) that can be used to better model hierarchical relationships. The approach is an attempt to more closely mimic biological neural organization. \~Wikipedia

A CapsNet is composed of capsules rather than neurons. A capsule is a small group of neurons that learns to detect a particular object within a given region of the image, and it outputs a vector whose length represents the estimated probability that the object is present, and whose orientation encodes the object’s pose parameters. If the object is changed slightly then the capsule will output a vector of the same length, but oriented slightly differently. Thus, capsules are equivariant.

**Why Capsule Neural Networks are required?**

Computer graphics deals with constructing a visual image from some internal hierarchical representation of geometric data, relationships between 3D objects can be represented by a so-called pose, which is in essence translation plus rotation. But how do we model these hierarchical relationships inside of a neural network? For a CNN, this task is really hard because it does not have this built-in understanding of 3D space, but there is type of neural network (CapsNet), for which it is much easier because these relationships are explicitly modeled.

CNNs perform exceptionally great when they are classifying images which are very close to the data set. If the images have rotation, tilt or any other different orientation then CNNs have poor performance. This problem was solved by adding different variations of the same image during training. Pooling layer helps in creating the positional invariance for CNN but what we needed was not invariance but equivariance. Equivariance makes CapsNet understand positional, orientational, proportional invariances. This leads us to the recent advancement of Capsule Networks.

**How Capsule Neural Networks work?**

![](http://ankitrathi.files.wordpress.com/2018/05/5e7d8-1h4cgbnhw5ai-mae5zas0xa.jpeg)

*Important differences between capsules and neurons. Source: author, inspired by the talk on CapsNets given by naturomics.*

A neuron receives input scalars from other neurons, then multiplies them by scalar weights and sums. This sum is then passed to one of the many possible nonlinear activation functions, that take the input scalar and output a scalar according to the function. That scalar will be the output of the neuron that will go as input to other neurons.

In essence, artificial neuron can be described by 3 steps:

1.  scalar weighting of input scalars
2.  sum of weighted input scalars
3.  scalar-to-scalar nonlinearity

while, the capsule has vector forms of the above 3 steps in addition to the new step, affine transform of input:

1.  matrix multiplication of input vectors
2.  scalar weighting of input vectors
3.  sum of weighted input vectors
4.  vector-to-vector nonlinearity

We see that the design of the capsule builds up upon the design of artificial neuron, but expands it to the vector form to allow for more powerful representational capabilities. It also introduces matrix weights to encode important hierarchical relationships between features of different layers. The result succeeds to achieve the goal of the designer: neuronal activity equivariance with respect to changes in inputs and invariance in probabilities of feature detection.

**References**

[Understanding Hinton’s Capsule Networks. Part I: Intuition.](https://medium.com/ai%C2%B3-theory-practice-business/understanding-hintons-capsule-networks-part-i-intuition-b4b559d1159b)

[Introducing Capsule Networks](https://www.oreilly.com/ideas/introducing-capsule-networks)

[Understanding Hinton’s Capsule Networks. Part II: How Capsules Work.](https://medium.com/ai%C2%B3-theory-practice-business/understanding-hintons-capsule-networks-part-ii-how-capsules-work-153b6ade9f66)

------------------------------------------------------------------------

*Thank you for reading my post. I regularly write about Data & Technology on* [*LinkedIn*](https://www.linkedin.com/today/posts/ankitrathi) *&* [*Medium*](https://medium.com/@rathi.ankit)*. If you would like to read my future posts then simply ‘Connect’ or ‘Follow’. Also feel free to connect on* [*Slideshare*](https://www.slideshare.net/ankitrathi)*.*
