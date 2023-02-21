---
layout: pub
tag: research
permalink: /publications/neural-shadow-mapping
featured: true
publication-date: 11-22

short-title: NSM
title: Neural Shadow Mapping
format-title: Neural Shadow Mapping
authors:
    - name: Sayantan Datta
      institution: McGill University
      link: https://sayan1an.github.io/
      internship: True
      mgl-member: True

    - name: Derek Nowrouzezahrai
      institution: McGill University
      link: http://www.cim.mcgill.ca/~derek/
      mgl-member: True

    - name: Christoph Schied
      institution: NVIDIA Research
      link: https://research.nvidia.com/person/christoph-schied

    - name: Zhao Dong
      institution: Reality Labs Research, Meta
      link: http://flycooler.com/

journal: ACM SIGGRAPH '22 Conference Proceedings
journal-note: SIGGRAPH America
location:
    city: Vancouver
    country: Canada
    continent: Americas
spotlight-note:
internship-note: Work done during an internship at Reality Labs Research, Meta <i class="bi bi-meta"></i>
volume: 41
number: 6
article-no: 8
doi: 10.1145/3528233.3530700
month: July
year: 2022

thumbnail: /pubs-assets/2022-datta-neural-shadows/neural-shadows-thumb.png
thumbnail-video:
teaser: /pubs-assets/2022-datta-neural-shadows/neural-shadows-teaser.png
teaser-caption: |
    Our hard and soft shadowing method approaches the quality of offline ray tracing whilst striking a favorable position on the performance-accuracy spectrum. On the high-performance end, we produce higher quality results than <em>n</em>×<em>n</em> Moment Shadow Maps (MSM-<em>n</em>). We require only vanilla shadow mapping inputs to generate visual (and temporal) results that approach ray-traced reference, surpassing more costly denoised interactive ray-traced methods.

abstract: |
    We present a neural extension of basic shadow mapping for fast, high quality hard and soft shadows. We compare favorably to fast pre-filtering shadow mapping, all while producing visual results on par with ray traced hard and soft shadows. We show that combining memory bandwidth-aware architecture specialization and careful temporal-window training leads to a fast, compact and easy-to-train neural shadowing method. Our technique is memory bandwidth conscious, eliminates the need for post-process temporal anti-aliasing or denoising, and supports scenes with dynamic view, emitters and geometry while remaining robust to unseen objects.

acknowledgements: |
    We thank the reviewers for their constructive feedback, the ORCA for the Amazon Lumberyard Bistro model, the Stanford CG Lab for the Bunny, Buddha, and Dragon models, Marko Dabrovic for the Sponza model and Morgan McGuire for the Bistro, Conference and Living Room models. This work was done when Sayantan was an intern at Meta Reality Labs Research. While at McGill University, he was also supported by a Ph.D. scholarship from the <em>Fonds de recherche du Québec – Nature et Technologies (FRQNT)</em>.

downloads:
    published: True
    paper:
        - file: /pubs-assets/2022-datta-neural-shadows/neural-shadows.pdf
          size: 3.5MB
    arxiv:
        url:
    main:
        url: https://sayan1an.github.io/neuralShadowMapping.html
    publisher:
        url: https://dl.acm.org/doi/10.1145/3550454.3555450
    supplementary:
    videos:
        - url: https://www.youtube.com/watch?v=4I-1t72Bylg
          type: Youtube
          size:
          venue: SIGGRAPH Talk
    video-embed: https://www.youtube.com/embed/4I-1t72Bylg
    code:
        published: False
        file:
        size:
        url:

tex: |
    @inproceedings{datta2022nsm,
        author = {Datta, Sayantan and Nowrouzezahrai, Derek and Schied, Christoph and Dong, Zhao},
        title = {Neural Shadow Mapping},
        journal = {ACM SIGGRAPH 2022 Conference Proceedings},
        year = {2022},
        month = july
    }
---
