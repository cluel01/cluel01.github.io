---
layout: page
title: HyperNN
description: Neural Network For Learning Hyperboxes
img: assets/img/publication_preview/ESANN.png
importance: 5
# category: work
# related_publications: true
---

Hyperbox-based classification has been seen as a promising technique in which decisions on the data are represented as a series of orthogonal, multidimensional boxes (i.e., hyperboxes) that are often interpretable and human-readable. However, existing methods are no longer capable of efficiently handling the increasing volume of data many application domains face nowadays. We address this gap by proposing a novel, fully differentiable framework for hyperbox-based classification via neural networks. In contrast to previous work, our hyperbox models can be efficiently trained in an end-to-end fashion, which leads to significantly reduced training times and superior classification results.

The code for this project can be found in the following <a href="https://github.com/mlde-ms/hypernn">Github repository</a>.

## References
<div class="publications">
  {% bibliography -f papers -q @*[key=esann]* %}
  {% bibliography -f papers -q @*[key=neurocom]* %}
</div>