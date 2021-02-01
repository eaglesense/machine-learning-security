## Machine Learning Security

Artificial Intelligence (AI) or Machine Learning (ML) is widely used today because it achieves much better results than humans can in many domains. The technology is based on a learning process in which an algorithm is trained with large amounts of data. This yields to a generalized model that should interpret unseen data. For example, a model's task could be to classify a traffic sign. ML is increasingly used in critical areas where errors can have serious consequences, such as a self-driving car that classifies a stop sign as a speed limit sign. This raises the question how secure such systems are.

An AI is often trained and evaluated with data that originates from controlled environments. In practice, however, this assumption is not given in many domains. Research has already shown practical attacks against AI systems and thus proven fundamental security problems.

## Table of Contents
1. [Events](#events) 📆
2. [Groups](#groups) 🔬
3. [Libraries](#libraries) 📚
4. [Demos](#demos) 🧪
5. [Videos](#videos) 🎞️
6. [Literature](#literature) 📘 📄

### Events

[Workshop on Artificial Intelligence and Security (AISec)](https://aisec.cc/)

### Groups

The [Secure Systems Group](https://crysp.uwaterloo.ca/research/SSG/) at the University of Waterloo (formerly resident at the Aalto University) researches in the field of machine learning and security/privacy as well as model extraction attacks and defenses.

The [Pattern Recognition and Applications Lab (PRALab)](https://pralab.diee.unica.it/en/AdversarialMachineLearning) at the University of Cagliari researches in the field of Adversarial Machine Learning.

The [Berryville Institute of Machine Learning (BIML)](https://berryvilleiml.com/) elaborates a taxonomy of attack vectors on machine learning and works on a threat model. They also maintain a [bibliography](https://berryvilleiml.com/references/) that contains papers related to machine learning security.

### Libraries

| Name | ML Libraries | ML models | Attacks | Defenses | Noteworthy |
| --- |:---:|:---:|:---:|:---:|:---:|
| Adversarial Robustness Toolbox | Tensorflow (v1 and v2), Keras, PyTorch, Scikit-learn, XGBoost, LightGBM, CatBoost, GPy | DNN, (Gradient Boosted) Decision Trees, SVM, RF, Logistic Regression, Gaussian Processes, and more  | >= 17 attacks | _Model Hardening_: Adversarial Training, Feature Squeezing, Label Smoothing, Spatial Smoothing, JPEG Compression, Thermometer Encoding, Total Variance Minimization, Gaussian Data Augmentation, Pixel Defense; _Runtime Detection (Evasion)_: Binary Detector based on Inputs and Activations, Fast generalized subset scan based detector; _Runtime Detection (Poisoning)_: Poisoning Filter Using Activation Clustering Against Backdoor Attacks | Emprirical Robustness, Loss Sensitivity, CLEVER, Clique Method Robustness Verification for Decision Tree Ensembles
| secml     | A PyTorch wrapper (can be extended to use other ML frameworks) enables use of DNNs, Scikit-learn | DNN, SVM, RF | Training-time poisoning attacks, test-time evasion attacks | Integrates and extends many attacks from CleverHans | Explainability Visualization, feature-based and prototype-based explanation methods, integrated gradient for explanation |
| Foolbox | PyTorch, Keras, Tensorflow, Theano, Lasagne, MXNet | | >= 15 attacks| | _Adversarial criteria_: Targeted misclassification, top-k misclassification, distance measures |
| CleverHans | Tensorflow (v1) | | >= 10 attacks | adversarial training | |

| Name | Category |
| --- |:---:|
| [AdvBox](https://github.com/advboxes/AdvBox) | Adversarial Example Generation and Robustness Benchmark |
| [Perceptron Robustness Benchmark](https://github.com/advboxes/perceptron-benchmark) | Benchmark for (computer vision) DNNs |
| [AdversarialDNN-Playground](https://github.com/QData/AdversarialDNN-Playground) | Web-based Visualization for Adversarial ML |
| [advertorch](https://github.com/BorealisAI/advertorch) | Attack, Defense, Adversarial Training |
| [alibi-detect](https://github.com/SeldonIO/alibi-detect) | Outlier, Adversarial, and Drift Detection |
| [DEEPSEC](https://github.com/kleincup/DEEPSEC) | Security, Attack, and Defense Analysis |
| [EvadeML-Zoo](https://github.com/mzweilin/EvadeML-Zoo) | Benchmarking and Visualization |
| [MIA](https://github.com/spring-epfl/mia) | Membership Inference Attack |
| [Textfool](https://github.com/bogdan-kulynych/textfool) | Attack on Text Classification |
| [Outlier Exposure](https://github.com/hendrycks/outlier-exposure) | Outlier Detection |
| [PyOD](https://github.com/yzhao062/pyod) | Outlier Detection |
| [SUOD](https://github.com/yzhao062/SUOD) | Outlier Detection |

| Name | Category |
| --- |:---:|
| [PySyft](https://github.com/OpenMined/PySyft) | Private Deep Learning |
| [substra](https://github.com/SubstraFoundation/substra) | Private Deep Learning |
| [Tensorflow Privacy](https://github.com/tensorflow/privacy) | Differential Privacy in ML |
| [TF Encrypted](https://github.com/tf-encrypted/tf-encrypted) | Encrypted ML |

The [secml](https://arxiv.org/pdf/1912.10013.pdf) Python library is hosted [here](https://gitlab.com/secml/secml), and its documentation can be found [here](https://secml.gitlab.io/).

The [Adversarial Robustness Toolbox](https://arxiv.org/abs/1807.01069) is hosted [here](https://github.com/Trusted-AI/adversarial-robustness-toolbox).

The [CleverHans Adversarial Examples Library](https://arxiv.org/abs/1610.00768) is hosted [here](https://github.com/tensorflow/cleverhans), and is explained in detail on the [cleverhans blog](http://www.cleverhans.io/).

The [Foolbox](https://arxiv.org/abs/1707.04131) project is hosted [here](https://github.com/bethgelab/foolbox).

### Demos

With [adversarial.js](https://kennysong.github.io/adversarial.js/) one can create adversarial examples to attack neural networks within a browser.

[Secure ML Demo](https://www.pluribus-one.it/research/sec-ml/demo)

### Videos

### Literature

*Intriguing properties of neural networks*. [Szegedy et al. (2013)](https://research.google/pubs/pub42503/) discovered that deep neural networks, trained on an image classification task, are susceptible to adversarial examples. Minor manipulations of an image that are imperceptible to the naked eye can cause a neural network to output arbitrary classifications. Moreover, they found that adversarial examples are transferable between neural networks, that is, even neural networks with different parametrizations and training sets can be susceptible to the same adversarial examples. The authors of this work coined the term *adversarial examples* to describe input data perturbed with adversarial intent and performed experiments on crafting adversarial examples in the domain of image classification. The results indicate that the internal operation of neural networks behaves very sensitive to apparently insignificant changes to an input's semantic leading to an unexpected output.

*Adversarial patch*. [Brown et al. (2017)](https://arxiv.org/abs/1712.09665) defined a *patch application operator* which is a method to craft adversarial patches that attract the attention of neural networks and cause them to classify images as the target class. The operator randomly applies different transformations to an adversarial patch (e.g., changing rotation and size), and then places the result to several locations in different images. The process is iterated to find the parameters for which the target class has the highest probability. The determined adversarial patches cause the desired classification independently from factors such as image background, illumination, and viewing angle. Also, they work for different types of classifiers. The authors hypothesize that adversarial patches exploit the fact that models have to handle images that depict more than one item in the domain of object recognition, and consequently models are forced to decide on which of the items is the main focus. As adversarial patches attract the attention of neural networks, they even work in presence of other items. Due to this properties, the authors assume that adversarial patches are universal perturbations. Because adversarial examples modify original images by adding imperceptible, pixel-based perturbations, defenses that address the vulnerability to adversarial examples provide no sufficient protection against adversarial patches.
