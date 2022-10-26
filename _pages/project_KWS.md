---
layout: none
title: Metric Learning for User-defined Keyword Spotting
permalink: /kws
description: Benchmarking Background Robustness for Continuous Sign Language Recognition.
keywords: "User-defined keyword spotting, Metric learning"
title: "Metric Learning for User-defined Keyword Spotting"
# venue: British Machine Vision Conference (BMVC 2022)
# pdf: False
# arxiv: False
# code: False
# slide: False
# poster: False
# bibtex: >
#   @inproceedings{jang2022signing, <br />
#   &nbsp;&nbsp; title={Signing Outside the Studio: Benchmarking Background Robustness for Continuous Sign Language Recognition}, <br />
#   &nbsp;&nbsp; author={Jang, Youngjoon and Oh, Youngtaek and Cho, Jae Won and Kim, Dong-Jin and Chung, Joon Son and Kweon, In So}, <br />
#   &nbsp;&nbsp; booktitle={British Machine Vision Conference (BMVC)}, <br />
#   &nbsp;&nbsp; year={2022} <br />
#   }
#   &nbsp;&nbsp; pages={0000-0000} <br />

abstract: >
  <p>
    The goal of this work is to detect new spoken terms defined by users. While most previous works address Keyword Spotting (KWS) as a closed-set classification problem, this limits their transferability to unseen terms. The ability to define custom keywords has advantages in terms of user experience.
  </p>
  <p>
    In this paper, we propose a metric learning-based training strategy for user-defined keyword spotting. In particular, we make the following contributions: (1) We construct a large-scale keyword dataset with an existing speech corpus and propose a filtering method to remove data which degrade a performance of a KWS model. (2) With comprehensive experiments, we prove that metric learning-based pre-training on our dataset, followed by fine-tuning on a smaller in-domain keyword dataset, enriches the KWS model’s representation. (3) For the fair comparison in the KWS field, we propose an unified evaluation protocol and metrics.
  </p>
  <p>
    Our proposed system does not require incremental training on the user-defined keywords, and outperforms previous works by a significant margin on the Google Speech Commands dataset using the proposed as well as the existing metricsminimal additional training images.
  </p>
---


<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="description"
        content="{{ page.description }}">
  <meta name="keywords" content="{{ page.keywords }}">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>{{ page.title }}</title>

  <!-- Global site tag (gtag.js) - Google Analytics -->
  {% include scripts/analytics.html %}
  <!-- mathjax -->
  <script type="text/x-mathjax-config"> 
    MathJax.Hub.Config({ tex2jax: { inlineMath: [ ['$','$'], ["\\(","\\)"] ], processEscapes: true } }); 
  </script>
  <script src='https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.2/MathJax.js?config=TeX-MML-AM_CHTML'></script>
  <!--/ mathjax -->
  <link href="https://fonts.googleapis.com/css?family=Google+Sans|Noto+Sans|Castoro" rel="stylesheet">

  <link rel="stylesheet" href="./assets/nerfies/css/bulma.min.css">
  <link rel="stylesheet" href="./assets/nerfies/css/bulma-carousel.min.css">
  <link rel="stylesheet" href="./assets/nerfies/css/bulma-slider.min.css">
  <link rel="stylesheet" href="./assets/nerfies/css/fontawesome.all.min.css">
  <link rel="stylesheet"
        href="https://cdn.jsdelivr.net/gh/jpswalsh/academicons@1/css/academicons.min.css">
  <link rel="stylesheet" href="./assets/nerfies/css/index.css">

  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
  <script defer src="./assets/nerfies/js/fontawesome.all.min.js"></script>
  <script src="./assets/nerfies/js/bulma-carousel.min.js"></script>
  <script src="./assets/nerfies/js/bulma-slider.min.js"></script>
  <script src="./assets/nerfies/js/index.js"></script>
</head>
<body>

<nav class="navbar" role="navigation" aria-label="main navigation">
  <div class="navbar-brand">
    <a role="button" class="navbar-burger" aria-label="menu" aria-expanded="false">
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
    </a>
  </div>
  <div class="navbar-menu">
    <div class="navbar-start" style="flex-grow: 1; justify-content: center;">
      <a class="navbar-item" href="https://art-jang.github.io">
      <span class="icon">
          <i class="fas fa-home"></i>
      </span>
      </a>
    </div>
  </div>
</nav>

<section class="hero">
  <div class="hero-body">
    <div class="container is-max-desktop">
      <div class="columns is-centered">
        <div class="column has-text-centered">
          <h1 class="title is-3 publication-title">{{ page.title }}</h1>
          <div class="is-size-4 publication-authors">
            <span class="author-block">
              <a href="">Jaemin Jung</a><sup>1</sup>,</span>
            <span class="author-block">
              <a href="">Youkyum Kim</a><sup>1</sup>,</span>
            <span class="author-block">
              <a href="">Jihwan Park</a><sup>2</sup>,</span>
            <span class="author-block">
              <a href="">Youshin Lim</a><sup>2</sup>,</span>
            <span class="author-block">
              <a href="">Byeong-Yeol Kim</a><sup>2</sup>,</span>
            <span class="author-block">
              <a href="https://art-jang.github.io">Youngjoon Jang</a><sup>1</sup>,</span>
            <span class="author-block">
              <a href="https://mm.kaist.ac.kr/joon/">Joon Son Chung</a><sup>1</sup>,</span>
          </div>
          <div class="is-size-5 publication-authors">
            <span class="author-block"><sup>1</sup>KAIST / Daejeon, South Korea.</span>
            <span class="author-block"><sup>2</sup>Hyundai Motor Company / Seoul, South Korea.</span>
          </div>
          <div class="column has-text-centered">
            <div class="publication-links">
              <!-- PDF Link. -->
              {%- if page.pdf %}
              <span class="link-block">
                <a href="{{ page.pdf }}" target="_blank"
                   class="external-link button is-normal is-rounded is-dark">
                  <span class="icon">
                      <i class="fas fa-file-pdf"></i>
                  </span>
                  <span>Paper</span>
                </a>
              </span>
              {%- endif %}
              {%- if page.arxiv %}
              <span class="link-block">
                <a href="{{ page.arxiv }}"
                   class="external-link button is-normal is-rounded is-dark">
                  <span class="icon">
                      <i class="ai ai-arxiv"></i>
                  </span>
                  <span>arXiv</span>
                </a>
              </span>
              {%- endif %}
              {%- if page.video %}
              <!-- Video Link. -->
              <span class="link-block">
                <a href="{{ page.video }}"
                   class="external-link button is-normal is-rounded is-dark">
                  <span class="icon">
                      <i class="fab fa-youtube"></i>
                  </span>
                  <span>Video</span>
                </a>
              </span>
              {%- endif %}
              {%- if page.code %}
              <!-- Code Link. -->
              <span class="link-block">
                <a href="{{ page.code }}"
                   class="external-link button is-normal is-rounded is-dark">
                  <span class="icon">
                      <i class="fab fa-github"></i>
                  </span>
                  <span>Code</span>
                  </a>
              </span>
              {%- endif %}
              {%- if page.slide %}
              <!-- slide Link. -->
              <span class="link-block">
                <a href="{{ page.slide | prepend: '/assets/daso/' }}" target="_blank"
                   class="external-link button is-normal is-rounded is-dark">
                  <span class="icon">
                      <i class="far fa-file-powerpoint"></i>
                  </span>
                  <span>Slides</span>
                  </a>
              </span>
              {%- endif %}
              {%- if page.poster %}
              <!-- poster Link. -->
              <span class="link-block">
                <a href="{{ page.poster | prepend: '/assets/daso/' }}" target="_blank"
                   class="external-link button is-normal is-rounded is-dark">
                  <span class="icon">
                      <i class="fas fa-file-powerpoint"></i>
                  </span>
                  <span>Poster</span>
                  </a>
              </span>
              {%- endif %}
            </div>
          </div>
          <div class="column has-text-centered">
            <div class="is-size-5 publication-authors">
              {{ page.venue }}
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
<!-- project_page.html -->
<section class="hero teaser">
  <div class="container is-max-desktop">
    <div class="hero-body">
      <div class="columns is-centered">
        <div class="column">
          <div class="content">
            <h2 class="title is-3">CAT</h2>
            <img src="assets/KWS/grad_Final_CAT.png"/>
            <audio controls=""><source src="assets/KWS/CAT_9023-296468-0028_1.wav" type="audio/wav"></audio>
          </div>
        </div>
        <div class="column">
          <div class="content">
            <h2 class="title is-3">FIRST</h2>
            <img src="assets/KWS/grad_Final_FIRST.png"/>
            <audio controls=""><source src="assets/KWS/FIRST_737-123448-0014_4.wav" type="audio/wav"></audio>
          </div>
        </div>
        <div class="column">
          <div class="content">
            <h2 class="title is-3">GREAT</h2>
            <img src="assets/KWS/grad_Final_GREAT.png"/>
            <audio controls=""><source src="assets/KWS/GREAT_6399-278844-0007_15.wav" type="audio/wav"></audio>
          </div>
        </div>
      </div>
      <div class="columns is-centered">
        <div class="column">
          <div class="content">
            <h2 class="title is-3">SPEECH</h2>
            <img src="assets/KWS/grad_Final_SPEECH.png"/>
            <audio controls=""><source src="assets/KWS/SPEECH_3285-121401-0034_7.wav" type="audio/wav"></audio>
          </div>
        </div>
        <div class="column">
          <div class="content">
            <h2 class="title is-3">PRINCE</h2>
            <img src="assets/KWS/grad_Final_PRINCE.png"/>
            <audio controls=""><source src="assets/KWS/PRINCE_4487-1803-0023_22.wav" type="audio/wav"></audio>
          </div>
        </div>
        <div class="column">
          <div class="content">
            <h2 class="title is-3">FINGERS</h2>
            <img src="assets/KWS/grad_Final_FINGERS.png"/>
            <audio controls=""><source src="assets/KWS/FINGERS_1748-1562-0042_39.wav" type="audio/wav"></audio>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
<section class="section">
  <div class="container is-max-desktop">
    <!-- Abstract. -->
    <div class="columns is-centered has-text-centered">
      <div class="column is-four-fifths">
        <h2 class="title is-3">Abstract</h2>
        <div class="content has-text-justified">
          {{ page.abstract }}
        </div>
      </div>
    </div>
    <!--/ Abstract. -->
  </div>
</section>

<section class="section">
  <div class="container is-max-desktop">
    <!-- Concurrent Work. -->
    <div class="columns is-centered">
      <div class="column is-full-width">
        <h2 class="title is-3">References</h2>
        <div class="content has-text-justified">
          <p>
            [1] Koller, Oscar, Jens Forster, and Hermann Ney. "Continuous sign language recognition: Towards large vocabulary statistical recognition systems handling multiple signers." Computer Vision and Image Understanding 141 (2015): 108-125.
          </p>
          <p>
            [2] He, Kaiming, et al. "Deep residual learning for image recognition." Proceedings of the IEEE conference on computer vision and pattern recognition. 2016.
          </p>
          <p>
            [3] Min, Yuecong, et al. "Visual alignment constraint for continuous sign language recognition." Proceedings of the IEEE/CVF International Conference on Computer Vision. 2021.
          </p>
          <p>
            [4] Zhang, Hongyi, et al. "mixup: Beyond empirical risk minimization." arXiv preprint arXiv:1710.09412 (2017).
          </p>
          <p>
            [5] Yu, Fisher, et al. "Lsun: Construction of a large-scale image dataset using deep learning with humans in the loop." arXiv preprint arXiv:1506.03365 (2015).
          </p>
          <p>
            [6] Szegedy, Christian, et al. "Going deeper with convolutions." Proceedings of the IEEE conference on computer vision and pattern recognition. 2015.
          </p>
          <!-- <p>
            [6] Selvaraju, Ramprasaath R., et al. "Grad-cam: Visual explanations from deep networks via gradient-based localization." Proceedings of the IEEE international conference on computer vision. 2017.
           </p>-->
        </div>
      </div>
    </div>
  </div>
</section>

{%- if page.bibtex %}
<section class="section" id="BibTeX">
  <div class="container is-max-desktop content">
    <h2 class="title">BibTeX</h2>
    <p>
      If you find our work useful for your research, please cite with the following bibtex:
    </p>
    <pre><code>{{ page.bibtex }}</code></pre>
  </div>
</section>
{%- endif %}

<footer class="footer">
  <div class="container">
    <div class="content has-text-centered">
      {%- if page.pdf %}
      <a class="icon-link"
         href="{{ page.pdf }}">
        <i class="fas fa-file-pdf"></i>
      </a>
      {%- endif %}
      {%- if page.code %}
      <a class="icon-link" href="{{ page.code }}" class="external-link" disabled>
        <i class="fab fa-github"></i>
      </a>
      {%- endif %}
    </div>
    <div class="columns is-centered">
      <div class="column is-8">
        <div class="content">
          <p>This website is based on the <a href="https://github.com/nerfies/nerfies.github.io">Nerfies website template</a>,
            which is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative
            Commons Attribution-ShareAlike 4.0 International License</a>.
          </p>
        </div>
      </div>
    </div>
  </div>
</footer>

</body>
</html>