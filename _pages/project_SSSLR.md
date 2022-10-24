---
layout: none
title: Self-Sufficient Framework for Sign Language Recognition
permalink: /ssslr
description: Self-Sufficient Framework for Sign Language Recognition.
keywords: "Sign language recognition, Pseudo-labels, Vision and language"
title: "Self-Sufficient Framework for Sign Language Recognition"
# venue: False
# pdf: False
# arxiv: False
# code: False
# slide: False
# poster: False
# bibtex: >
#   @inproceedings{oh2022daso, <br />
#   &nbsp;&nbsp; title={DASO: Distribution-Aware Semantics-Oriented Pseudo-label for Imbalanced Semi-Supervised Learning}, <br />
#   &nbsp;&nbsp; author={Oh, Youngtaek and Kim, Dong-Jin and Kweon, In So}, <br />
#   &nbsp;&nbsp; booktitle={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)}, <br />
#   &nbsp;&nbsp; year={2022}, <br />
#   &nbsp;&nbsp; pages={9786-9796} <br />
#   }
abstract: >
  <p>
    The goal of this work is to devise a self-sufficient framework for Continuous Sign Language Recognition (CSLR) that addresses the issues of sign language recognition,  including (1) the demand for complex features such as hands, face, and mouth for understanding and (2) the absence of frame level annotations.
  </p>
  <p>
    To this end, we propose (1) Divide and Focus Convolution (DFConv) which extracts both manual and non-manual features without additional networks or annotations and (2) Dense Pseudo-Label Refinement (DPLR) which propagates non-spiky frame-level pseudo-labels by combining the ground truth gloss sequence label with the predicted sequence.
  </p>
  <p>
    We demonstrate that our model achieves state-of-the-art performance among RGB-based methods experimentally on large-scale CSLR benchmarks, PHOENIX-2014 and PHOENIX-2014-T, while showing comparable results with better efficiency compared to the other approaches that use multi-modality or extra annotations.
  </p>
---


<!-- <!DOCTYPE html> -->
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
              <a href="https://art-jang.github.io">Youngjoon Jang</a><sup>1</sup>,</span>
            <span class="author-block">
              <a href="https://ytaek-oh.github.io">Youngtaek Oh</a><sup>1</sup>,</span>
            <span class="author-block">
              <a href="https://chojw.github.io/">Jae Won Cho</a><sup>1</sup>,</span>
            <span class="author-block">
              <a href="">Myungchul Kim</a><sup>1</sup>,</span>
            <span class="author-block">
              <a href="https://sites.google.com/site/djkimcv/">Dong-Jin Kim</a><sup>2</sup>,</span>
            <span class="author-block">
              <a href="https://scholar.google.com/citations?user=XA8EOlEAAAAJ&hl=ko">In So Kweon</a><sup>1</sup>,</span>
            <span class="author-block">
              <a href="https://mm.kaist.ac.kr/joon/">Joon Son Chung</a><sup>1</sup>,</span>
          </div>
          <div class="is-size-5 publication-authors">
            <span class="author-block"><sup>1</sup>KAIST / Daejeon, South Korea.</span>
            <span class="author-block"><sup>2</sup>Hanyang University / Seoul, South Korea.</span>
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
      <video id="teaser" autoplay muted loop playsinline height="100%">
        <source src="assets/ssslr/ssslr_demo.mp4" type="video/mp4">
      </video>
      <h2 class="subtitle has-text-centered is-size-5">
        Our framework is intended to train sign language recognition models without additional annotations. Our model trained on weekly-labeled sign language datasets shows better or comparable performance compared to other methods using multiple modalities or additional knowledge.
      </h2>
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

<!-- Results -->
<section class="section">
  <div class="container is-max-desktop">
    <div class="columns is-centered">
      <div class="column is-full-width">
        <h2 class="title is-3">Additional Experiments</h2> 
        <div class="content has-text-justified">
          <p>
            We show more experimental results to support our framework's novelty. 
          </p>
        </div>
        <!-- same imbalance -->
        <h3 class="title is-5">Robustness Comparison</h3>
        <div class="content has-text-justified">
          <p class="mb-4">
            We show our framework's the robustness in a real world scenario by chainging scale and translation during the inference time. Futhermore, we show the failure cases of pose-detector in STMC [1], where the transformation (scale, translation) are adapted. Note that our framework requires only RGB modality.
          </p>
          <div class="columns is-centered">
            <div class="column is-7">
              <img src="assets/ssslr/robustness.png"/>
            </div>
          </div>
          <div class="columns is-centered">
            <div class="column is-7">
              <img src="assets/ssslr/robustness_results.png"/>
            </div>
          </div>
        </div>
        <!-- different imbalance -->
        <h3 class="title is-5">Efficiency Analysis</h3>
        <div class="content has-text-justified">
          <p class="mb-4">
            We compare the computational complexity with the most recent multi-cue based method, STMC. Even though the pose detector of STMC is light-weight, it still induces the bottleneck in the inference time. We highlight that DFConv significantly reduces both FLOPs and inference time by pulling out the pose estimator. For reference, in out environment, extracting human keypoints with HRNet [2] from PHOENIX-2014 dataset [3] takes 2-3 GPU days. Note that we implement STMC due to the absence of the code.
          </p>
        </div>
        <div class="hero-body">
          <div class="columns is-centered">
            <div class="column is-6">
              <img src="assets/ssslr/efficiency.png"/>
            </div>
          </div>
          <h2 class="subtitle has-text-centered">
            Comparison of computational cost and inference time with STMC. (*): we directly take the reported results in the original STMC paper.
          </h2>
        </div>
        <!-- different imbalance -->
        <h3 class="title is-5">Generality of DPLR</h3>
        <div class="content has-text-justified">
          <p class="mb-4">
            To demonstrate the wide applicability of DPLR, we compare DPLR with other CSLR approaches using pseudo-labeling.
          </p>
        </div>
        <div class="hero-body">
          <div class="columns is-centered">
            <div class="column is-6">
              <img src="assets/ssslr/generality.png"/>
            </div>
          </div>
          <h2 class="subtitle has-text-centered">
             Specifically, we consider FCN [4] and VAC [5], and replace the GFE and VA modules corresponding to the pseudo-labeling modules of each method with our DPLR module. For both methods, DPLR shows superior  erformance compared to previous pseudo-labeling modules: GFE and VA . Moreover, we highlight that DPLR further boosts the full version of VAC, achieving the WER of 21.6% in the Test split. This indicates that DPLR is complementary to the VA module in VAC. 
          </h2>
        </div>
      </div>
    </div>
  </div>
</section>
<!--/ Results -->

<!-- Analysis -->
<section class="section">
  <div class="container is-max-desktop">
    <div class="columns is-centered">
      <div class="column is-full-width">
        <h2 class="title is-3">Additional Qualitative Results</h2> 
        <div class="content has-text-justified">
          <p>
            We visualize more qualitative examples.
          </p>
        </div>
        <!-- same imbalance -->
        <h3 class="title is-5">Divide and Focus Convolution</h3>
        <div class="hero-body">
          <div class="columns is-centered">
            <div class="column is-11">
              <img src="assets/ssslr/dfconv.png"/>
            </div>
          </div>
          <h2 class="subtitle has-text-centered">
            The comparison of GradCAM [6] activation maps between Ours and VGG-11 backbone network. DFConv better highlights multiple individual elements (hands, faces) across the entire image area whereas VGG-11 [7] simply attends to only hands.
          </h2>
        </div>
        <!-- different imbalance -->
        <h3 class="title is-5">Gloss-level Sequence Prediction</h3>
        <div class="content has-text-justified">
          <p>
            To explain the effectiveness of DPLR, we show more qualitative results of gloss-level sequence predictions. Note that the extra network is not required for the Dense Pseudo-Labels (DPL), and as the classifier for DPLR is an auxiliary, it does not affect on the inference time, which is important factor to satisfy real-time operation.
          </p>
        </div>
        <div class="hero-body">
          <div class="columns is-centered">
            <div class="column is-12">
              <img src="assets/ssslr/qualitative.png"/>
            </div>
          </div>
          <h2 class="subtitle has-text-centered">
            Qualitative results of the predicted gloss sequences on the PHOENIX-2014 Test split. Each color blocks represent different glosses, and the hirizontal axis is the time axis.
          </h2>
        </div>
      </div>
    </div>
  </div>
</section>
<!--/ Analysis -->


<!-- Analysis -->
<section class="section">
  <div class="container is-max-desktop">
    <div class="columns is-centered">
      <div class="column is-full-width">
        <h2 class="title is-3">Additional Discussion</h2> 
        <!-- same imbalance -->
        <h3 class="title is-5">Potential Societal Impact</h3>
        <div class="content has-text-justified">
          <p>
            Our proposed solution directly contributes to the development of a sign translation system by providing high-quality multi-cue aware visual features to modern sign translation models. Advanced sign interpretation technologies could help socially marginalized deaf people and improve accessibility in social infrastructures such as education and health, which hearing people take for granted. However, current available large-scale PHOENIX/T benchmarks, which are sourced in a specific domain (e.g., weather forecast) could bias the model towards the certain scenario in language and visual appearance, leading to potential miscommunication, which could affect the lives deaf people.
          </p>
        </div>
        <h3 class="title is-5">Limitation and Future Work</h3>
        <div class="content has-text-justified">
          <p>
            Although we have shown that both non-manual and manual expressions are simultaneously captured from a sign video, the limitation of our work would come from the assumption that non-manual expressions occur in upper region of a frame, and vice versa for the manual expressions. While we address the issue by introducing the adaptability of the division ratio r at test time, not only the position, but also variations in scale of the signer (e.g. due to distance from camera) could be introduced in practical scenarios. Future CSLR works should embrace such practical challenges so that the recognition system can be deployed in the real world with ease. 
          </p>
        </div>
      </div>
    </div>
  </div>
</section>
<!--/ Analysis -->

<section class="section">
  <div class="container is-max-desktop">
    <!-- Concurrent Work. -->
    <div class="columns is-centered">
      <div class="column is-full-width">
        <h2 class="title is-3">References</h2>
        <div class="content has-text-justified">
          <p>
            [1] Zhou, Hao, et al. "Spatial-temporal multi-cue network for continuous sign language recognition." Proceedings of the AAAI Conference on Artificial Intelligence. Vol. 34. No. 07. 2020.
          </p>
          <p>
            [2] Sun, Ke, et al. "Deep high-resolution representation learning for human pose estimation." Proceedings of the IEEE/CVF conference on computer vision and pattern recognition. 2019
          </p>
          <p>
            [3] Koller, Oscar, Jens Forster, and Hermann Ney. "Continuous sign language recognition: Towards large vocabulary statistical recognition systems handling multiple signers." Computer Vision and Image Understanding 141 (2015): 108-125.
          </p>
          <p>
            [4] Cheng, Ka Leong, et al. "Fully convolutional networks for continuous sign language recognition." European Conference on Computer Vision. Springer, Cham, 2020.
          </p>
          <p>
            [5] Min, Yuecong, et al. "Visual alignment constraint for continuous sign language recognition." Proceedings of the IEEE/CVF International Conference on Computer Vision. 2021.
          </p>
          <p>
            [6] Selvaraju, Ramprasaath R., et al. "Grad-cam: Visual explanations from deep networks via gradient-based localization." Proceedings of the IEEE international conference on computer vision. 2017.
          </p>
          <p>
            [7] Simonyan, Karen, and Andrew Zisserman. "Very deep convolutional networks for large-scale image recognition." arXiv preprint arXiv:1409.1556 (2014).
          </p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- {%- if page.bibtex %}
<section class="section" id="BibTeX">
  <div class="container is-max-desktop content">
    <h2 class="title">BibTeX</h2>
    <p>
      If you find our work useful for your research, please cite with the following bibtex:
    </p>
    <pre><code>{{ page.bibtex }}</code></pre>
  </div>
</section>
{%- endif %} -->

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