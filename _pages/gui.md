---
title: "Hengmin Zhang - GUI for HAR"
layout: gridlay
excerpt: "Hengmin Zhang -- GUI for HAR"
sitemap: false
permalink: /gui/
---


### 1. Project

#### 1.1 Why Not End-to-End？
-  Refinement stage uses the output of predictor stage as input, so the performance of prediction is very important. Although you can achieve low error rate on trainset, which can be refined for better performance, base model will certainly make mistakes on the testset and make no sense to refinement (refining the error cannot boost performance.
- If we use the end-to-end strategy, the limited size of current datasets for surgery phase recognition cannot afford the refinement stage with additional parameters, which leads to overfitting on testset.


#### 1.2 Aims and Solutions
To simulate the real output of the predictor by generating two disturbed sequences. 
- Mask-Hard-Frame: Using their former techniques to find hard frames in trainset, which are not recognizable from their visual appearance, and cover the hard frames via a black mask. As is shown in Figure.1, frame-wise methods may perform poorly.
- Cross-Validate: Through Cross Validate, the valset can play the role of testset, the output can be simulated as the real predictions of the predictor.



### 2. Awards

#### 2.2 Why ？
-  Complicated surgical scenes lead to limited inter-phase variance but high intra-phase variance. So, it is necessary to capture the long-range temporal dynamics. However, due to the limits of GPU memory, joint architectures like DeepConvLSTM or 3D CNNs only can collect information from a short-term view with 10s duration at most. Watching only short-term cues is not sufficient to achieve accurate recognition.

#### 2.2 Aims and Solutions
it is crucial to simultaneously take both advantages of end-to-end learning and long-range temporal information in the medical scenarios. The paper introduces an end-to-end architecture to observe long-range temporal dependency and capture complex multi-scale temporal pattern.
-  **Memory Bank**: A non-local bank operator is used to attentively relate the past to the present. The memory bank is consisting of Resnet50 and LSTM network for the storage of long-term characteristics. It needs to be train in advance. The sequence length is optional. In my perspectives, the whole architecture is not end-to-end since the trained memory bank can be a reference in the training of backbone and do not need to calculate gradients and do backpropagation. Hence, it can great save computational cost.
- **Temporal variation layer**: Tolerating the varieties in temporal extent is essential. The temporal variation module(Multi-scale CNNs) is introduced to capture features in different temporal scales. It is worth noticed that the different temporal features are stacked along channel dimension and conclude the layer by a max-pooling layer for channel reduction. Hence, the output can have the same shape with the module input.
- **Non-local Bank Operator**: To effectively leverage long-range and multi-scale past information, a unified temporal memory relation network is introduced to achieve it. All the preceding features are considered with the current time step, hence, the current feature can be augmented. Also, the linear operation avoids too heavy regularization with similarity matrix directly performed on the input signal. It seems take the inspiration of <a href=" http://proceedings.mlr.press/v70/dauphin17a"> GLU </a> in this module which is good at long-term modeling.
