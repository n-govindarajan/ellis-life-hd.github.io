---
layout: post
title: "ELLIS Life / Data Science Seminar: Dmitry Kobak"
event_title: "Neighbour Embeddings for Scientific Visualization"
event_subtitle: "How do the existing algorithms differ and what are the trade-offs?"
event_person: "Dmitry Kobak, University of Tübingen"
event_time: "June 16, 11:00 AM (CEST)"
poster: ELSS_20210616_Kobak_poster.png
link: https://us02web.zoom.us/meeting/register/tZYocuipqzgtHtY7eRgvuAGdaowriXHygMlA
---

### Abstract

I am going to present our recent work on manifold learning and low-dimensional visualizations of single-cell transcriptomic data. Single-cell transcriptomics yields ever growing datasets containing RNA expression levels for thousands of genes from up to millions of cells, often exhibiting rich hierarchical structure, both continuous and discrete. Common data analysis pipelines include dimensionality reduction for visualising the data in two dimensions, most frequently performed using methods like t-SNE, UMAP, and ForceAtlas2. These methods are all examples of _neighbour embeddings_: their aim is to keep similar cells as neighbours in the embedding. The most established algorithm, t-SNE, excels at revealing local structure in high-dimensional data, but often struggles to represent the global structure accurately. I will discuss how much this applies to other neighbor embedding algorithms. I will show that changing the balance between the attractive and the repulsive forces yields a spectrum of embeddings, characterized by a simple trade-off: stronger attraction can better represent continuous manifold structures, while stronger repulsion can better represent discrete cluster structures. I will demonstrate that prominent neighbor embedding algorithms can all be placed onto this attraction-repulsion spectrum. I will elucidate other trade-offs, such as revealing coarser or finer cluster structure depending on the shape of the similarity kernel. Furthermore, I will demonstrate the influence of optimization parameters such as the learning rate and the initialization on the resulting embeddings. I will also discuss how to construct two-dimensional embeddings of other kinds of data, including library data and image data.

### Biosketch

Dmitry Kobak studied computer science and physics in St. Petersburg, Russia. He did PhD in computational neuroscience between Freiburg, Germany, and Imperial College London, UK, before moving to the Champalimaud Institute in Portugal for his postdoc. His interests gradually shifted towards data science and machine learning, and since 2017 he is working in the University of Tübingen, Germany, on data analysis of single-cell transcriptomic data. He is fascinated by manifold learning and dimensionality reduction, and is obsessed with figuring out how exactly various machine learning methods work.

Website: [https://dkobak.github.io](https://dkobak.github.io).