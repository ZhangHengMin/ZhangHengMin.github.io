---
title: "Hengmin Zhang - Publications"
layout: gridlay
excerpt: "Hengmin Zhang -- Publications."
sitemap: false
permalink: /publications/
---


### Publications
-  **Memory Bank**: A non-local bank operator is used to attentively relate the past to the present. The memory bank is consisting of Resnet50 and LSTM network for the storage of long-term characteristics. It needs to be train in advance. The sequence length is optional. In my perspectives, the whole architecture is not end-to-end since the trained memory bank can be a reference in the training of backbone and do not need to calculate gradients and do backpropagation. Hence, it can great save computational cost.
- **Temporal variation layer**: Tolerating the varieties in temporal extent is essential. The temporal variation module(Multi-scale CNNs) is introduced to capture features in different temporal scales. It is worth noticed that the different temporal features are stacked along channel dimension and conclude the layer by a max-pooling layer for channel reduction. Hence, the output can have the same shape with the module input.
- **Non-local Bank Operator**: To effectively leverage long-range and multi-scale past information, a unified temporal memory relation network is introduced to achieve it. All the preceding features are considered with the current time step, hence, the current feature can be augmented. Also, the linear operation avoids too heavy regularization with similarity matrix directly performed on the input signal. It seems take the inspiration of <a href=" http://proceedings.mlr.press/v70/dauphin17a"> GLU </a> in this module which is good at long-term modeling.

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


### Theses

<p>To be continued</p><br>

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
