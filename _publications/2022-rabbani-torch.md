---
layout: pub
tag: research
permalink: /publications/torch
featured: false
publication-date: 07-22

short-title: CPF
title: Compact Poisson Filters for Fast Fluid Simulation
format-title: 
authors:
    - name: Amir Hossein Rabbani
      institution: Ubisoft Montreal
      link: https://www.shahinrabbani.ca/
      
    - name: Jean-Philippe Guertin
      institution: Ubisoft Montreal
      link: https://jpg.sh/

    - name: Damien Rioux-Lavoie
      institution: McGill University & Ubisoft Montreal
      link: https://riouxld21.github.io/research
      mgl-member: True
      internship: True
      
    - name: Arnaud Schoentgen
      institution: Ubisoft Montreal
      link: http://arnaud-schoentgen.com/

    - name: Kaitai Tong
      institution: University of British Columbia & Ubisoft Montreal
      link: http://ktai.ca/

    - name: Alexandre Siroix-Vigneux
      institution: McGill University & Ubisoft Montreal
      link: http://www.alexandresiroisvigneux.com/
      mgl-member: True
      internship: True

    - name: Derek Nowrouzezahrai
      institution: McGill University
      link: http://www.cim.mcgill.ca/~derek/
      mgl-member: True

journal: ACM SIGGRAPH '22 Conference Proceedings
journal-note: SIGGRAPH America
location:
    city: Vancouver
    country: Canada
    continent: Americas
spotlight-note:
internship-note: Work done during an internship at Ubisoft LaForge <i class="bi bi-controller"></i>
volume:
number:
article-no: 35
doi: 10.1145/3528233.3530737
month: July
year: 2022

thumbnail: /pubs-assets/2022-rabbani-torch/torch-thumbnail.png
thumbnail-video:
teaser: /pubs-assets/2022-rabbani-torch/torch-teaser.png
teaser-caption: |
    Rocket (top left) illustrates large scale smoke and fire and BurningMan (bottom left) showcases a complex usercontrolled dynamic scene: our Poisson filter solver enforces incompressibility at interactive rates. Right: 50th-order inverse Poisson kernel, its first four rank terms and associated convolution filters.

abstract: |
    Poisson equations appear in many graphics settings including, but not limited to, physics-based fluid simulation. Numerical solvers for such problems strike context-specific memory, performance, stability and accuracy trade-offs. We propose a new Poisson filter-based solver that balances between the strengths of spectral and iterative methods. We derive universal Poisson kernels for forward and inverse Poisson problems, leveraging careful adaptive filter truncation to localize their extent, all while maintaining stability and accuracy. Iterative composition of our compact filters improves solver iteration time by orders-of-magnitude compared to optimized linear methods. While motivated by spectral formulations, we overcome important limitations of spectral methods while retaining many of their desirable properties. We focus on the application of our method to high-performance and high-fidelity fluid simulation, but we also demonstrate its broader applicability.

acknowledgements:

downloads:
    published: True
    paper:
        - file: /pubs-assets/2022-rabbani-torch/torch.pdf
          size: 19.3 MB
    arxiv:
        url:
    main:
        url: https://riouxld21.github.io/research/publication/2022-torch/
    publisher:
        url: https://dl.acm.org/doi/10.1145/3528233.3530737
    supplementary:
        - url: https://www.shahinrabbani.ca/uploads/8/9/0/5/89055470/supplementary.pdf
          type:
          size:
    slides:
        file:
        size:
        file-key:
        size-key:
    videos:
    video-embed:
    code:
        published: True
        file:
        size:
        url: https://github.com/Ubisoft-LaForge/CompactPoissonFilters
    bibtex:
        file:
        size:

tex: |
    @inproceedings{rabbani2022torch,
        author = {Rabbani, Amir Hossein and Guertin, Jean-Philippe and Rioux-Lavoie, Damien and Schoentgen, Arnaud and 
                  Tong, Kaitai and Siroix-Vigneux, Alexandre and Nowrouzezahrai, Derek},
        title = {Neural Shadow Mapping},
        journal = {ACM SIGGRAPH 2022 Conference Proceedings},
        year = {2022},
        month = july
    }
---
