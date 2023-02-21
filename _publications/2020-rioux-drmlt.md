---
layout: pub
tag: research
permalink: /publications/drmlt
featured: false
publication-date: 03-20

short-title: DRMLT
title: Delayed Rejection Metropolis Light Transport
format-title: Delayed Rejection Metropolis Light Transport
summary: Applying delayed rejection MCMC to light transport simulation
authors:
    - name: Damien Rioux-Lavoie
      institution: McGill University
      link: https://riouxld21.github.io/research
      joint-first: True
      mgl-member: True

    - name: Joey Litalien
      institution: McGill University
      link: https://joeylitalien.github.io
      joint-first: True
      mgl-member: True

    - name: Adrien Gruson
      institution: McGill University
      link: https://profs.etsmtl.ca/agruson/
      mgl-member: True

    - name: Toshiya Hachisuka
      institution: The University of Tokyo
      link: https://cs.uwaterloo.ca/~thachisu/

    - name: Derek Nowrouzezahrai
      institution: McGill University
      link: http://www.cim.mcgill.ca/~derek/
      mgl-member: True

journal: ACM Transactions on Graphics (TOG)
journal-note: SIGGRAPH America
location:
    city: Los Angeles
    country: USA 
    continent: Remote
volume: 39
number: 3
article-no: 26
doi: 10.1145/3388538
month: May
year: 2020

thumbnail: /pubs-assets/2020-rioux-drmlt/drmlt-thumb.png
teaser: /pubs-assets/2020-rioux-drmlt/drmlt-teaser.png
teaser-caption: |
    We generalize the Metropolis–Hastings algorithm with delayed rejection: our <em>delayed rejection Metropolis light transport</em> (DRMLT) method selectively applies different mutation strategies, improving upon one-stage primary sample space algorithms, i.e., PSSMLT with Gaussian proposals (PSSMLT / G) and H2MC. One variant of our method first attempts an isotropic Gaussian proposal, resorting to more intricate kernels (that improve local exploration with differential information) only when the first attempt failed, e.g., on rough dielectrics. DRMLT focuses computations in hard-to-explore regions without compromising quality in comparatively simpler regions (e.g., on the board). We visualize a per-pixel relative second-stage acceptance, where violet and yellow extremes respectively indicate the efficiency of the first and second stages.

abstract: |
    Designing robust mutation strategies for primary sample space Metropolis light transport is a challenging problem: poorly-tuned mutations both hinder state space exploration and introduce structured image artifacts. Scenes with complex materials, lighting and geometry make hand-designing strategies that remain optimal over the entire state space infeasible. Moreover, these difficult regions are often sparse in state space, and so relying exclusively on intricate—and often expensive—proposal mechanisms can be wasteful where simpler inexpensive mechanisms are more sample efficient. We generalize Metropolis–Hastings light transport to employ a flexible two-stage mutation strategy based on delayed rejection Markov chain Monte Carlo. Our approach generates multiple proposals based on the failure of previous ones, all while preserving Markov chain ergodicity. This allows us to reduce error while maintaining fast global exploration and low correlation across chains. Direct application of delayed rejection to light transport leads to low acceptance probabilities, and so we also propose a novel transition kernel to alleviate this issue. We benchmark our approach on several applications including <em>bold-then-timid</em> and <em>cheap-then-expensive</em> proposals across different light transport algorithms. Our method is applicable to any primary sample space algorithm with minimal implementation effort, producing consistently better results on a variety of challenging scenes.

acknowledgements: |
    Computing resources were provided by the National Systems of Compute Canada. This research was partially funded by the Natural Sciences and Engineering Council of Canada (RGPIN-2018-05669) and the Japan Society for the Promotion of Science KAKENHI (18KK0309).

downloads:
    published: True
    paper:
        - file: /assets/drmlt/drmlt.pdf
          size: 21.5MB
    publisher:
        url: https://dl.acm.org/doi/abs/10.1145/3388538
    supplementary:
        - url: http://adrien-gruson.com/research/2020_DRMLT/drmlt-supplemental.zip
          type: ZIP
          size: 185MB
        - url: http://adrien-gruson.com/research/2020_DRMLT
          type: HTML
    slides:
    videos:
        - url: https://www.youtube.com/watch?v=m22d-cTcubc
          type: Youtube
          size:
          venue: SIGGRAPH Talk
    video-embed: https://www.youtube.com/embed/m22d-cTcubc
    code:
        published: True
        file:
        size:
        url: https://github.com/joeylitalien/drmlt

tex: |
    @article{riouxlavoie2020drmlt,
        author = {Rioux-Lavoie, Damien and Litalien, Joey and Gruson, Adrien and Hachisuka, Toshiya and Nowrouzezahrai, Derek},
        title = {Delayed Rejection {Metropolis} Light Transport},
        journal = {ACM Transactions on Graphics},
        volume = {39},
        number = {3},
        year = {2020},
        month = may
    }
---
