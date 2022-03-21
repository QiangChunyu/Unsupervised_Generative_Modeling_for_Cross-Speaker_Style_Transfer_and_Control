<!DOCTYPE html>
<html lang="en-US"><head>
<meta http-equiv="content-type" content="text/html; charset=UTF-8">
    <meta charset="UTF-8">

<!-- Begin Jekyll SEO tag v2.7.1 -->
<title>K-Converter: An unsupervised singing Voice Conversion System | KConverter</title>
<meta name="generator" content="Jekyll v3.9.0">
<meta property="og:title" content="K-Converter: An unsupervised singing Voice Conversion System">
<meta property="og:locale" content="en_US">
<link rel="canonical" href="https://vcdemo-1.github.io/KConverter/">
<meta property="og:url" content="https://vcdemo-1.github.io/KConverter/">
<meta property="og:site_name" content="KConverter">
<meta name="twitter:card" content="summary">
<meta property="twitter:title" content="K-Converter: An unsupervised singing Voice Conversion System">
<script type="application/ld+json">
{"url":"https://vcdemo-1.github.io/KConverter/","@type":"WebSite","headline":"K-Converter: An unsupervised singing Voice Conversion System","name":"KConverter","@context":"https://schema.org"}</script>
<!-- End Jekyll SEO tag -->

    <link rel="preconnect" href="https://fonts.gstatic.com/">
    <link rel="preload" href="https://fonts.googleapis.com/css?family=Open+Sans:400,700&amp;display=swap" as="style" type="text/css" crossorigin="">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="theme-color" content="#157878">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
    <link rel="stylesheet" href="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/style.css">
    <!-- start custom head snippets, customize with your own _includes/head-custom.html file -->

<!-- Setup Google Analytics -->



<!-- You can set your favicon here -->
<!-- link rel="shortcut icon" type="image/x-icon" href="/KConverter/favicon.ico" -->

<!-- end custom head snippets -->

  </head>
  <body>
    <a id="skip-to-content" href="#content">Skip to the content.</a>

    <header class="page-header" role="banner">
      <h1 class="project-name">K-Converter: An unsupervised singing Voice Conversion System</h1>
      <h2 class="project-tagline"></h2>
      
        <a href="https://github.com/vcdemo-1/KConverter" class="btn">View on GitHub</a>
      
      
    </header>

    <main id="content" class="main-content" role="main">
      <h1 id="-k-converter-an-unsupervised-singing-voice-conversion-system"><center> K-Converter: An unsupervised singing Voice Conversion System</center></h1>
<center>Ying Zhang, Peng Yang, Jinba Xiao, Ye Bai, Hao Che, Xiaorui Wang</center>
<p><br></p>
<center>Kwai, Beijing, P.R. China</center>
<p><br></p>

<h2 id="abstract">Abstract</h2>
<div style="text-align: justify"> Singing voice conversion (SVC) 
converts a singer's voice to another one's voice while preserving the 
linguistic content. Recently, some SVC systems rely on super-vised 
phonetic features extracted from pre-trained automatic speech 
recognition (ASR) models, increasing system complexity. Some end-to-end 
SVC systems use adver-sarial training, which causes instability during 
optimization. To address these issues, we present K-Converter, a simple 
system to disentangle the timbre, pitch, and content information without
 any manual supervision or adversarial training. First, low quefrencies 
of mel-frequency cepstral coefficients (MFCC), which remove the global 
excitation mainly, are used as input representation. And the pitch-shift
 augmentation is used for further disentangling the pitch. Second, an 
encoder network is carefully designed to construct an information 
bottleneck, which learns to break up the pitch and timbre information of
 the source. Third, the content consistency loss is introduced to keep 
the content consistent between encoder outputs of source utterances and 
reconstructed ones. Experimental results show that our proposed system 
performs well in both speech naturalness and timbre similarity, with 
better robustness to comparisons. </div>

<p><br></p>

<h2 id="model-architecture">Model Architecture</h2>
<table border="0">
  <tbody>
    <tr>
      <td><img src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/kconverter.png" alt="Overall Architecture"></td>
    </tr>
  </tbody>
</table>

<p><br></p>

<h2 id="audio-samples">Audio Samples</h2>

<p><strong>Target Singers</strong></p>

<hr>
<table>
  <thead>
    <tr>
      <th>Target</th>
      <th>Samples</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Female</td>
      <td><audio controls="controls" preload="auto">
            <source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/f_biaobei_002_01.wav"></audio></td>
    </tr>
    <tr>
      <td>Male</td>
      <td><audio controls="controls" preload="auto">
            <source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/m_biaobei_093_0001.wav"></audio></td>
    </tr>
  </tbody>
</table>
<hr>

<p><strong>Source Singers</strong></p>

<table>
  <thead>
    <tr>
      <th>Source</th>
      <th>Samples</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>F1</td>
      <td><audio controls="controls" preload="auto">
            <source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/f_wangchenrui_1021_500_002.wav"></audio></td>
    </tr>
    <tr>
      <td>F2</td>
      <td><audio controls="controls" preload="auto">
            <source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/f_mpol_20_123.wav"></audio></td>
    </tr>
    <tr>
      <td>M1</td>
      <td><audio controls="controls" preload="auto">
            <source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/m_wuduo_1028_766_018.wav"></audio></td>
    </tr>
    <tr>
      <td>M2</td>
      <td><audio controls="controls" preload="auto">
            <source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/m_zhiy_14_123.wav"></audio></td>
    </tr>
  </tbody>
</table>
<hr>

<p><br></p>

<h2 id="comparison-with-baseline-systems">Comparison with Baseline Systems</h2>

<p><strong>Target Female</strong></p>

<table align="center">
  <thead>
    <tr>
      <th>System</th>
      <th>F1</th>
      <th>F2</th>
      <th>M1</th>
      <th>M2</th>
    </tr>
  </thead>
  <tbody>
   <tr>
      <td>BASE1</td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/vaekl-f_wangchenrui_1021_500_002.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/vaekl-f_mpol_20_123_to_fbiaobei.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/vaekl-m_wuduo_1028_766_018.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/vaekl-m_zhiy_14_123_to_fbiaobei.wav"></audio></td>
    </tr>
    <tr>
      <td>BASE2</td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/confusion-f_wangchenrui_1021_500_002_002.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/confusion-f_mpol_20_123_to_fbiaobei.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/confusion-m_wuduo_1028_766_018.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/confusion-m_zhiy_14_123_to_fbiaobei.wav"></audio></td>
    </tr>
    <tr>
      <td>Ours</td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/oursox-f_wangchenrui_1021_500_002_002.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/oursox-f_mpol_123_to_fbiaobei.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/oursox-m_wuduo_1028_766_018.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/oursox-m_zhiy_14_123_to_fbiaobei.wav"></audio></td>
    </tr>
  </tbody>
</table>
<hr>

<p><strong>Target Male</strong></p>

<table align="center">
  <thead>
    <tr>
      <th>System</th>
      <th>F1</th>
      <th>F2</th>
      <th>M1</th>
      <th>M2</th>
    </tr>
  </thead>
  <tbody>
   <tr>
      <td>BASE1</td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/vaekl-f_wangchenrui_1021_500_002_002.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/vaekl-f_mpol_20_123_to_mbiaobei.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/vaekl-m_wuduo_1028_766_018_002.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/vaekl-m_zhiy_14_123_to_mbiaobei.wav"></audio></td>
    </tr>
    <tr>
      <td>BASE2</td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/confusion-f_wangchenrui_1021_500_002.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/confusion-f_mpol_20_123_to_mbiaobei.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/confusion-m_wuduo_1028_766_018_002.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/confusion-m_zhiy_14_123_to_mbiaobei.wav"></audio></td>
    </tr>
    <tr>
      <td>Ours</td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/oursox-f_wangchenrui_1021_500_002.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/oursox-f_mpol_20_123_to_mbiaobei.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/oursox-m_wuduo_1028_766_018_002.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/oursox-m_zhiy_14_123_to_mbiaobei.wav"></audio></td>
    </tr>
  </tbody>
</table>
<hr>
<p><br></p>

<h2 id="ablation">Ablation</h2>

<p><strong>Ablation of the feature representation</strong></p>
<table align="center">
  <thead>
    <tr>
      <th>Feature Representation</th>
      <th>F2F</th>
      <th>F2M</th>
      <th>M2F</th>
      <th>M2M</th>
    </tr>
  </thead>
  <tbody>
   <tr>
      <td>MEL80</td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/mel2mel-oursrc-f_wangchenrui_1021_500_002.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/mel2mel-oursox-f_wangchenrui_1021_500_002.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/mel2mel-oursrc-m_wuduo_1028_766_018.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/mel2mel-oursrc-m_wuduo_1028_766_018.htm"></audio></td>
    </tr>
    <tr>
      <td>MFCC20</td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/srcdata-oursox-f_wangchenrui_1021_500_002.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/srcdata-oursox-f_wangchenrui_1021_500_002_002.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/srcdata-oursox-m_wuduo_1028_766_018_002.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/srcdata-oursox-m_wuduo_1028_766_018.wav"></audio></td>
    </tr>
    <tr>
      <td>+Aug</td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/oursox-f_wangchenrui_1021_500_002_002.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/oursox-f_wangchenrui_1021_500_002.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/oursox-m_wuduo_1028_766_018.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/oursox-m_wuduo_1028_766_018_002.wav"></audio></td>
    </tr>
  </tbody>
</table>

<hr>
<p><strong>Ablation of the temporal down-sampling rate</strong></p>
<table align="center">
  <thead>
    <tr>
      <th></th>
      <th>F2F</th>
      <th>F2M</th>
      <th>M2F</th>
      <th>M2M</th>
    </tr>
  </thead>
  <tbody>
   <tr>
      <td>1</td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/freq1-oursox-f_mpol_20_123_to_f_biaobei.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/freq1-oursox-f_mpol_20_123_to_m_biaobei.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/freq1-oursox-m_zhiy_123_to_f_biaobei.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/freq1-oursox-m_zhiy_123_to_m_biaobei.wav"></audio></td>
    </tr>
    <tr>
      <td>8</td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/oursox-f_mpol_123_to_fbiaobei.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/oursox-f_mpol_20_123_to_mbiaobei.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/oursox-m_zhiy_14_123_to_fbiaobei.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/oursox-m_zhiy_14_123_to_mbiaobei.wav"></audio></td>
    </tr>
    <tr>
      <td>32</td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/freq32-oursox-f_mpol_20_123_to_f_biaobei.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/freq32-oursox-f_mpol_20_123-to-m_biaobei_gen.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/freq32-oursox-m_zhiy_123_to_f_biaobei.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/freq32-oursox-m_zhiy_123_to_m_biaobei.htm"></audio></td>
    </tr>
  </tbody>
</table>
<hr>

<p><strong>Ablation of the content consistency loss</strong></p>

<p>** source female*</p>
<audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/f_pmar_11_123.wav"></audio>
<p>** source male*</p>
<audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/m_wenzihao_1013_8_022.wav"></audio>

<table align="center">
  <thead>
    <tr>
      <th></th>
      <th>F2F</th>
      <th>F2M</th>
      <th>M2F</th>
      <th>M2M</th>
    </tr>
  </thead>
  <tbody>
   <tr>
      <td>w/o</td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/noct_f_pmar_to_fbiaobei.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/noct_f_pmar_to_mbiaobei.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/noct-m_wenzihao_1013_8_022.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/noct-m_wenzihao_1013_8_022_002.wav"></audio></td>
    </tr>
    <tr>
      <td>w</td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/oursox-f_pmar_11_fbiaobei.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/oursox-f_pmar_11_mbiaobei.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/oursox-m_wenzihao_1013_8_022_002.wav"></audio></td>
      <td><audio controls="controls" preload="auto"><source src="K-Converter%20An%20unsupervised%20singing%20Voice%20Conversion%20System%20KConverter_files/oursox-m_wenzihao_1013_8_022.wav"></audio></td>
    </tr>
  </tbody>
</table>



      <footer class="site-footer">
        
          <span class="site-footer-owner"><a href="https://github.com/vcdemo-1/KConverter">KConverter</a> is maintained by <a href="https://github.com/vcdemo-1">vcdemo-1</a>.</span>
        
        <span class="site-footer-credits">This page was generated by <a href="https://pages.github.com/">GitHub Pages</a>.</span>
      </footer>
    </main>
  

</body></html>
