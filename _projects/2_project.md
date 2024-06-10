---
layout: page
title: CLIP-Branches
description: Interactive Text-Image Search Engine
img: assets/img/clip-branches/Demo3.png
importance: 3
# category: work
# giscus_comments: true
---

The advent of text-image models, most notably CLIP, has significantly transformed the landscape of information retrieval. These models enable the fusion of various modalities, such as text and images. One significant outcome of CLIP is its capability to allow users to search for images using text as a query, as well as vice versa. This is achieved via a joint embedding of images and text data that can, for instance, be used to search for similar items. Despite efficient query processing techniques such as approximate nearest neighbor search, the results may lack precision and completeness. We introduce CLIP-Branches, a novel text-image search engine built upon the CLIP architecture. Our approach enhances traditional text-image search engines by incorporating an interactive fine-tuning phase, which allows the user to further concretize the search query by iteratively defining positive and negative examples. Our framework involves training a classification model given the additional user feedback and essentially outputs all positively classified instances of the entire data catalog. By building upon recent techniques, this inference phase, however, is not implemented by scanning the entire data catalog, but by employing efficient index structures pre-built for the data. Our results show that the fine-tuned results can improve the initial search outputs in terms of relevance and accuracy while maintaining swift response times.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/clip-branches/Demo1.png" title="Text Query" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/clip-branches/Demo2.png" title="Refinement" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/clip-branches/Demo3.png" title="Results" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Demonstration of CLIP-Branches search workflow. The user initiates a search with a query string and receives top k-initial results. These results are then labeled as positive (green) or negative (red) based on user preference, guiding the fine-tuning of the search. The fine-tuned results reflect more completeness and higher accuracy.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/clip-branches/SIGIR_2.png" title="Search Workflow" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Search process of CLIP-Branches. Traditional text-to-image search engines only consist of the steps ❶ to ❸ while CLIP-Branches adds a fine-tuning stage to refine the initial search results (Steps ❹-❼). Index structures are employed during the search for faster execution.
</div>

A demo how to use CLIP-Branches can be found in the following video:

<div class="video-container">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/lepPM3zi0l8" frameborder="0" allowfullscreen></iframe>
</div>


Come on and try it out yourself via the following <a href="https://web.clip-branches.net">link</a>.

## References
<div class="publications">
  {% bibliography -f papers -q @*[key=sigir]* %}
</div>