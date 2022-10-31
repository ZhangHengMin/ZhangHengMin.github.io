---
title: "Hengmin Zhang - Home"
layout: gridlay
excerpt: "Hengmin Zhang"
sitemap: false
permalink: /
---

<div class="container-fluid">

<div class="row">

<div class="col-sm-8">
Dr Zhang is willing to dive into data-driven research including Machine Learning, Edge-AI, Computer Vision, Computational Biology, etc. <br> Remimd the date: <a href="https://aideadlin.es/?sub=ML,CV">AI</a> and <a href="https://ccfddl.github.io/">CCF</a>


 

### News
{% for article in site.data.news limit:20 %}
{{ article.date }} :
<em>{{ article.headline }}</em>
{% endfor %}
<a href="{{ site.url }}{{ site.baseurl }}/allnews.html"></a>

</div>

<div class="col-sm-4" style="display:table-cell; vertical-align:middle; text-align:center">

  <ul style="overflow: hidden">
  <img src="{{ site.url }}{{ site.baseurl }}/images/myself.jpg" class="img-responsive" width="60%" />
  </ul>

  <!-- <br clear="all" /> -->

  Github&Gitlab: <a href="https://github.com/ZhangHengMin">ZhangHengMin</a> & <a href="https://gitlab.com/ZhangHengMin">ZhangHengMin</a> <br>
  ORCID: <a href="https://orcid.org/0000-0003-1795-4161">0000-0003-1795-4161</a> <br>   
  Google Scholar: <a href="https://scholar.google.com/citations?hl=zh-CN&user=SfMkEYgAAAAJ">Shuoyuan Wang</a> <br>
  Kaggle: <a href="https://www.kaggle.com/zhanghengmin">Khadgar</a> <br>


  <!-- <script type="text/javascript" id="clstr_globe" src="//clustrmaps.com/globe.js?d=qxy0eSYxkkDD23T1VJXNWt4_fn9cGJ1JRNShKPoCy8Y"></script> -->


</div>





