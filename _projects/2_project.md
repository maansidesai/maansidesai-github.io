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


One method of evaluating model performance is by examining the correlation coefficient. Assessing the correlation value from the model can show a qualitative stability of model weights, it does not show whether the fitted weights themselves are similar and stable when using more or less training data. In order to look at how the weights stabilize over time when adding more training data, we plotted the receptive fields at each iteration of adding increasing amounts of training set data for the TIMIT and movie trailer stimuli. Examples are shown in the videos below for one subject:


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
    <source src="https://maansidesai.github.io/assets/video/timit.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
  
  <video class="video" controls>
    <source src="https://maansidesai.github.io/assets/video/mt.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</div>

</body>

