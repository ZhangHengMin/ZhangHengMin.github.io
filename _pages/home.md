---
title: "Hengmin Zhang - Homepage"
layout: gridlay
excerpt: "Hengmin Zhang"
sitemap: false
permalink: /
---

<div class="container-fluid">

<div class="row">

<div class="col-sm-8">

### **Biography**

Dr Zhang is a Research Fellow with the School of Electrical and Electronic Engineering, **Nanyang Technological University (NTU)**, Singapore. Prior to that, he received the Ph.D. degree from the School of Computer Science and Engineering, *Nanjing University of Science and Technology (NUST)*, Nanjing, China.   

His research areas are Pattern Recognition, Numerical Optimization, Machine Learning, and Intelligent System.
 

### **News**
{% for article in site.data.news limit:20 %}
{{ article.date }} :
<em>{{ article.headline }}</em>
{% endfor %}
<a href="{{ site.url }}{{ site.baseurl }}/allnews.html"></a>

</div>

<div class="col-sm-4" style="display:table-cell; vertical-align:middle; text-align:center">

  <ul style="overflow: hidden">
  <img src="{{ site.url }}{{ site.baseurl }}/images/myself.jpg" class="img-responsive" width="85%" />
  </ul>

  <!-- <br clear="all" /> -->

  Google Scholar: <a href="https://scholar.google.com/citations?user=a1yd0H4AAAAJ&hl=zh-CN&oi=sra">Hengmin Zhang</a> <br>
  Email: zhanghengmin@126.com   
  
   


  <!-- <script type="text/javascript" id="clstr_globe" src="//clustrmaps.com/globe.js?d=qxy0eSYxkkDD23T1VJXNWt4_fn9cGJ1JRNShKPoCy8Y"></script> -->


</div>





