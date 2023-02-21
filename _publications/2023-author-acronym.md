---
# --- METADATA ---
layout: pub # Do not change
tag: research # Do not change
permalink: /publications/example # Paper URL; keep it concise, e.g., paper acronym
featured: false # If true, will be featured on home page
publication-date: 02-23 # MM-YY; for filtering purposes

# --- PAPER INFORMATION ---
title: My paper title
format-title: # This is helpful for long titles; will be broken down according to syntax for paper webpage; e.g., My very <br> long paper title
authors:
    - name: First Last
      institution: McGill University
      link: # Author's website; if none, put Google Scholar or LinkedIn
      joint-first: True # If true, will include a note for equal contribution
      mgl-member: True # Set to true if author is a member of the MGL; will underline authors in formatting to highlight contrib
      internship: True # If true, will include internship-note (see below)

    - name: First Last
      institution: Massachussets Institute of Technology
      link: #
      joint-first: True

    - name: First Last
      institution: Princeton University
      link: https://www.princeton.edu/

    - name: Derek Nowrouzezahrai
      institution: McGill University
      link: https://www.cim.mcgill.ca/~derek/
      mgl-member: True

journal: Journal name
journal-note: Journal note # e.g., SIGGRAPH Asia; leave empty if none
volume: # Leave empty if not provided by publisher
number:
article-no:
doi: XXX.XXX
month: Month
year: 2023

# --- CONFERENCE INFORMATION & NOTES ---
location:
  city: Los Angeles
  country: USA # Country; look up https://icons8.com/icon/set/flags/color (Flags of countries) for correct spelling; it will include a country icon
  continent: Americas # For America, write "Americas"; if remote, write "Remote"

# --- NOTES ---
spotlight-note: Spotlight # e.g., Poster, Oral, Spotlight
internship-note: Work done during an internship at Company Y <i class="bi bi-nvidia"></i> # Mention internship work, if paper was done in collaboration with industry; check https://icons.getbootstrap.com/ for possible icons
award-note: Best Paper Award # Include paper award, if it exists

# --- THUMBNAIL, TEASER & ABSTRACT ---
thumbnail: http://placehold.it/400x400 # Paper thumbnail; must be square dimension; named /pubs-assets/YYYY-author-acronym/acronym-thumb.png
teaser: http://placehold.it/1200x400 # Paper teaser; any dimensions; named /pubs-assets/YYYY-author-acronym/acronym-teaser.png; optional
teaser-caption: |
    This is a caption for the teaser. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin condimentum vehicula sapien, eu ullamcorper sapien aliquet nec. Aliquam a laoreet enim. Donec eget odio vitae orci euismod cursus. Nam imperdiet elit id urna congue suscipit. Nulla facilisi. 
abstract: |
    This is my abstract. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin condimentum vehicula sapien, eu ullamcorper sapien aliquet nec. Aliquam a laoreet enim. Donec eget odio vitae orci euismod cursus. Nam imperdiet elit id urna congue suscipit. Nulla facilisi. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae; Nunc molestie rhoncus erat, id finibus leo viverra ut. Quisque eleifend leo vel diam fringilla, auctor rhoncus nulla lacinia. Pellentesque porttitor porttitor dictum. Aenean ex dolor, vehicula vitae pulvinar sed, scelerisque nec velit. Cras feugiat sodales mauris non tincidunt. Integer non magna sit amet ipsum convallis porttitor. Suspendisse vel tellus augue. Vivamus sed viverra nisi, id placerat sem. Suspendisse faucibus enim libero, a interdum lectus tempus a. Mauris venenatis pretium euismod.
acknowledgements: |
    These are acknowledgements. Pellentesque porttitor porttitor dictum. Aenean ex dolor, vehicula vitae pulvinar sed, scelerisque nec velit. Cras feugiat sodales mauris non tincidunt. Integer non magna sit amet ipsum convallis porttitor. Suspendisse vel tellus augue. Vivamus sed viverra nisi, id placerat sem. Suspendisse faucibus enim libero, a interdum lectus tempus a. Mauris venenatis pretium euismod.

# --- DOWNLOADS & MEDIA ---
downloads:
    published: True # If false, webpage will exist without any download links; useful for preprints
    paper:
        - file: /pubs-assets/YYYY-author-acronym/acronym.pdf
          type: High-res
          size: XX.X MB # Specify paper size
        - file: /pubs-assets/YYYY-author-acronym/acronym-lowres.pdf
          type: Low-res
          size: XX.X MB # Specify paper size
    arxiv:
        url: https://arxiv.org/list/cs.GR/recent # Link to paper arXiv, if it exists
    main:
        url: https://my-paper.html # Link to author's paper website, if it exists
    publisher:
        url: https://dl.acm.org/doi/XXX.XXXX # Link to official paper website (e.g., ACM Digital Library)
    supplementary:
        - url: supplementary.pdf # Link supplementary
          type: PDF
          size: XX.X MB
        - url: supplementary.zip
          type: ZIP
          size: XX.X MB
        - url: webpage.html
          type: HTML
    slides:
        - file: slides.pdf 
          type: PDF
          size: XX.X MB
        - file: slides.ppt 
          type: Powerpoint
          size: XX.X MB
        - file: slides.key 
          type: Keynote
          size: XX.X MB
    videos: # Can be local file, or link to online video (e.g., YouTube)
        - url: video.mp4
          type: MP4
          size: XX.X MB
        - url: https://youtube.com
          type: Youtube
          size: # Leave empty
          venue: Colloquium # Mention location of video recording, e.g., if it's a talk 
    code:
        published: True # Only set to true if code has been released somewhere
        file: codebase.zip # If .zip, link here
        type: ZIP
        size: XX.X MB # Along with its size
        url: https://github.com/mgl/codebase # Link to GitHub repository

# --- BIBTEX CITATION ---
# Formatted BibTeX (ready to copy-paste into .bib); only include relevant info (no abstract, city, etc.); see example below
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