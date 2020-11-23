## Table of Contents
1. [Introduction](#introduction)
2. [Events and Groups](#events-and-groups) 📆
3. [Videos](#videos) :film_strip:
4. [Demos](#demos) :test_tube:
5. [Literature](#literature)  :blue_book: :page_facing_up:

### Introduction

Artificial Intelligence (AI) or Machine Learning (ML) is widely used today because it achieves much better results than humans can in many domains. The technology is based on a learning process in which an algorithm is trained with large amounts of data. This yields to a generalized model that should interpret unseen data. For example, a model's task could be to classify a traffic sign. ML is increasingly used in critical areas where errors can have serious consequences, such as a self-driving car that classifies a stop sign as a speed limit sign. This raises the question how secure such systems are.

An AI is often trained and evaluated with data that originates from controlled environments. In practice, however, this assumption is not given in many domains. Research has already shown practical attacks against AI systems and thus proven fundamental security problems.



### Events and Groups

### Videos

### Demos

With [adversarial.js](https://kennysong.github.io/adversarial.js/) one can create adversarial examples to attack neural networks within a browser.

### Literature

*Intriguing properties of neural networks*. [Szegedy et al. (2013)](https://research.google/pubs/pub42503/) discovered that deep neural networks, trained on an image classification task, are susceptible to adversarial examples. Minor manipulations of an image that are imperceptible to the naked eye can cause a neural network to output arbitrary classifications. Moreover, they found that adversarial examples are transferable between neural networks, that is, even neural networks with different parametrizations and training sets can be susceptible to the same adversarial examples. The authors of this work coined the term *adversarial examples* to describe input data perturbed with adversarial intent and performed experiments on crafting adversarial examples in the domain of image classification. The results indicate that the internal operation of neural networks behaves very sensitive to apparently insignificant changes to an input's semantic leading to an unexpected output.

*Adversarial patch*. [Brown et al. (2017)](https://arxiv.org/abs/1712.09665) defined a *patch application operator* which is a method to craft adversarial patches that attract the attention of neural networks and cause them to classify images as the target class. The operator randomly applies different transformations to an adversarial patch (e.g., changing rotation and size), and then places the result to several locations in different images. The process is iterated to find the parameters for which the target class has the highest probability. The determined adversarial patches cause the desired classification independently from factors such as image background, illumination, and viewing angle. Also, they work for different types of classifiers. The authors hypothesize that adversarial patches exploit the fact that models have to handle images that depict more than one item in the domain of object recognition, and consequently models are forced to decide on which of the items is the main focus. As adversarial patches attract the attention of neural networks, they even work in presence of other items. Due to this properties, the authors assume that adversarial patches are universal perturbations. Because adversarial examples modify original images by adding imperceptible, pixel-based perturbations, defenses that address the vulnerability to adversarial examples provide no sufficient protection against adversarial patches.
