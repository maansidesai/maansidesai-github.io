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

Our results showed strong tracking of acoustic and phonetic information in both the TIMIT and movie trailer stimuli. The model performance for TIMIT was generally better compared movie trailers which is likely attributed to the additional sound sources such as music, overlapping speakers, and background noise in the trailers compared to isolated speech from the TIMIT sentences. However despite the differences in the acoustic content of these contrasting stimuli, we found that it is possible to use a more naturalistic audiovisual stimuli and still robustly encode neural responses to speech information. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/F3.large.jpg" title="Main findings from Figure 3 of paper" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The Convex-Hull plots in panels A and B show the contribution of acoustic and phonetic information for the TIMIT and movie trailer stimuli, where the unity line separates the model performance when using a combination of phonological features, pitch, and the acoustic envelope versus using one of these features by itself. Generally, the acoustic envelope and phonological features were more predictive of EEG data than pitch, which contributed a small but significant proportion of unique variance for both TIMIT and movie trailers.
    In panels C and D, we performed a variance partition analysis shows the unique variance explained by individual features (phonological features, pitch, and envelope) for each participant separately (bar chart) and across all participants (pie chart) when fit on TIMIT data. 
    Overall, our results suggest that neural tracking for phonological features occurs both in noise-free as well as more uncontrolled, naturalistic settings despite the presence of varied background noise.
</div>

To learn more about the findings, check out the paper here: <a href="https://www.jneurosci.org/content/41/43/8946#sec-16">Desai et al. 2021</a>

