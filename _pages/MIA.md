---
title: "Hengmin Zhang - MIA"
layout: gridlay
excerpt: "Hengmin Zhang -- MIA"
sitemap: false
permalink: /MIA/
---

### 1. Group （NA）

-  **Memory Bank**: A non-local bank operator is used to attentively relate the past to the present. The memory bank is consisting of Resnet50 and LSTM network for the storage of long-term characteristics. It needs to be train in advance. The sequence length is optional. In my perspectives, the whole architecture is not end-to-end since the trained memory bank can be a reference in the training of backbone and do not need to calculate gradients and do backpropagation. Hence, it can great save computational cost.
- **Temporal variation layer**: Tolerating the varieties in temporal extent is essential. The temporal variation module(Multi-scale CNNs) is introduced to capture features in different temporal scales. It is worth noticed that the different temporal features are stacked along channel dimension and conclude the layer by a max-pooling layer for channel reduction. Hence, the output can have the same shape with the module input.
- **Non-local Bank Operator**: To effectively leverage long-range and multi-scale past information, a unified temporal memory relation network is introduced to achieve it. All the preceding features are considered with the current time step, hence, the current feature can be augmented. Also, the linear operation avoids too heavy regularization with similarity matrix directly performed on the input signal. It seems take the inspiration of <a href=" http://proceedings.mlr.press/v70/dauphin17a"> GLU </a> in this module which is good at long-term modeling.



### 2. Research

-  **Memory Bank**: A non-local bank operator is used to attentively relate the past to the present. The memory bank is consisting of Resnet50 and LSTM network for the storage of long-term characteristics. It needs to be train in advance. The sequence length is optional. In my perspectives, the whole architecture is not end-to-end since the trained memory bank can be a reference in the training of backbone and do not need to calculate gradients and do backpropagation. Hence, it can great save computational cost.
- **Temporal variation layer**: Tolerating the varieties in temporal extent is essential. The temporal variation module(Multi-scale CNNs) is introduced to capture features in different temporal scales. It is worth noticed that the different temporal features are stacked along channel dimension and conclude the layer by a max-pooling layer for channel reduction. Hence, the output can have the same shape with the module input.
- **Non-local Bank Operator**: To effectively leverage long-range and multi-scale past information, a unified temporal memory relation network is introduced to achieve it. All the preceding features are considered with the current time step, hence, the current feature can be augmented. Also, the linear operation avoids too heavy regularization with similarity matrix directly performed on the input signal. It seems take the inspiration of <a href=" http://proceedings.mlr.press/v70/dauphin17a"> GLU </a> in this module which is good at long-term modeling.
