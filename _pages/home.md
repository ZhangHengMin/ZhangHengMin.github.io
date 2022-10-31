---
title: "Shuoyuan Wang - Home"
layout: gridlay
excerpt: "Shuoyuan Wang"
sitemap: false
permalink: /
---

<div class="container-fluid">

<div class="row">

<div class="col-sm-8">
I am currently pursuing the Bachelor's degree of <a href="http://www.njnu.edu.cn/">Nanjing Normal University</a>, Nanjing, China. My recent research interests are in Machine Learning, Deep Learning and Human Activity Recognition(HAR) using wearables. <a href="https://scholar.google.com/citations?hl=zh-CN&user=n1qFlf8AAAAJ">A.P Lei Zhang</a> is my advisor. I am willing to dive into data-driven research including Machine Learning, Edge-AI, Computer Vision, Computational Biology, etc. <br> Remimd the date: <a href="https://aideadlin.es/?sub=ML,CV">AI</a> and <a href="https://ccfddl.github.io/">CCF</a>


### CV
You can download my [CV (English Version)](https://claydon-wang.github.io//papers/CV_E.pdf) here.

### News
{% for article in site.data.news limit:20 %}
{{ article.date }} :
<em>{{ article.headline }}</em>
{% endfor %}
<a href="{{ site.url }}{{ site.baseurl }}/allnews.html">see all news</a>

</div>

<div class="col-sm-4" style="display:table-cell; vertical-align:middle; text-align:center">

  <ul style="overflow: hidden">
  <img src="{{ site.url }}{{ site.baseurl }}/images/myself.jpg" class="img-responsive" width="100%" />
  </ul>

  <!-- <br clear="all" /> -->

  Shuoyuan Wang (王朔远)<br>  
  <a href="http://d.njnu.edu.cn/">School of Electric and Autumation Engineerning</a> <br>  
  <a href="http://www.njnu.edu.cn/">Nanjing Normal University</a> <br>  
  Nanjing, Jiangsu, China. <br>  
  E-mail: <a href="mailto:claytonwang0205@gmail.com.com">claytonwang0205@gmail.com</a> or <a href="mailto:21180403@njnu.edu.cn">21180403@njnu.edu.cn</a> <br>  
  Github&Gitlab: <a href="https://github.com/Claydon-Wang">Claydon-Wang</a> & <a href="https://gitlab.com/Clayden-Wang">Claydon-Wang</a> <br>
  ORCID: <a href="https://orcid.org/0000-0003-1795-4161">0000-0003-1795-4161</a> <br>   
  Google Scholar: <a href="https://scholar.google.com/citations?hl=zh-CN&user=SfMkEYgAAAAJ">Shuoyuan Wang</a> <br>
  Kaggle: <a href="https://www.kaggle.com/claydonwang">Khadgar</a> <br>
  <script type='text/javascript' id='clustrmaps' src='//cdn.clustrmaps.com/map_v2.js?cl=ffffff&w=200&t=n&d=qxy0eSYxkkDD23T1VJXNWt4_fn9cGJ1JRNShKPoCy8Y&co=4298d4&cmo=39c583&cmn=ebaa26'></script>

  <!-- <script type="text/javascript" id="clstr_globe" src="//clustrmaps.com/globe.js?d=qxy0eSYxkkDD23T1VJXNWt4_fn9cGJ1JRNShKPoCy8Y"></script> -->


</div>

</div>
</div>

<div class="col-sm-12">

### Publications
My papers may be under review and can be found in my [CV](https://claydon-wang.github.io//papers/CV_E.pdf). You can refer to the [abstract](https://claydon-wang.github.io//papers/Abstract.pdf) of my ""first-author" paper currently. I will release my <a href="https://scholar.google.com/citations?hl=zh-CN&user=SfMkEYgAAAAJ">paper</a> and <a href="https://github.com/Claydon-Wang">code</a> once my paper is accepted.<br>


{% for publi in site.data.publist limit:100 %}

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

<br clear="all"/>

##### <a href="{{ site.url }}{{ site.baseurl }}/publications">see all publications</a>

</div>

<div class="col-sm-12">

### Explorations

{% for publi in site.data.exlist limit:6 %}

<div class="col-sm-11 clearfix">
 <div class="well">
 <pubtit>{{ publi.title }}</pubtit>

 <img src="{{ site.url }}{{ site.baseurl }}/images/explore/{{ publi.image }}" class="img-responsive" width="200px" style="float: left" />

 <p>{{ publi.description }}</p>

 <p><em>{{ publi.participants }}</em></p>

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
 
 {% if publi.number_link == 6 %}
 <p><a href="{{ publi.link1.url }}">{{ publi.link1.display }}</a>
 /
 <a href="{{ publi.link2.url }}">{{ publi.link2.display }}</a>
 /
 <a href="{{ publi.link3.url }}">{{ publi.link3.display }}</a>
 /
 <a href="{{ publi.link4.url }}">{{ publi.link4.display }}</a>
 /
 <a href="{{ publi.link5.url }}">{{ publi.link5.display }}</a>
 /
 <a href="{{ publi.link6.url }}">{{ publi.link6.display }}</a></p>
 {% endif %}

 </div>
</div>

{% endfor %}
<br clear="all"/>

##### <a href="{{ site.url }}{{ site.baseurl }}/explorations">see all research explorations</a>

<p> &nbsp; </p>

</div>

