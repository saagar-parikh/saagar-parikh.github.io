---
layout: page
title: Automated Active Learning for ZTF Data
description: 
img: assets/img/caltech-ztf-banner.jpg
importance: 1
category: work
github: https://github.com/saagar-parikh/scope
related_publications: 
---

Formulated a robust active learning framework with automation in selecting the data points to be labeled to reduce human
efforts by 90% and improve the performance of existing classification models such as DNN and XGBoost.

Analyzed billions of astronomical sources and their time-series representation of varying intensities (light curves) from the
Zwicky Transient Facility (ZTF) survey and used API queries and data visualization for preprocessing tasks

<figure>
    <img src="assets/img/caltech-flowchart.jpeg" alt="flowchart" align="middle" width="500">
    <figcaption>Active learning pipeline that selects the most impactful sources using: i. the 6 types based on the classification scores, ii. spatial cross-matching and demanding agreement between the g and r bands, iii. braai scores, and iv. amplitudes.</figcaption>
</figure>

<!--
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/caltech-flowchart.jpeg" class="img-fluid rounded z-depth-1" align="center" width="500" %}
    </div>
</div>
<div class="caption">
    Active learning pipeline that selects the most impactful sources using: i. the 6 types based on the classification scores, ii. spatial cross-matching and demanding agreement between the g and r bands, iii. braai scores, and iv. amplitudes.
</div>
-->
