---
layout: page
title: Graph Neural Networks 
description: For Predicting Molecule Properties
img: assets/img/gnn/MT_2.png
importance: 4
# category: work
# giscus_comments: true
---

Over the last years, deep neural networks (NN) became the de-facto standard in machine learning (ML) for solving nearly every complex learning tasks. While they have found application in areas like natural language processing or image recognition, they are still in its infancy for areas with graph-structured data. Here, the development on graph-based tasks has hesitated in contrast to other areas in ML since typical components from deep neural architectures like convolutions can not directly be utilized on graph data. However, the demand for deep neural-based solutions on graph structures like molecules or networks has never ceased as they are expected to strongly improve the results of currently applied methods.

Inspired by classic NNs, graph neural networks (GNN) were introduced for processing and predicting graph-structured data in neural architectures. By adapting
conventional NN components for the graph domain, GNNs are capable of learning patterns based on the graph structure. Unlike prevalent methods like network or
graph encoders, GNNs not just encode the graph structure into a feature vector but are also making predictions on the data in an end-to-end manner. Thereby, GNN models could outperform benchmark models for graph-data. Due to the rapid growth of published GNN models during the last years, it demands for an overview and categorization of existing approaches to allow for a smooth start into this topic. Moreover, the general overview of prevalent GNN models should be extended with applied models in chemistry, more concretely in quantitative structure-property relationship (QSPR) modeling. In this area, the interest using GNNs for predicting molecular properties is immense. Existing methods like density functional theory (DFT) require huge amounts of time to compute the estimates. The expectation in research is that deep learning architectures based on GNNs can alleviate the computational costs for molecular property prediction while still maintaining a decent accuracy of the results.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/gnn/MT_1.png" title="Search Workflow" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Schematic software architecture of the developed GNN benchmark platform.
</div>