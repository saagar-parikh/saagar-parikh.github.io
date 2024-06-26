---
layout: page
title: Automated Active Learning for ZTF Data
description: 
img: assets/img/caltech-cover.png
importance: 5
category: work
github: https://github.com/saagar-parikh/scope
project_pdf: https://drive.google.com/file/d/1yAK0L4ZAONK__nz-AtWX9mYuta2f_DDQ/view?usp=share_link
related_publications: 
---
<!--
<table>
  <tr>
    <td align="left" width="50%">Summer Undergraduate Research Fellow</td>
    <td align="right" width="50%">May 2022 - Jul 2022</td>
  </tr>
  <tr>
    <td align="left" width="50%">California Institute of Technology</td>
    <td align="right" width="50%">Pasadena, PA</td>
  </tr>
</table>
-->
<style>
.responsive-wrap iframe{ max-width: 100%;}
</style>


- Formulated a robust active learning framework with automation in selecting the data points to be labeled to reduce human efforts by 90% and improve the performance of existing classification models such as DNN and XGBoost.
- Analyzed billions of astronomical sources and their time-series representation of varying intensities (light curves) from the Zwicky Transient Facility (ZTF) survey and used API queries and data visualization for preprocessing tasks

Quick Links:
- [GitHub](https://github.com/saagar-parikh/scope)
- [Report](https://drive.google.com/file/d/1yAK0L4ZAONK__nz-AtWX9mYuta2f_DDQ/view?usp=share_link)
- [Slide Deck](https://docs.google.com/presentation/d/1LZb8REz-GU_0IbBQegeJj5PaQQXCzWyd/edit?usp=drive_link&ouid=104194021196236041832&rtpof=true&sd=true)


### Active Learning Pipeline

<p align="center"><img src="/assets/img/caltech-flowchart.jpeg" alt="flowchart" width="60%"></p>

Active learning pipeline that selects the most impactful sources using: i. the 6 types based on the classification scores, ii. spatial cross-matching and demanding agreement between the g and r bands, iii. braai scores, and iv. amplitudes.

### Consolidated data format

Relabelling has to be done by trained professionals, and they should be provided all the useful information in a consolidated form to save time. 
Thus, created combined plots of all the required information in a single image, as shown below

<p align="center"><img src="/assets/img/caltech-combined-image.jpg" alt="flowchart" width="80%"></p>

Combined image containing the consolidated data to be shown to the domain expert for labelling containing the following information: light curve, phase-folded light curve, cutouts, Gaia HR diagram, class scores and metadata such as ra, dec, period, amplitude, standard deviation and inverse von Neumann ratio


### Slide Deck

<div align="center" class="responsive-wrap">
<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vS_I6sFbWSb7KGZVQmyQF6hDNNjeZWSHlp91ZwShaIO_LwHe9sHj0PzBaKioaGCIw/embed?start=true&loop=true&delayms=3000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>
</div>