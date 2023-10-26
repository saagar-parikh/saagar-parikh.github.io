---
layout: page
title: PointResNet - Residual Network for 3D Point Cloud Segmentation and Classification
description:
img: assets/img/pointresnet-cover.png
importance: 5
category: work
project_pdf: https://arxiv.org/abs/2211.11040
---

- Designed a residual-block based novel architecture that outperformed the baselines by 4% for the segmentation task on ShapeNetPart dataset and produced comparable results for the classification task on the ModelNet-40 dataset.
- The network takes n input points and applies transformations, several multi-layer perceptron (MLP) layers with skip connections, and then aggregates features using max pooling. The classification network applies fully connected and dropout layers and obtains k scores for k classes. The segmentation network extends the classification network by combining local and global features, using convolutional layers, and finally giving per point scores as output. The connected skip layers represent ResBlock-n, where n is the number of features of a single block layer. Numbers in MLP layers represent a number of features.
<p align="center"><img src="/assets/img/pointresnet-block.png" width="100%"></p>


<p align="center"><img src="/assets/img/pointresnet-seg.png" width="50%"></p>
<p align="center">Qualitative comparison of part segmentation results on ShapeNetPart dataset</p>


<div align="center">
    
<table class="tg">
    <tr>
        <td></td>
        <td>Eval acc &#8593;</td>
    </tr>
    <tr>
        <td>PointNet</td>
        <td align="center">90.6</td>
    </tr>
    <tr>
        <td>PointNet++</td>
        <td align="center">88.4</td>
    </tr>
    <tr>
        <td>ECC</td>
        <td align="center">90.8</td>
    </tr>
    <tr>
        <td>RTN</td>
        <td align="center">92.6</td>
    </tr>
    <tr>
        <td>PointResNet (Ours)</td>
        <td align="center"><b>94.79</b></td>
    </tr>
</table>


Quantitative comparison of part segmentation results on ShapeNetPart dataset
</div>



<div align="center">

<table class="tg">
<thead>
  <tr>
    <th></th>
    <th align="center" colspan="2">ModelNet10</th>
    <th align="center" colspan="2">ModelNet40</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td></td>
    <td>Eval acc</td>
    <td>Eval avg class acc</td>
    <td>Eval acc</td>
    <td>Eval avg class acc</td>
  </tr>
  <tr>
    <td>PointNet</td>
    <td align="center">92.52</td>
    <td align="center">92.08</td>
    <td align="center">89.2</td>
    <td align="center">86.2</td>
  </tr>
  <tr>
    <td>PointNet++</td>
    <td align="center">-</td>
    <td align="center">-</td>
    <td align="center">91.9</td>
    <td align="center">-</td>
  </tr>
  <tr>
    <td>PointConv</td>
    <td align="center">-</td>
    <td align="center">-</td>
    <td align="center"><b>92.5</b></td>
    <td align="center">-</td>
  </tr>
  <tr>
    <td>ECC</td>
    <td align="center">90.0</td>
    <td align="center">-</td>
    <td align="center">83.2</td>
    <td align="center">-</td>
  </tr>
  <tr>
    <td>RTN</td>
    <td align="center">-</td>
    <td align="center">-</td>
    <td align="center">90.2</td>
    <td align="center">86.5</td>
  </tr>
  <tr>
    <td>ResNet-50</td>
    <td align="center">-</td>
    <td align="center">-</td>
    <td align="center">66.3</td>
    <td align="center">-</td>
  </tr>
  <tr>
    <td>PointResNet (Ours)</td>
    <td align="center"><b>92.86</b></td>
    <td align="center"><b>92.29</b></td>
    <td align="center">88.76</td>
    <td align="center">85.58</td>
  </tr>
</tbody>
</table>


Quantitative comparison of classification accuracy on ModelNet10 and ModelNet40 with the state-of-the-art methods.

</div>

