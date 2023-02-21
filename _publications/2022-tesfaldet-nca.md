---
layout: pub
tag: research
permalink: /publications/nca
featured: false
publication-date: 12-22

short-title: NCA
title: Attention-based Neural Cellular Automata
format-title:
authors:
    - name: Mattie Tesfaldet
      institution: McGill University & Mila
      link: https://riouxld21.github.io/research
      mgl-member: True

    - name: Derek Nowrouzezahrai
      institution: McGill University & Mila
      link: http://www.cim.mcgill.ca/~derek/
      mgl-member: True

    - name: Christopher Pal
      institution: École Polytechnique de Montréal
      link: https://sites.google.com/view/christopher-pal

journal: Neural Information Processing Systems
journal-note: NeurIPS
location:
    city: New Orleans
    country: USA
    continent: Americas
spotlight-note: Poster
volume:
number:
article-no:
doi: 3550454.3555450
month: December
year: 2022

thumbnail:
thumbnail-video:
teaser:
teaser-caption: 

abstract: |
    Recent extensions of Cellular Automata (CA) have incorporated key ideas from modern deep learning, dramatically extending their capabilities and catalyzing a new family of Neural Cellular Automata (NCA) techniques. Inspired by Transformer-based architectures, our work presents a new class of <em>attention-based</em> NCAs formed using a spatially localized—yet globally organized—self-attention scheme. We introduce an instance of this class named <em>Vision Transformer Cellular Automata (ViTCA)</em>. We present quantitative and qualitative results on denoising autoencoding across six benchmark datasets, comparing ViTCA to a U-Net, a U-Net-based CA baseline (UNetCA), and a Vision Transformer (ViT). When comparing across architectures configured to similar parameter complexity, ViTCA architectures yield superior performance across all benchmarks and for nearly every evaluation metric. We present an ablation study on various architectural configurations of ViTCA, an analysis of its effect on cell states, and an investigation on its inductive biases. Finally, we examine its learned representations via linear probes on its converged cell state hidden representations, yielding, on average, superior results when compared to our U-Net, ViT, and UNetCA baselines.

acknowledgements: 

downloads:
    published: True
    paper:
        - file: nca.pdf
          size: XX.X MB
    arxiv:
        url: https://arxiv.org/abs/2211.01233
    main:
        url: https://openreview.net/forum?id=9t24EBSlZOa
    publisher:
        url: https://neurips.cc/Conferences/2022/ScheduleMultitrack?event=54709
    supplementary:
    slides:
    videos:
    video-embed:
    code:
        published: False
        file:
        size:
        url:

tex: |
    @article{resfaldet202nca,
        author = {Tesfaldet, Matthew and Nowrouzezahrai, Derek and Pal, Christopher},
        title = {Attention-based Neural Cellular Automata},
        journal = {Advances in Neural Information Processing Systems (NeurIPS)},
        year = {2022},
        month = dec
    }
---