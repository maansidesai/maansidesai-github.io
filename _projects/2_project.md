---
layout: page
title: Dataset size considerations
description: Findings summarized from Desai et al. 2023 (Frontiers in Human Neuroscience)
img: assets/img/MT_how_much.jpg
importance: 2
category: work
giscus_comments: true
---

Thinking about building neuroscience experiments that are ecologically valid is important, especially when working with children or clinical populations who may not be able to withstand long and tedious tasks. A follow up study utilized the same movie trailer and sentence listening stimuli to answer a fundamental methodological question: how much data does one need to collect to trust the fidelity of the results when using naturalistic stimuli? When working with clinical populations or children, an experimenter may be limited in the amount of time they have for data collection. In the 2021 JNeuro study, we investigated acoustic and phonetic selectivity measured with EEG collected over the span of one hour. We wondered, however, whether their results would still be as reliable with a shorter experimental session. Myself and colleagues in the Hamilton lab have reported considerations for the amount of data needed and provide some suggestions for future developing natural speech experimental paradigms. 

In this study, we used the same movie trailer and TIMIT speech sentences in addition to openly published existing EEG dataset where <a href="https://pubmed.ncbi.nlm.nih.gov/29478856/">Broderick et al. 2018</a> had participants listened to audiobooks, another form of naturalisitic speech stimuli. We conducted the same encoding model by chunking our training set data into 2-second long segments. The size of the data subset started with 10 random sentences for TIMIT, or 10 2-s chunks of movie trailers or audiobook stimuli. This chunk size was chosen as it is similar to the average TIMIT sentence length. After fitting the models on a subset of data, the size of the training set was gradually increased (by 1 random TIMIT sentence at a time or a random 2-s chunk of movie trailers or a random 2-s chunk of audiobooks). For each training set size, we used a 10-fold bootstrapping procedure so that the particular 2-s chunks included in the training set were sampled randomly from the original training dataset.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/how_much_data_2.jpg" title="Main kneepoint figure" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This plot shows the increasing correlation value based on the stimulus set used (TIMIT, movie trailers, or audiobooks) for each feature representation used (acoustic or phonetic) to predict the EEG data. Dashed vertical lines and shading indicate the knee point and corresponding error bar for each individual model type. Despite different numbers of features and differing model complexity, a similar amount of data was required for each of these models
</div>

<title>Embedded Videos</title>
<style>
  .video-container {
    display: flex;
    justify-content: space-between;
    margin-bottom: 20px;
  }

  .video {
    width: 45%; /* Adjust as needed */
  }
</style>

<body>

<div class="video-container">
  <video class="video" controls>
    <source src="assets/video/timit.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
  
  <video class="video" controls>
    <source src="assets/video/mt.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</div>

</body>



Extra code below to remove/edit

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/how_much_data_2.jpg" title="Main kneepoint figure" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, _bled_ for your project, and then... you reveal its glory in the next row of images.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>

The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}

```html
<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
```

{% endraw %}
