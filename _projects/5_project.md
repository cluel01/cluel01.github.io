---
layout: page
title: Decision Branches
description: Novel Machine Learning Model For Efficient Search
img: assets/img/publication_preview/VLDB.png
importance: 1
# category: work
# related_publications: true
---
The vast amounts of data collected in various domains pose great challenges to modern data exploration and analysis. To find "interesting" objects in large databases, users typically define a query using positive and negative example objects and train a classification model to identify the objects of interest in the entire data catalog. However, this approach requires a scan of all the data to apply the classification model to each instance in the data catalog, making this method prohibitively expensive to be employed in large-scale databases serving many users and queries interactively. In this work, we propose a novel framework for such search-by-classification scenarios that allows users to interactively search for target objects by specifying queries through a small set of positive and negative examples. Unlike previous approaches, our framework can rapidly answer such queries at low cost without scanning the entire database. Our framework is based on an index-aware construction scheme for decision trees and random forests that transforms the inference phase of these classification models into a set of range queries, which in turn can be efficiently executed by leveraging multidimensional indexing structures. Our experiments show that queries over large data catalogs with hundreds of millions of objects can be processed in a few seconds using a single server, compared to hours needed by classical scanning-based approaches.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/decisionbranches/VLDB_Framework.png" title="Framework" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Our search-by-classification framework accelerates data retrieval by utilizing an index-aware classifier and pre-built indexes. The classifier leverages efficient range queries on the indexes, eliminating the need for time-consuming full data scans.
</div>

The construction algorithm of our machine learning model is based on two stages. The first stage is the initialization phase, where minimal boxes are constructed that are grown from a random positive trainig sample. The second stage is the expansion phase, where the boundaries of the boxes are expanded to cover more positive training samples by minimizing an impurity measure similar to a decision tree. The final model is a set of hyperboxes that can be used to classify unseen data points.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/decisionbranches/VLDB_Init.png" title="Init" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Initialization phase. The hyperboxes are grown from a random positive training sample.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/publication_preview/VLDB.png" title="Expansion" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Expansion phase. The boundaries of the hyperboxes are expanded to cover more positive training samples.
</div>
<!-- <div class="caption">
    This image can also have a caption. It's like magic.
</div> -->

The code for this project can be found in the following <a href="https://github.com/decisionbranches/decisionbranches">Github repository</a>.

## References
<div class="publications">
  {% bibliography -f papers -q @*[key=vldb]* %}
</div>