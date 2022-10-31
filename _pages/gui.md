---
title: "Hengmin Zhang - GUI for HAR"
layout: gridlay
excerpt: "Hengmin Zhang -- GUI for HAR"
sitemap: false
permalink: /gui/
---

### GUI for Human Activity Recognition using wearable devices22

<center>
<figure>
		<div id="projectid">
    <img src="{{ site.url }}{{ site.baseurl }}/images/explore/GUI.png" width="700px" />
		</div>

<figcaption>
<br>
Overview

</figcaption>
</figure>
</center>

- This project is a GUI based on Tkinter. The sensor datas operated by sliding window are stored in "/dataset/WISDM".The data can be download from <a href="https://www.cis.fordham.edu/wisdm/dataset.php">WISDM</a> website. We can extract random samples from them to predict human actions.<br>
We can Randomly select a time-series sample in WISDM. It can be visualized as below:

<center>
<figure>
		<div id="projectid">
    <img src="{{ site.url }}{{ site.baseurl }}/images/explore/raw_data.png" width="400px" />
		</div>

<figcaption>
<br>
Multimodal sensor signals in WISDM 

</figcaption>
</figure>
</center>

- The model in the Figure is algorithms based on machine learning or deep learning. We give the example of CNNs in our <a href="https://github.com/Claydon-Wang/GUI-for-HAR">respositories</a>. The model can be trained in remote server and further deployed on mobile devices like Raspberry Pi. Hence, we can intuitively evaluate the model efficiency through metrics such as inference time.
- WISDM dataset contains 6 activities:
<center>
<figure>
		<div id="projectid">
    <img src="{{ site.url }}{{ site.baseurl }}/images/explore/HAR/standing.png" width="150px" />
    <img src="{{ site.url }}{{ site.baseurl }}/images/explore/HAR/sitting.png" width="150px" />
    <img src="{{ site.url }}{{ site.baseurl }}/images/explore/HAR/jogging.png" width="150px" />
    <img src="{{ site.url }}{{ site.baseurl }}/images/explore/HAR/walking.png" width="150px" />
    <img src="{{ site.url }}{{ site.baseurl }}/images/explore/HAR/upstairs.png" width="150px" />
    <img src="{{ site.url }}{{ site.baseurl }}/images/explore/HAR/downstairs.png" width="150px" />
		</div>

<figcaption>
<br>
Activities in WISDM

</figcaption>
</figure>
</center>

- The results can be shown as below:

- The initial interface can be shown as below:

<center>
<figure>
		<div id="projectid">
    <img src="{{ site.url }}{{ site.baseurl }}/images/explore/origin.png" width="300px" />
		</div>

<figcaption>
<br>
Initial interface

</figcaption>
</figure>
</center>

- The results can be shown as below:

<center>
<figure>
		<div id="projectid">
    <img src="{{ site.url }}{{ site.baseurl }}/images/explore/classification.png" width="300px" />
		</div>

<figcaption>
<br>
Results example

</figcaption>
</figure>
</center>

#### Acknowledgements
Thank to my friend <a href="https://github.com/Chauncey-Wang">Xin Wang</a> for the discussion and help in this project.