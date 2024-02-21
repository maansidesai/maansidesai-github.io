---
layout: page
title: Generalizable EEG encoding models with naturalistic audiovisual stimuli
description: Findings summarized from Desai et al. 2021 (Journal of Neuroscience)
img: assets/img/eeg.jpg
importance: 1
category: work
related_publications: true
---

Understanding speech and language is something that humans engage in daily, and for many it is relatively effortless. However, the brain’s ability to comprehend speech in a naturalistic and noisy environment is a complex process. To understand this process, scientists conduct experiments using electrophysiological measurements such as electroencephalography (EEG), a non-invasive method of recording brain activity from the level of the scalp, and various types of stimuli. These stimuli range from simple “clicks” or “tones”, to syllables, or short sentences. Unfortunately, these stimuli are limited in understanding how the brain processes speech and sounds in a naturalistic environment. Additionally, listening to a single tone of a syllable such as “ba” or “ga” or sentences repeatedly as an EEG participant is tedious and boring. 

 We used naturalistic stimuli, specifically children’s movie trailers, to understand how the brain processes speech and audiovisual information. A primary motivation of this study was to see if it possible to replace more controlled experiments, such as sentence listening, with stimuli that are more engaging and fun to listen to. This is particularly important as some of my dissertation research involved working with children in an in-patient hospital environment, so interesting tasks mean a better experience for both researcher and participant. These results showed that it was possible to robustly encode speech using acoustically rich and naturalistic stimuli such as movie trailers and these results were comparable to understanding how the brain processes speech in a noise-free sentence listening setting [1].


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/F1.large.jpg" title="Task and analysis schematic" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Task and analysis schematic (Figure 1 from the study). Here, recorded scalp EEG responses as participants listened to sentence from the TIMIT (Texas Instruments Massachusetts Institute of Technology) speech corpus, and listened to and watched movie trailers. We extracted acoustic and phonetic properties of the corresponding speech information and fit encoding models to predict neural responses to these speech feature representations at each EEG channel. 
</div>

Our results demonstrated 

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
