---
layout: project
urltitle: "LightFormer: Light Oriented Global Neural Rendering in Dynamic Scene"
title: "LightFormer: Light Oriented Global Neural Rendering in Dynamic Scene"
categories: computer graphics, machine learning, rendering
permalink: /
---
<style> 
.center{text-align:center} 
</style> 

<br>
<div class="row">
  <div class="col-xs-12">
    <center>
      <h2>LightFormer: Light-Oriented Global Neural Rendering in Dynamic Scene</h2>
    </center>
    <br>
    <center>
      <a href="https://www.renhaocheng.com">Haocheng Ren</a><sup>1</sup>,
      <a href="http://www.cad.zju.edu.cn/home/huo/">Yuchi Huo</a><sup>1</sup>,
      <a href="https://www.eee.hku.hk/~evanpeng/">Yifan Peng</a><sup>2</sup>,
      Hongtao Sheng<sup>1</sup>,
      Weidong Xue<sup>1</sup>,
      Hongxiang Huang<sup>1</sup>,
      Jingzhen Lan<sup>1</sup>,
      <a href="http://www.cad.zju.edu.cn/home/rwang/">Rui Wang</a><sup>1</sup>,
      <a href="http://www.cad.zju.edu.cn/home/bao/">Hujun Bao</a><sup>1</sup>,
    </center>
    <br>
    <center>
      <sup>1</sup>State Key Laboratory of CAD &amp; CG, Zhejiang University
      <sup>2</sup>University of Hong Kong
    </center>
    <br>
    <center>
      ACM Transactions on Graphics (SIGGRAPH 2024)
    </center>
    <br>
    <center>
      <!-- <a href='https://arxiv.org/abs/2107.06149'>arXiv</a> | <a href="{{ "/static/pdf/supp.pdf" | prepend:site.baseurl }}">Supp</a> | <a href='https://www.kujiale.com/coohomcloud/minervas'>Online System</a> | <a href="https://coohom.github.io/cloud-docs/">Doc</a> -->
      <!--  -->
      <a href="{{ "/static/pdf/paper.pdf" | prepend:site.baseurl }}">Paper</a> | <a href="{{ "/static/pdf/supp.pdf" | prepend:site.baseurl }}">Supp</a> | <a href='https://pan.zju.edu.cn/share/555b20693638fcd67b7f8968c6?isCurrent=1&isopen=1&preview=455036531272&preview_side_active=1&scenario=share&share_type=file'>Video</a> | <a href="{{ "/comparison_tool/index.html" | prepend:site.baseurl }}">Interactive viewer</a>
    </center>
  </div>
</div><br>

<div class="row">
  <div class="col-md-12">
    <img src="{{ "/static/img/teaser.png" | prepend:site.baseurl }}">
  </div>
</div><br>

<!-- <div class="row" id="news">
  <div class="col-xs-12">
    <h2>News</h2>
  </div>
</div> -->

<!-- <div class="row">
  <div class="col-xs-12">
    <ul>
      <li>2022-08: The MINERVAS System is accepted to Computer Graphics Forum, Pacific Graphics 2022!</li>
      <li>2021-07: The MINERVAS System is available online!</li>
    </ul>
  </div>
</div><br> -->


<div class="row" id="abstract">
  <div class="col-xs-12">
    <h2>Abstract</h2>
  </div>
</div>

<div class="row">
  <div class="col-xs-12">
    <p>
      <!-- <center><iframe width="900" height="500" src="https://www.youtube.com/embed/wUUINjbLNG0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center> -->
      <!-- <center><iframe width="900" height="500" src="https://www.youtube.com/embed/sAr4AYdpdrU" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center> -->
      <center><iframe width="900" height="500" src="https://www.youtube.com/embed/5PflBxEjeq4" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>
    </p>
    <p>
      The generation of global illumination in real time has been a long-standing challenge in the graphics community, particularly in dynamic scenes with complex illumination. 
      Recent neural rendering techniques have shown great promise by utilizing neural networks to represent the illumination of scenes and then decoding the final radiance. However, incorporating object parameters into the representation may limit their effectiveness in handling fully dynamic scenes.
      This work presents a neural rendering approach, dubbed LightFormer, that can generate realistic global illumination for fully dynamic scenes, including dynamic lighting, materials, cameras, and animated objects, in real time. Inspired by classic many-lights methods, the proposed approach focuses on the neural representation of light sources in the scene rather than the entire scene, leading to the overall better generalizability. The neural prediction is achieved by leveraging the virtual point lights and shading clues for each light.
      Specifically, two stages are explored. In the light encoding stage, each light generates a set of virtual point lights in the scene, which are then encoded into an implicit neural light representation, along with screen-space shading clues like visibility. In the light gathering stage, a pixel-light attention mechanism composites all light representations for each shading point. Given the geometry and material representation, in tandem with the composed light representations of all lights, a lightweight neural network predicts the final radiance.
      Experimental results demonstrate that the proposed LightFormer can yield reasonable and realistic global illumination in fully dynamic scenes with real-time performance.
    </p>
  </div>
</div><br>

<!-- <div class="row">
  <div class="col-xs-12">
    <h2>Online System</h2>
  </div>
</div>

<div class="row">
  <div class="col-xs-12">
    <p>
      We provide a free trial account for each user with the limited scene and machine time, you can sign up <a href='https://www.kujiale.com/coohomcloud/minervas#/register'>here</a>. If you would like to use our system for research purposes, please send the <a href="{{ "/static/pdf/tos.pdf" | prepend:site.baseurl }}">Terms of Use</a> to <a href="mailto:minervas@qunhemail.com" class="email" data-animate-hover="shake" data-animate="fadeInUp">MINERVAS Group<i class="fa fa-envelope"></i></a>. Once receiving the agreement form, our group will contact you.
    </p>
  </div>
</div><br>

<div class="row">
  <div class="col-xs-12">
    <h2>DSL Examples</h2>
  </div>
</div>

<div class="row">
  <div class="col-xs-12">
    <p>
      MINERVAS system allows users to control the data generation pipeline via Domain Specific Language (DSL). The DSL is designed with flexibility and ease of use. For flexibility, we build our DSL as an internal DSL under the Python programming language. For ease of use, we provide several common samplers for users to easily generate diverse scenes for domain randomization.
    </p>
    <p>
      Here we show some examples of our DSL and generated results. We only show the built-in samplers here. For more information about DSL, please refer to <a href='https://coohom.github.io/cloud-docs/'>Document</a>.
    </p>
  </div>
</div><br> -->


<!-- **** Furniture arrangement sampler *** -->
<!-- <div class="center">
  <div class="col-xs-12">
    <h3>Furniture Rearrangment</h3>
  </div>
</div>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.0.1/styles/atom-one-light.min.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.0.1/highlight.min.js"></script>
<script>hljs.highlightAll();</script>
<pre><code class="python">class FurnitureLayoutSampler(SceneProcessor):
  def process(self):
      for room in self.shader.world.rooms:
          room.randomize_layout(self.shader.world)
</code></pre>

<link rel="stylesheet" href="{{ '/static/css/w3.css' | prepend:site.baseurl }}">
<div class="w3-center w3-content w3-section" style="max-width:600px">
  <img class="mySlides" src="{{ '/static/img/samples/Layout_0.jpg' | prepend:site.baseurl }}" style="width:100%">
  <img class="mySlides" src="{{ '/static/img/samples/Layout_1.jpg' | prepend:site.baseurl }}" style="width:100%">
  <img class="mySlides" src="{{ '/static/img/samples/Layout_2.jpg' | prepend:site.baseurl }}" style="width:100%">
  <img class="mySlides" src="{{ '/static/img/samples/Layout_3.jpg' | prepend:site.baseurl }}" style="width:100%">
</div>

<script type="text/javascript" src="{{ '/static/js/slideshow.js' | prepend:site.baseurl }}"></script>
<script>
carousel("mySlides", 0);
</script>

<!-- **** Material sampler *** -->
<!-- <div class="center">
  <div class="col-xs-12">
    <h3>Material Sampler</h3>
  </div>
</div>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.0.1/styles/atom-one-light.min.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.0.1/highlight.min.js"></script>
<script>hljs.highlightAll();</script>
<pre><code class="python">class MaterialSampler(EntityProcessor):
    def process(self):
        for instance in self.shader.world.instances:
            if instance.label in [247, 894]: # 247: 'chair', 894: 'desk'
                self.shader.world.replace_material(id=instance.id)
</code></pre>

<link rel="stylesheet" href="{{ '/static/css/w3.css' | prepend:site.baseurl }}">
<div class="w3-center w3-content w3-section" style="max-width:600px">
  <img class="mySlides2" src="{{ '/static/img/samples/Material_4.jpg' | prepend:site.baseurl }}" style="width:100%">
  <img class="mySlides2" src="{{ '/static/img/samples/Material_6.jpg' | prepend:site.baseurl }}" style="width:100%">
  <img class="mySlides2" src="{{ '/static/img/samples/Material_7.jpg' | prepend:site.baseurl }}" style="width:100%">
  <img class="mySlides2" src="{{ '/static/img/samples/Material_8.jpg' | prepend:site.baseurl }}" style="width:100%">
</div>

<script>
carousel("mySlides2", 0);
</script> -->

<!-- **** Light sampler *** -->
<!-- <div class="center">
  <div class="col-xs-12">
    <h3>Light Sampler</h3>
  </div>
</div>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.0.1/styles/atom-one-light.min.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.0.1/highlight.min.js"></script>
<script>hljs.highlightAll();</script>
<pre><code class="python">class LightSampler(EntityProcessor):
    def process(self):
        for light in self.shader.world.lights:
            light._tune_temp(1) # randomize color temperature
            light.tune_intensity(1) # randomize intensity
            light.tune_random(1.2) # randomize intensity
</code></pre>

<link rel="stylesheet" href="{{ '/static/css/w3.css' | prepend:site.baseurl }}">
<div class="w3-center w3-content w3-section" style="max-width:600px">
  <img class="mySlides3" src="{{ '/static/img/samples/Light_1.jpg' | prepend:site.baseurl }}" style="width:100%">
  <img class="mySlides3" src="{{ '/static/img/samples/Light_2.jpg' | prepend:site.baseurl }}" style="width:100%">
  <img class="mySlides3" src="{{ '/static/img/samples/Light_3.jpg' | prepend:site.baseurl }}" style="width:100%">
  <img class="mySlides3" src="{{ '/static/img/samples/Light_4.jpg' | prepend:site.baseurl }}" style="width:100%">
</div>

<script>
carousel("mySlides3", 0);
</script> -->


<!-- **** Model sampler *** -->
<!-- <div class="center">
  <div class="col-xs-12">
    <h3>Model Sampler</h3>
  </div>
</div>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.0.1/styles/atom-one-light.min.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.0.1/highlight.min.js"></script>
<script>hljs.highlightAll();</script>
<pre><code class="python">class ModelSampler(EntityProcessor):
    def process(self):
        for instance in self.shader.world.instances:
            if instance.type == 'ASSET':
                self.shader.world.replace_model(id=instance.id)
</code></pre>

<link rel="stylesheet" href="{{ '/static/css/w3.css' | prepend:site.baseurl }}">
<div class="w3-center w3-content w3-section" style="max-width:600px">
  <img class="mySlides4" src="{{ '/static/img/samples/Model_0.jpg' | prepend:site.baseurl }}" style="width:100%">
  <img class="mySlides4" src="{{ '/static/img/samples/Model_1.jpg' | prepend:site.baseurl }}" style="width:100%">
  <img class="mySlides4" src="{{ '/static/img/samples/Model_16.jpg' | prepend:site.baseurl }}" style="width:100%">
  <img class="mySlides4" src="{{ '/static/img/samples/Model_14.jpg' | prepend:site.baseurl }}" style="width:100%">
</div>

<script>
carousel("mySlides4", 0);
</script> -->

<!-- **** Depth sampler *** -->
<!-- <div class="center">
  <div class="col-xs-12">
    <h3>Depth sampler</h3>
  </div>
</div>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.0.1/styles/atom-one-light.min.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.0.1/highlight.min.js"></script>
<script>hljs.highlightAll();</script>
<pre><code class="python">class DepthNoiseSample(PixelProcessor):
    def process(self):
        # 0: NoNoiseModel
        # 1: GaussianNoiseModel
        # 2: PoissonNoiseModel
        # 3: SaltAndPepperNoiseModel
        # 4: KinectNoiseModel
        self.gen_depth(noise=4)
</code></pre>

<link rel="stylesheet" href="{{ '/static/css/w3.css' | prepend:site.baseurl }}">
<div class="w3-center w3-content w3-section" style="max-width:600px">
  <img class="mySlides5" src="{{ '/static/img/samples/depth.jpg' | prepend:site.baseurl }}" style="width:100%">
  <img class="mySlides5" src="{{ '/static/img/samples/depth_Kinect.jpg' | prepend:site.baseurl }}" style="width:100%">
  <img class="mySlides5" src="{{ '/static/img/samples/depth_Gaussian.jpg' | prepend:site.baseurl }}" style="width:100%">
  <img class="mySlides5" src="{{ '/static/img/samples/depth_Poisson.jpg' | prepend:site.baseurl }}" style="width:100%">
</div>

<script>
carousel("mySlides5", 0);
</script>
<br> -->

<!-- <div class="center">
  <div class="col-xs-12">
    <h3>Visual Results</h3>
  </div>
</div>


<link rel="stylesheet" href="{{ '/static/css/w3.css' | prepend:site.baseurl }}">
<div class="w3-center w3-content w3-section" style="max-width:1200px">
  <img class="mySlides5" src="{{ '/static/img/results1.png' | prepend:site.baseurl }}" style="width:100%">
</div>

<script>
carousel("mySlides0", 0);
</script>
<br>

<div class="center">
  <div class="col-xs-12">
    <h3>Free-view Walk-through</h3>
  </div>
</div>


<link rel="stylesheet" href="{{ '/static/css/w3.css' | prepend:site.baseurl }}">
<div class="w3-center w3-content w3-section" style="max-width:1200px">
  <img class="mySlides5" src="{{ '/static/img/results2.png' | prepend:site.baseurl }}" style="width:100%">
</div> -->

<script>
carousel("mySlides1", 0);
</script>
<br>




<div class="row">
  <div class="col-xs-12">
    <h2>Acknowledgements</h2>
  </div>
</div>

<div class="row">
  <div class="col-xs-12">
    <p>
      We thank all reviewers for their insightful comments. We also thank Chuankun Zheng, Yuzhi Liang for helpful discussions, and He Zhu for preparing 3D scenes. 
    </p>
  </div>
</div><br>

<div class="row">
  <div class="col-xs-12">
    <h2>Citation</h2>
  </div>
</div>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.0.1/styles/atom-one-light.min.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/11.0.1/highlight.min.js"></script>
<!-- <script>hljs.highlightAll();</script> -->
<pre><code class="text">
@article{ren2024lightformer,
  title={LightFormer: Light-Oriented Global Neural Rendering in Dynamic Scene},
  author={Ren, Haocheng and Huo, Yuchi and Peng, Yifan and Sheng, Hongtao and Huang, Hongxiang and Xue, Weidong and Lan, Jingzhen and Wang, Rui and Bao, Hujun},
  journal={ACM Transactions on Graphics},
  volume={43},
  number={4},
  pages={1--14},
  year={2024},
  publisher={ACM New York, NY}
}
<!-- @article{10.1145/3582001,
author = {Ren, Haocheng and Fan, Hangming and Wang, Rui and Huo, Yuchi and Tang, Rui and Wang, Lei and Bao, Hujun},
title = {Data-Driven Digital Lighting Design for Residential Indoor Spaces},
year = {2023},
issue_date = {June 2023},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
volume = {42},
number = {3},
issn = {0730-0301},
url = {https://doi.org/10.1145/3582001},
journal = {ACM Trans. Graph.},
doi = {10.1145/3582001},
month = {mar},
articleno = {28},
numpages = {18},
keywords = {Lighting design, neural network, interior design, deep learning, data-driven approach}} -->
</code></pre>

<hr>
