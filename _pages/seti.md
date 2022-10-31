---
title: "Shuoyuan Wang - SETI competition record "
layout: gridlay
excerpt: "Shuoyuan Wang -- SETI competition record"
sitemap: false
permalink: /seti/
---

### A brief record of SETI


<center>
<figure>
		<div id="projectid">
    <img src="{{ site.url }}{{ site.baseurl }}/images/explore/SETI_competition.jpg" width="700px" />
		</div>

<figcaption>
<br>
<a href="https://www.kaggle.com/c/seti-breakthrough-listen">SETI Competition Homepage</a> 

</figcaption>
</figure>
</center>

#### input/output
- Input: image contain 6 channels, 3 contain detection signal, 3 contain background noise.
- Positive:Negative = 95%:5%
- Output: the possibility that whather the image contains anomalous signal, 0~1.
- Evaluation criteria: AUC of ROC

#### Baseline model
- efficientnet_b0_ns; batchsize = 128; optimizer = Adamw; LR = 1e-3; epoch = 20; 5folds; resolution = 320x320
- mixup = 0.1
- performance: local = 83.9, score = 73.0

#### Effective tricks(in competition test set)
##### Data Augmentation
- Remove rotation in data augmentation(+0.5%) 
- Image resolution: 320(base) --> 512(2%) --><strong>832(3%)</strong> --> 1024(3.1%)
- 819x256(bad), <strong>832x832</strong>(good)
- mixup = {0.1， 0.2， 0.5， 1， 2， 5， 10}, <strong>2</strong> Perform best(+0.2%)

##### Model Structure
- MLP layers for classification:search: layer{1, 2, 3}, meurons{128, 256, 512, 1024}, larger MLP only slight boost, it is unnecessary. We choose <strong>1 layer</strong>.
- dropout{0，0.2， 0.5， 0.8}, we mix 0 and 0.5
- bigger model: <strong>efficientnetv2_m(+0.5%)</strong>

##### Batch Size&Epoch
- batchsize:128 -><strong>192(+0.4%)</strong>, better mixup?
- epoch:20 -> 60(+0.1%)

##### Learning Rate Search
- Grid search in: optimizer{sgd, adam, adamw}; Learning Rate{3e-2, 1e-2 ... 3e-6, 1e-6},;decay{onecycle, cosine}, we use <strong>adamw, onecycle, 1.75e-3</strong>

##### Reuse Old Data
- Positive:Negative = 80%:20%<strong>(+0.2%)</strong>

##### Pseudo Labelling
- Use prediction of model as labels and train the network again in testset<strong>(+0.5%)</strong>. why pseudo labelling can work in most kaggle competition?

##### Ensemble Learning
- Use efficiennetb0, b4, tf_efficientnet_v2m<strong>(+0.2%)</strong>


#### Invalid tricks(in competition test set)
- focal loss and label smooth
- cutout
- transformer, densenet,regnet, skresnet, dsan

### Result:14/768(Top 2%)

#### Worth thinking about
- why why pseudo labelling can work in most kaggle competition?<br> 
 A: The model has never seen the real test set
- We should select different data augmentation according to data set distribution.
- After the competition, we find it necessary to <strong>only mixup the negative</strong>
- Few-Shot Learning is more in line with the thinking process of human brain.

#### Magic in other outstanding groups
- Only test set have the signal like "s", it is useful to adds those signals(p = 0.01) to the training set
- The background between train and test data is very different. Cleaning the data can bring big boosts of LB.
- Under the above conditions, only 4xTTA（regular、hflip、vflip、hflip+vflip, we use 12xTTA.
- The mixup uses logical OR instead of alpha blending when mixing targets. This allows creating a model that responds strongly to weak signals.
- Using only the high reliable pseudo-labels to find the difference between training and testing in this competition.
- An emsemble of four EfficientNets(b1,b2,b3,b4) with Convolutional Triplet Attention Module is work.
- GeM Pooling (p=4)

#### Acknowledgements
- Thank to my friend Haiyang, Liu from UTokyo for the discussion and help in the competition.