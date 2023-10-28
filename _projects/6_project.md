---
layout: page
title: Enhancement of Infrared Night Vision Images
description:
img: assets/img/imgenhance-cover.png
importance: 6
category: work
github: https://github.com/saagar-parikh/image-enhancement-verilog/
---

- Evaluated image enhancement algorithms like Histogram Equalization and Histogram Matching to increase the contrast in infrared images using OpenCV and ranked them based on their Peak Signal-to-Noise Ratio (PSNR) values.
- Simulated the top performing algorithms on an FPGA board using Verilog.

<table>
<thead>
  <tr>
    <th></th>
    <th>Original</th>
    <th>DPHE</th>
    <th>HE</th>
    <th>Advanced Enhanced Image</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td><p align="center">Image 1</td>
    <td><p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week4/Images/4_190x150.png">
      </p>
    </td>
    <td><p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week4/Images/4_DPHE_vivado.png">
      </p>
   </td>    
   <td><p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week4/Images/4_HE_vivado.png">
      </p>
   </td>  
   <td><p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week4/Images/4_matlab.png">
      </p>
   </td>
 </tr>
  <tr>
    <td><p align="center">Image 2</td>
    <td><p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week4/Images/8_190x150.png">
      </p>
    </td>
    <td><p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week4/Images/8_DPHE_vivado.png">
      </p>
   </td>    
   <td><p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week4/Images/8_HE_vivado.png">
      </p>
   </td>  
   <td><p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week4/Images/8_matlab.png">
      </p>
   </td>
 </tr>
  <tr>
    <td><p align="center">Image 3</td>
    <td><p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week4/Images/634_190x150.png">
      </p>
    </td>
    <td><p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week4/Images/634_DPHE_vivado.png">
      </p>
   </td>    
   <td><p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week4/Images/634_HE_vivado.png">
      </p>
   </td>  
   <td><p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week4/Images/634_matlab.png">
      </p>
   </td>
 </tr>
  <tr>
    <td><p align="center">Image 4</td>
    <td><p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week4/Images/4119_190x150.png">
      </p>
    </td>
    <td><p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week4/Images/4119_DPHE_vivado.png">
      </p>
   </td>    
   <td><p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week4/Images/4119_HE_vivado.png">
      </p>
   </td>  
   <td><p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week4/Images/4119_matlab.png">
      </p>
   </td>
 </tr>
</tbody>
</table>

<h2> Brief</h2>

<b>Algorithms used:</b>
<ol>
  <li>Histogram Equalisation
  <li>Histogram Matching
  <li>Double Plateau Histogram Equalisation
  <li>Top Hat Transform
</ol>  
<!--
* [**Performance Comparison**](#performance-comparison-of-the-algorithms)
* [**Verilog Implementation**](#verilog-implementation)
* [**Future Scope**](#future-scope)
* [**Acknowledgement**](#acknowledgement)
-->
<b>Dataset:</b> <a href="https://projects.asl.ethz.ch/datasets/doku.php?id=ir:iricra2014">ir:iricra2014 – ASL Datasets</a>

<h2>Algorithms</h2>
<h3>1. Histogram Equalisation</h3>
<ul>
  <li>A contrast stretching algorithm with a mathematical function that uniformly stretches the image histogram.</li>
  <li>Calculate the  probability and cumulative distribution function(CDF) of gray scale values, normalize the values by multiplying  CDF values with the greatest gray scale level.</li>
  <li>Stretches the intensity values present in the image to the entire range of intensity values, thus increasing the contrast of the image.</li>
</ul>


<b>Sample Results:</b>

<table border="0">
 <tr>
    <td></td>
    <td><b style="font-size:15px"><p align="center">Image</b></td>
    <td><b style="font-size:15px"><p align="center">Histogram</b></td>
 </tr>
 <tr>
    <td><p align="center">Original</p></td>
    <td>
      <p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week1/Histogram Equalisation/8.png">
      </p>
    </td>
    <td>
      <p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week1/Histogram Equalisation/8-orig-hist.png">
      </p>
    </td>
 </tr>
 <tr>
    <td><p align="center">Enhanced</td>
    <td>
      <p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week1/Histogram Equalisation/8-after-manual-histequal.png">
      </p>
    </td>
    <td>
      <p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week1/Histogram Equalisation/8-equalized-hist.png">
      </p>
    </td>
 </tr>
</table>


<h2>2. Histogram Matching</h2>
<ul>
  <li>Extension of histogram equalization.
  <li>This algorithm transforms a target image so that it’s histogram matches with the histogram of a given reference image.
  <li>Firstly, histogram equalization is performed on both, the target and the reference image, which is then followed by the matching part.
  <li>The target image histogram is manipulated such that it matches the histogram of the reference image.
</ul>
<b>Sample Results:</b>

<table border="0">
 <tr>
    <td></td>
    <td><b style="font-size:15px"><p align="center">Image</b></td>
    <td><b style="font-size:15px"><p align="center">Histogram</b></td>
 </tr>
 <tr>
    <td><p align="center">Reference</p></td>
    <td>
      <p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week1/Histogram Matching/ref.jpeg">
      </p>
    </td>
    <td>
      <p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week1/Histogram Matching/ref-orig-hist.png">
      </p>
    </td>
 </tr>
 <tr>
    <td><p align="center">Target</td>
    <td>
      <p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week1/Histogram Matching/target.jpeg">
      </p>
    </td>
    <td>
      <p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week1/Histogram Matching/target-orig-hist.png">
      </p>
    </td>
 </tr>
 <tr>
    <td><p align="center">Target after Histogram Matching</td>
    <td>
      <p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week1/Histogram Matching/target-after-hist-match.jpeg">
      </p>
    </td>
    <td>
      <p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week1/Histogram Matching/target-match-hist.png">
      </p>
    </td>
 </tr>
</table>

<h2>3. Double Plateau Histogram Equalisation</h2>
<ul>
  <li>In the image histogram, there are certain grayscale values (bins) which have exceptionally high frequencies while some have very low.
  <li>Thus, we select two threshold values of frequencies, and clip the bins according to these thresholds.
  <li>The excess pixels in a high frequency bin are redistributed into the bins having low frequencies.
</ul>
<b>Sample Results:</b>

<table border="0">
 <tr>
    <td></td>
    <td><b style="font-size:15px"><p align="center">Image</b></td>
    <td><b style="font-size:15px"><p align="center">Histogram</b></td>
 </tr>
 <tr>
    <td><p align="center">Original</p></td>
    <td>
      <p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week2/Double Plateaus Histogram Equalisation/1.png">
      </p>
    </td>
    <td>
      <p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week2/Double Plateaus Histogram Equalisation/1-orig-hist.png">
      </p>
    </td>
 </tr>
 <tr>
    <td><p align="center">Enhanced</td>
    <td>
      <p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week2/Double Plateaus Histogram Equalisation/1-dphe-img.png">
      </p>
    </td>
    <td>
      <p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week2/Double Plateaus Histogram Equalisation/1-dphe-hist.png">
      </p>
    </td>
 </tr>
</table>

<b>Clipped Frequencies Graph:</b>
 <p align="center">
   <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week2/Double Plateaus Histogram Equalisation/1-clipped-freq-graph.png">
 </p>

<h2>4. Top Hat Transform</h2>
<ul>
  <li>In digital image processing, the algorithm extracts minute elements and details from the images.
  <li>Considering structural elements, the filter enhances bright  objects of interests in a dark background.
  <li>Hence, it focuses on enhancing the light pixels in dark background.
</ul>
<table border="0">
 <tr>
    <td><b style="font-size:15px"><p align="center">Original Image</b></td>
    <td><b style="font-size:15px"><p align="center">Enhanced Image</b></td>
 </tr>
 <tr>
    <td>
      <p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week2/Top Hat Transform/128.png">
      </p>
    </td>
    <td>
      <p align="center">
        <img width="400" src="https://github.com/saagar-parikh/image-enhancement-verilog/blob/main/Week2/Top Hat Transform/128-tophat-img.png">
      </p>
    </td>
 </tr>
</table>

<h2>Performance Comparison of the Algorithms</h2>
<ul>
  <li><b>Peak Signal to Noise Ratio (PSNR)</b>: It uses the mean squared error of all the pixels between the two images to compute an expression.
  <li>The higher the PSNR value, the better the image enhancement.
  <li>We compare the PSNR value of all the 4 new images with an enhanced image obtained using an advanced, inbuilt image processing function on MATLAB.
  <li>Based on the PSNR values, Double Plateaus Histogram Equalization and Histogram Equalization were the best performing algorithms.
</ul>

<p>
Results:
<ul>
  <li>Histogram Equalisation PSNR = 14.132
  <li>Histogram Matching PSNR = 13.722
  <li>Double Plateau Histogram Equalisation PSNR = 21.523
  <li>Top Hat Transform PSNR = 9.854
</ul>

<h2>Verilog Implementation</h2>

<h3>1. Reading images in Vivado</h3>
<ul>
  <li>Images need to be converted to binary text files to be read onto Vivado.
  <li>The entire image is flattened to a 1 D array, each element contains the pixel’s intensity value in binary 8 bit format using Python.
  <li>The file can be read using the readmemb function on Vivado.
</ul>
<h3>2. Performing the algorithms in Vivado</h3> 
<ul>
  <li>The image is read on the testbench and passed to the design module.
  <li>The design consists of a single module:
    <ul>
      <li>It inputs the image as a 1 D array and converts it to a 2 D array of dimensions same as that of the original image.
      <li>The algorithm is now performed on this 2 D array that represents the image.
      <li>This image is again flattened to a 1 D image and sent as an output to the testbench.
    </ul>
<p>
The output is received at the testbench and written into a binary file.
This binary text file is converted to obtain the new image using python.

<h2>3. Comparing the algorithms in Vivado</h2>

<b>Comparison:</b>
<p>
PSNR values of images obtained from both the algorithms for different images:

<table border="0">
 <tr>
  <td><p align="center">Image no.</td>
  <td><p align="center">PSNR after<br> Histogram Equalisation</td>
  <td><p align="center">PSNR after<br> Double Plateaus Histogram Equalisation</td>
 </tr>
 <tr>
  <td><p align="center">Image 1</td>
  <td><p align="center">12.703</td>
  <td><p align="center">23.120</td>
 </tr>
 <tr>
  <td><p align="center">Image 2</td>
  <td><p align="center">9.144</td>
  <td><p align="center">24.936</td>
 </tr>
 <tr>
  <td><p align="center">Image 3</td>
  <td><p align="center">14.333</td>
  <td><p align="center">18.820</td>
 </tr>
 <tr>
  <td><p align="center">Image 4</td>
  <td><p align="center">9.864</td>
  <td><p align="center">22.864</td>
 </tr> 
</table>

<ul>
  <li>After performing the algorithms on different images, we can see that the PSNR values are higher for Double Plateaus Histogram Equalization in all cases.
  <li>Thus, Double Plateaus Histogram Equalization is the best amongst the ones that were used.
</ul>
<h2>Future Scope</h2>
<ul>
  <li>If we are able to perform these algorithms on each frame in a video fast enough, we can get real time video enhancement.
  <li>Applying these algorithms on Night vision goggles can improve the enhancement of images.
</ul>
