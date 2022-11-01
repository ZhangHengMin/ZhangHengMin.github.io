---
title: "Hengmin Zhang - GUI for HAR"
layout: gridlay
excerpt: "Hengmin Zhang -- GUI for HAR"
sitemap: false
permalink: /gui/
---


### Project

-  **Principal Investigator (PI)** for the National Science Young Fund of China, 
Title: Nonconvex Low-rank Structure Learning Method and Theory (Grant 61906067),  01/2020–12/2022

-  **Principal Investigator (PI)** for the China Postdoctoral Science Special Foundation, 
Title: Large-scale Robust Regression Analysis Method and Theory (Grant 2020T130191), 08/2020–03/2021

-  **Principal Investigator (PI)** for the China Postdoctoral Science Foundation,
Title: Robust Regression Analysis Method and Algorithm (Grant 2019M651415),  05/2019–03/2021

-  **Principal Investigator (PI)** for the Jiangsu Province Graduate Student Training and Innovation,
Title: Modeling and Optimization Algorithms for Low-rank Matrix Recovery Problems (Grant KYCX17_0359), 05/2017-2018.05

-  **Co-Principal Investigator (Co-PI)** for the National Science Fund of China,
Title: Power System Intrusion-tolerant Control and Mimic Defense for General False Data Injection Attacks
(Grant 62073138), 01/2021–12/2024

-  **Co-Principal Investigator (Co-PI)** for the National Science Fund of China,
Title: Robust Matrix Regression Method and Its Application for Image Classification (Grant 61876083),  01/2019–12/2022

-  **Co-Principal Investigator (Co-PI)** for the National Science Young Fund of China,
Title: Interactive Machine Teaching and Machine Learning Algorithms (Grant 61602246),  01/2017–12/2019

### Awards （NA）

-  **Memory Bank**: A non-local bank operator is used to attentively relate the past to the present. The memory bank is consisting of Resnet50 and LSTM network for the storage of long-term characteristics. It needs to be train in advance. The sequence length is optional. In my perspectives, the whole architecture is not end-to-end since the trained memory bank can be a reference in the training of backbone and do not need to calculate gradients and do backpropagation. Hence, it can great save computational cost.
- **Temporal variation layer**: Tolerating the varieties in temporal extent is essential. The temporal variation module(Multi-scale CNNs) is introduced to capture features in different temporal scales. It is worth noticed that the different temporal features are stacked along channel dimension and conclude the layer by a max-pooling layer for channel reduction. Hence, the output can have the same shape with the module input.
- **Non-local Bank Operator**: To effectively leverage long-range and multi-scale past information, a unified temporal memory relation network is introduced to achieve it. All the preceding features are considered with the current time step, hence, the current feature can be augmented. Also, the linear operation avoids too heavy regularization with similarity matrix directly performed on the input signal. It seems take the inspiration of <a href=" http://proceedings.mlr.press/v70/dauphin17a"> GLU </a> in this module which is good at long-term modeling.
