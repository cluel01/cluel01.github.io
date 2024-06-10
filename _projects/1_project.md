---
layout: page
title: RapidEarth
description: A Geospatial Searchengine
img: assets/img/rapidearth/search_engine1.png
importance: 2
# category: work
# related_publications: true
---
Data exploration and analysis in various domains often necessitate the search for specific objects in massive databases. A common search strategy, often known as search-by-classification, resorts to training machine learning models on small sets of positive and negative samples and to performing inference on the entire database to discover additional objects of interest. While such an approach often yields very good results in terms of classification performance, the entire database usually needs to be scanned, a process that can easily take several hours even for medium-sized data catalogs. In this work, we present RapidEarth, a geospatial search-by-classification engine that allows analysts to rapidly search for interesting objects in very large data collections of satellite imagery in a matter of seconds, without the need to scan the entire data catalog. RapidEarth embodies a co-design of multidimensional indexing structures and decision branches, a recently proposed variant of classical decision trees. These decision branches allow RapidEarth to transform the inference phase into a set of range queries, which can be efficiently processed by leveraging the  forementioned multidimensional indexing structures. The main contribution of this work is a geospatial search engine that implements these technical findings.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/rapidearth/search_engine4.png" title="Define Query" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/rapidearth/search_engine2.png" title="Search Results" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Visual search interface of RapidEarth. Left: User query is defined by selecting positive (red) and negative (blue) patches that resemble the query set. Right: Visualization of query results, where yellow patches correspond to the found patches that fit the query and green patches are found objects that were also part of the query set.
</div>


The results of the entire dataset can be inspected by navigating over the map:

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/rapidearth/search_engine3.png" title="Results on Map" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<!-- <div class="caption">
    This image can also have a caption. It's like magic.
</div> -->


A demo how to use RapidEarth can be found in the following video:

<div class="video-container">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/jwS96I1qhU8" frameborder="0" allowfullscreen></iframe>
</div>


Come on and try it out yourself via the following <a href="https://web.rapid.earth">link</a>.

## References
<div class="publications">
  {% bibliography -f papers -q @*[key=sigspatial]* %}
</div>