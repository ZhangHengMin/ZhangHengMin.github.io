---
title: "Hengmin Zhang - Publications"
layout: gridlay
excerpt: "Hengmin Zhang -- Publications."
sitemap: false
permalink: /publications/
---

### **Book Chapter** 

- Yang J, Cui Z, Xu C, Qian J, Gong C, **Zhang H** and Jin Z. Artificial intelligence: Pattern Recognition. 
**Electronic Industry Press**, Aug. 2020. 

#

### **From 2021** 

- **Zhang H**, Qian F, Shi P, Du W, Tang Y, Qian J, Gong C and Yang J. Generalized Nonconvex Nonsmooth Low-rank Matrix Recovery Framework with Feasible Algorithm Designs and Convergence Analysis[J]. **IEEE Transactions on Neural Networks and Learning Systems**, DOI: 10.1109/TNNLS.2022.3183970.  

- **Zhang H**, Qian F, Zhang B, Du W, Qian J and Yang J. Incorporating Linear Regression Problems Into An Adaptive
Framework with Feasible Optimizations[J]. **IEEE Transactions on Multimedia**, DOI: 10.1109/TMM.2022. 3171088.  

- **Zhang H**, Qian F, Shang F, Du W, Qian J and Yang J. Global Convergence Guarantees of (A)GIST for a Family of
Noncovex Sparse Learning Problems[J]. **IEEE Transactions on Cybernetics**, 2022, 52(5): 3276-3288.  

-  Yu G, Ma L, Jin Y, Du W, Liu Q and **Zhang H**. A Survey on Knee-oriented Multi-objective Evolutionary
Optimization[J]. **IEEE Transactions on Evolutionary Computation**, DOI: 10.1109/TEVC.2022.3144880. 

- Qian J, Wong W, **Zhang H**, Xie J and Yang J. Joint Optimal Transport with Convex Regularization for Robust
Image Classification[J]. **IEEE Transactions on Cybernetics**, 2022, 52(3): 1553-1564. 

- **Zhang H**, Luo W, Du W, Qian J and Yang J. Robust Recovery of Low Rank Matrix by Nonconvex Rank
Regularization[C]. **International Conference on Image and Graphics (ICIG)**, 2021: 106-119.

-  Qian J, Zhu S, Wong W, **Zhang H**, Lai Z and Yang J. Dual Robust Regression for Pattern Classification[J].
**Information Sciences**, 2021, 546: 1014-1029.  

#

### **Before 2020**

-  **Zhang H**, Qian J, Zhang B, Yang J, Gong C and Wei Y. Low-Rank Matrix Recovery via Modified Schatten-p Norm
Minimization with Convergence Guarantees[J]. **IEEE Transactions on Image Processing**, 2020, 29(0), 3132-3142. 
 

- **Zhang H**, Du W, Li Z, Liu X, Long J and Qian F. Nonconvex Rank Relaxations based Matrix Regression for Face
Reconstruction and Recognition[C]. **China Automation Congress (CAC)**, 2020: 2335-2340.

- **Zhang H**, Du W, Liu X, Zhang B and Qian F. Factored Trace Lasso based Linear Regression Methods: Optimizations and Applications[C]. **International Conference on Cognitive Systems and Information Processing (ICCSIP)**, 2020, 121-130.

- Luo W, **Zhang H**, Li J, Wei X. Learning Semantically Enhanced Feature for Fine-Grained Image Classification[J].
**IEEE Signal Processing Letters**, 2020, 27: 1545-1549.  

-  **Zhang H**, Gong C, Qian J, Zhang B, Xu C and Yang J. Efficient Recovery of Low Rank Matrix via Double
Nonconvex Nonsmooth Rank Minimization[J]. **IEEE Transactions on Neural Networks and Learning Systems**, 2019,
30(10): 2916-2925.  

-  **Zhang H**, Qian J, Gao J, Yang J and Xu C. Scalable Proximal Jacobian Iteration Method with Global Convergence
Analysis for Nonconvex Unconstrained Composite Optimizations[J]. **IEEE Transactions on Neural Networks and
Learning Systems**, 2019, 30(9), 2825-2839.  

-  **Zhang H**, Yang J, Shang F, Gong C and Zhang Z. LRR for Subspace Segmentation via Tractable Schatten-p Norm
Minimization and Factorization[J]. **IEEE Transactions on Cybernetics**, 2019, 49(5): 1722-1734.
<a href=" https://github.com/ZhangHengMin/SpNM-SpNF-LRR.git"> [Code] </a>

-  **Zhang H**, Yang J and Zheng W. Research Progress of Low-Rank Matrix Approximation and Optimization
Problem[J]. **Pattern Recognition and Artificial Intelligence**, 2018, 31(1): 23-36. 

-  **Zhang H**, Yang J, Xie J, Qian J and Zhang B. Weighted Sparse Coding Regularized Nonconvex Matrix Regression
for Robust Face Recognition[J]. **Information Sciences**, 2017, 394: 1-17.  

-  **Zhang H**, Yang J, Qian J and Luo W. Nonconvex Relaxation based Matrix Regression for Face Recognition with
Structural Noise and Mixed Noise[J]. **Neurocomputing**, 2017, 269: 188-198.  

-  Gong C, **Zhang H**, Yang J and Tao D. Learning with Inadequate and Incorrect Supervision[C]. **IEEE International
Conference on Data Mining (ICDM)**, 2017: 889-894.

-  Xie J, Yang J, Qian J, Tai Y, and **Zhang H**. Robust Nuclear Norm based Matrix Regression with Applications to
Face Recognition[J]. **IEEE Transactions on Image Processing**, 2017, 26(5), 2286-2295.  

-  Chen Y, Yang J, Luo L, **Zhang H**, Qian J, Tai Y and Zhang J. Adaptive Noise Dictionary Construction via IRRPCA
for Face Recognition[J].  **Pattern Recognition**, 2016, 59: 26-41.  

-  **Zhang H**, Luo W, Yang J and Luo L. Locality-constrained Group Sparse Coding Regularized NMR for Robust
Face Recognition[C]. **IEEE Asian Conference on Pattern Recognition (ACPR)**, 2015: 740-744.

#

{% for publi in site.data.publist %}

<div class="col-sm-11 clearfix">
 <div class="well">
 <pubtit>{{ publi.title }}</pubtit>

 <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="200px" style="float: left" />

 <p>{{ publi.description }}</p>

 <p><em>{{ publi.authors }}</em></p>

 <p>{{ publi.venue }}</p>

 {% if publi.number_link == 1 %}
 <p><a href="{{ publi.link1.url }}">{{ publi.link1.display }}</a></p>
 {% endif %}

 {% if publi.number_link == 2 %}
 <p><a href="{{ publi.link1.url }}">{{ publi.link1.display }}</a>
 /
 <a href="{{ publi.link2.url }}">{{ publi.link2.display }}</a></p>
 {% endif %}

 {% if publi.number_link == 3 %}
 <p><a href="{{ publi.link1.url }}">{{ publi.link1.display }}</a>
 /
 <a href="{{ publi.link2.url }}">{{ publi.link2.display }}</a>
 /
 <a href="{{ publi.link3.url }}">{{ publi.link3.display }}</a></p>
 {% endif %}

 {% if publi.number_link == 4 %}
 <p><a href="{{ publi.link1.url }}">{{ publi.link1.display }}</a>
 /
 <a href="{{ publi.link2.url }}">{{ publi.link2.display }}</a>
 /
 <a href="{{ publi.link3.url }}">{{ publi.link3.display }}</a>
 /
 <a href="{{ publi.link4.url }}">{{ publi.link4.display }}</a></p>
 {% endif %}

 {% if publi.number_link == 5 %}
 <p><a href="{{ publi.link1.url }}">{{ publi.link1.display }}</a>
 /
 <a href="{{ publi.link2.url }}">{{ publi.link2.display }}</a>
 /
 <a href="{{ publi.link3.url }}">{{ publi.link3.display }}</a>
 /
 <a href="{{ publi.link4.url }}">{{ publi.link4.display }}</a>
 /
 <a href="{{ publi.link5.url }}">{{ publi.link5.display }}</a></p>
 {% endif %}

 </div>
</div>

{% endfor %}

<p> &nbsp; </p>


 

{% for publi in site.data.theseslist limit:6 %}

<div class="col-sm-11 clearfix">
 <div class="well">
 <pubtit>{{ publi.title }}</pubtit>

 <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="200px" style="float: left" />

 <p>{{ publi.description }}</p>

 <p><em>{{ publi.authors }}</em></p>

 <p>{{ publi.venue }}</p>

 {% if publi.number_link == 1 %}
 <p><a href="{{ publi.link1.url }}">{{ publi.link1.display }}</a></p>
 {% endif %}

 {% if publi.number_link == 2 %}
 <p><a href="{{ publi.link1.url }}">{{ publi.link1.display }}</a>
 /
 <a href="{{ publi.link2.url }}">{{ publi.link2.display }}</a></p>
 {% endif %}

 {% if publi.number_link == 3 %}
 <p><a href="{{ publi.link1.url }}">{{ publi.link1.display }}</a>
 /
 <a href="{{ publi.link2.url }}">{{ publi.link2.display }}</a>
 /
 <a href="{{ publi.link3.url }}">{{ publi.link3.display }}</a></p>
 {% endif %}

 {% if publi.number_link == 4 %}
 <p><a href="{{ publi.link1.url }}">{{ publi.link1.display }}</a>
 /
 <a href="{{ publi.link2.url }}">{{ publi.link2.display }}</a>
 /
 <a href="{{ publi.link3.url }}">{{ publi.link3.display }}</a>
 /
 <a href="{{ publi.link4.url }}">{{ publi.link4.display }}</a></p>
 {% endif %}

 {% if publi.number_link == 5 %}
 <p><a href="{{ publi.link1.url }}">{{ publi.link1.display }}</a>
 /
 <a href="{{ publi.link2.url }}">{{ publi.link2.display }}</a>
 /
 <a href="{{ publi.link3.url }}">{{ publi.link3.display }}</a>
 /
 <a href="{{ publi.link4.url }}">{{ publi.link4.display }}</a>
 /
 <a href="{{ publi.link5.url }}">{{ publi.link5.display }}</a></p>
 {% endif %}

 </div>
</div>

{% endfor %}

<p> &nbsp; </p>

<!-- ## Full List

{% for publi in site.data.publist %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %} -->
