---
layout: pub
tag: research
permalink: /publications/mc-fluid
featured: false
publication-date: 11-22

short-title: MC-Fluid
title: A Monte Carlo Method for Fluid Simulation
format-title: A Monte Carlo Method for Fluid Simulation
authors:
    - name: Damien Rioux-Lavoie
      institution: McGill University
      link: https://riouxld21.github.io/research
      joint-first: True
      mgl-member: True

    - name: Ryusuke Sugimoto
      institution: University of Waterloo
      link: https://rsugimoto.net/
      joint-first: True

    - name: Tümay Özdemir
      institution: University of Waterloo
      link: 

    - name: Naoharu H. Shimada
      institution: Osaka University
      link: https://n-h-shimada.github.io/

    - name: Christopher Batty
      institution: University of Waterloo
      link: https://cs.uwaterloo.ca/~c2batty/

    - name: Derek Nowrouzezahrai
      institution: McGill University
      link: http://www.cim.mcgill.ca/~derek/
      mgl-member: True

    - name: Toshiya Hachisuka
      institution: University of Waterloo
      link: https://cs.uwaterloo.ca/~thachisu/

journal: ACM Transactions on Graphics
journal-note: SIGGRAPH Asia
location:
    city: Daegu
    country: South Korea
    continent: Asia
spotlight-note:
volume: 41
number: 6
article-no: 240
doi: 3550454.3555450
month: November
year: 2022

thumbnail: /pubs-assets/2022-rioux-mcfluid/mcfluid-thumb.png
thumbnail-video:
teaser: /pubs-assets/2022-rioux-mcfluid/mcfluid-teaser.png
teaser-caption: |
    We simulate two leapfrogging vortex rings (top) with a cross section visualization to illustrate the interior flow. We passively advect constant density fields toward closed mesh (middle) and triangle soup Stanford bunnies (bottom). We render all simulations with Blender’s principled volume shader.

abstract: |
    We present a novel Monte Carlo-based fluid simulation approach capable of pointwise and stochastic estimation of fluid motion. Drawing on the Feynman-Kac representation of the vorticity transport equation, we propose a recursive Monte Carlo estimator of the Biot-Savart law and extend it with a stream function formulation that allows us to treat free-slip boundary conditions using a Walk-on-Spheres algorithm. Inspired by the Monte Carlo literature in rendering, we design and compare variance reduction schemes suited to a fluid simulation context for the first time, show its applicability to complex boundary settings, and detail a simple and practical implementation with temporal grid caching. We validate the correctness of our approach via quantitative and qualitative evaluations – across a range of settings and domain geometries – and thoroughly explore its parameters’ design space. Finally, we provide an in-depth discussion of several axes of future work building on this new numerical simulation modality.

acknowledgements: 

downloads:
    published: True
    paper:
        - file: /pubs-assets/2022-rioux-mcfluid/mcfluid.pdf
          size: 13.8MB
    arxiv:
        url:
    main:
        url: https://riouxld21.github.io/research/publication/2022-mcfluid/
    publisher:
        url: https://dl.acm.org/doi/10.1145/3550454.3555450
    supplementary:
    slides:
    videos:
    video-embed:
    code:
        published: False
        file:
        size:
        url:
    bibtex:
        file: /pubs-assets/2022-rioux-mcfluid/mcfluid.bib
        size: 0.5KB

tex: |
    @article{riouxlavoie2022mcfluid,
        author = {Rioux-Lavoie, Damien and Sugimoto, Ryusuke and \"{O}zdemir, T\"{u}may and Shimada, Naoharu H. and 
                  Batty, Christopher and Nowrouzezahrai, Derek and Hachisuka, Toshiya},
        title = {A Monte Carlo Method for Fluid Simulation},
        journal = {ACM Transactions on Graphics},
        volume = {41},
        number = {6},
        year = {2022},
        month = dec
    }
---