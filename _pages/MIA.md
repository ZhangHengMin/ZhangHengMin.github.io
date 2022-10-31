---
title: "Hengmin Zhang - MIA"
layout: gridlay
excerpt: "Hengmin Zhang -- MIA"
sitemap: false
permalink: /MIA/
---

### 1. Not End-to-End: Explore Multi-Stage Architecture for Online Surgical Phase Recognition. <a href="https://arxiv.org/abs/2107.04810">paper link</a>

#### 1.1 Why Not End-to-End？
-  Refinement stage uses the output of predictor stage as input, so the performance of prediction is very important. Although you can achieve low error rate on trainset, which can be refined for better performance, base model will certainly make mistakes on the testset and make no sense to refinement (refining the error cannot boost performance.
- If we use the end-to-end strategy, the limited size of current datasets for surgery phase recognition cannot afford the refinement stage with additional parameters, which leads to overfitting on testset.


#### 1.2 Aims and Solutions
To simulate the real output of the predictor by generating two disturbed sequences. 
- Mask-Hard-Frame: Using their former techniques to find hard frames in trainset, which are not recognizable from their visual appearance, and cover the hard frames via a black mask. As is shown in Figure.1, frame-wise methods may perform poorly.
- Cross-Validate: Through Cross Validate, the valset can play the role of testset, the output can be simulated as the real predictions of the predictor.

<center>
<figure>
		<div id="projectid">
    <img src="{{ site.url }}{{ site.baseurl }}/images/explore/MIA/1.png" width="600px" />
		</div>

<figcaption>
<br>
hard frame in visual appearance

</figcaption>
</figure>
</center>

#### 1.3 Experiment Reproduction
I both use their pretrained model and local trained model. The performance of local based model and refinement model may be higher than they report in manuscript. I use their provided video feature, which downsampled 25 fps to 5 fps. The training process work on the server (GPU: 24GB GeForce RTX 3090x4; CPU: 6thGen Intel i7-6850K; RAM: 64 GB).

<center>
<figure>
		<div id="projectid">
    <img src="{{ site.url }}{{ site.baseurl }}/images/explore/MIA/NETE.png" width="750px" />
		</div>

<figcaption>
<br>
Result on cholec80

</figcaption>
</figure>
</center>

### 2. Temporal Memory Relation Network forWorkflow Recognition from Surgical Video Recognition. <a href="https://arxiv.org/pdf/2103.16327.pdf">paper link</a>

#### 2.2 Why ？
-  Complicated surgical scenes lead to limited inter-phase variance but high intra-phase variance. So, it is necessary to capture the long-range temporal dynamics. However, due to the limits of GPU memory, joint architectures like DeepConvLSTM or 3D CNNs only can collect information from a short-term view with 10s duration at most. Watching only short-term cues is not sufficient to achieve accurate recognition.

#### 2.2 Aims and Solutions
it is crucial to simultaneously take both advantages of end-to-end learning and long-range temporal information in the medical scenarios. The paper introduces an end-to-end architecture to observe long-range temporal dependency and capture complex multi-scale temporal pattern.
-  **Memory Bank**: A non-local bank operator is used to attentively relate the past to the present. The memory bank is consisting of Resnet50 and LSTM network for the storage of long-term characteristics. It needs to be train in advance. The sequence length is optional. In my perspectives, the whole architecture is not end-to-end since the trained memory bank can be a reference in the training of backbone and do not need to calculate gradients and do backpropagation. Hence, it can great save computational cost.
- **Temporal variation layer**: Tolerating the varieties in temporal extent is essential. The temporal variation module(Multi-scale CNNs) is introduced to capture features in different temporal scales. It is worth noticed that the different temporal features are stacked along channel dimension and conclude the layer by a max-pooling layer for channel reduction. Hence, the output can have the same shape with the module input.
- **Non-local Bank Operator**: To effectively leverage long-range and multi-scale past information, a unified temporal memory relation network is introduced to achieve it. All the preceding features are considered with the current time step, hence, the current feature can be augmented. Also, the linear operation avoids too heavy regularization with similarity matrix directly performed on the input signal. It seems take the inspiration of <a href=" http://proceedings.mlr.press/v70/dauphin17a"> GLU </a> in this module which is good at long-term modeling.

#### 2.3 Experiment Reproduction
Experiment Reproduction is time consuming, I first set the sequence length = 10 both in training memory bank and backbone. The result is similar with their report in the paper. Given the sequence length = 10, each epoch will take up 30min. I am try to reproduce their best result. The sequence length should be 40 in terms of cholec80 dataset. Each epoch will take up 2h25min in the training of memory bank. The training process work on the server (GPU: 24GB GeForce RTX 3090x4; CPU: 6thGen Intel i7-6850K; RAM: 64 GB).

<center>
<figure>
		<div id="projectid">
    <img src="{{ site.url }}{{ site.baseurl }}/images/explore/MIA/TMR_result.png" width="750px" />
		</div>

<figcaption>
<br>
TMRNet Result on cholec80

</figcaption>
</figure>
</center>