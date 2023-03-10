
<html lang="en-US">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="theme-color" content="#157878">
    <link rel="stylesheet" href="/assets/css/style.css?v=e27bf585b9c641a881074e09853cb11204774c97">
  </head>
  <body>

<h2>Title<a name="Title"></a></h2>
    
<p>Robust Few-shot Speech Synthesis with Fine-grained Noise Modeling via Adversarial Factorization<p>
    
<h2>Abstract<a name="abstract"></a></h2>

<p>Few-shot speech synthesis aims to synthesize speech using target speaker's voice with limited data. Pre-training and fine-tuning techniques often work well with high-quality data. Nevertheless, it is usually costly to collect in real applications, which presents challenge to synthesize clean speech from noisy data. Previous studies introduce an additional noise control module to address the problem. However, a single noise embedding is difficult to capture the complicated acoustic condition, such as the type and level of background noise vary along time. In this paper, we present a noise-robust speech synthesis system by integrating disentangled, fine-grained features. These fine-grained features learn to present local noise variations disentangled from prosody. Multi-speaker and adaptation experiments are conducted with real-world and artificial noisy data. Results show the effectiveness of our method compared to baselines under both of the two noisy conditions.</p>

<h2>Contents</h2>
<ol>
  <li><a href="#multi-speaker">Synthesized samples: Multi-speaker</a></li>
  <li><a href="#fewshot-artificial">Synthesized samples: Few-shot+Artificial</a></li>
  <li><a href="#fewshot-realworld">Synthesized samples: Few-shot+Real-World</a></li>
</ol>

    
<h2>1. Synthesized samples -- Multi-speaker<a name="multi-speaker"></a></h2>
    
<h3> Here we present a piece of noisy and clean audio of reference speaker to extract Zs in our multi-speaker database.</h3>

<table class="table">
<tbody>
         <tr>
            <td>Female</td>
            <td><audio src="wavs\spk30-noise.wav" controls="" preload=""></audio></td>
            <td><audio src="wavs\spk30-clean.wav" controls="" preload=""></audio></td>
        </tr>
</tbody>
</table>    
    
<h3> Here we present the synthesized audios from different models using noisy and clean audios to extract Zs.</h3>
    

<h3> Using three reference audios </h3>
<table>
    <tr>
      <th style="text-align: left">Models</th>
      <td style="text-align: left">noisy Zs</td>
      <td style="text-align: left">clean Zs</td>
    </tr>
  
    <tr>
      <th style="text-align: center"><strong>Base-FS</strong></th>
      <td colspan="2" style="text-align: left"><audio src="wavs\fs.wav" controls="" preload=""></audio></td>
    </tr>
  
    <tr>
      <th style="text-align: left"><strong>Base-Utt</strong></th>
      <td style="text-align: left"><audio src="wavs\baseline.wav" controls="" preload=""></audio></td>
      <td style="text-align: left"><audio src="wavs\baseline-clean.wav" controls="" preload=""></audio></td>
    </tr>
  
    <tr>
      <th style="text-align: left"><strong>Proposed(w/o advpitch)</strong></th>
      <td style="text-align: left"><audio src="wavs\advenr.wav" controls="" preload=""></audio></td>
      <td style="text-align: left"><audio src="wavs\advenr-clean.wav" controls="" preload=""></audio></td>
    </tr>
  
    <tr>
      <th style="text-align: left"><strong>Proposed</strong></th>
      <td style="text-align: left"><audio src="wavs\advenr-advpitch.wav" controls="" preload=""></audio></td>
      <td style="text-align: left"><audio src="wavs\advenr-advpitch-clean.wav" controls="" preload=""></audio></td>
    </tr>
  
</table>
    
   
    
    
<h2>2. Synthesized samples -- Few-shot Artificial<a name="fewshot-artificial"></a></h2>
    
<h3> Here we present noisy audios from a female, whose noisy audios are obtained by adding noise to clean audio</h3>

<table class="table">
<tbody>
         <tr>
            <td>Female</td>
            <td><audio src="wavs\dengziqi_96.wav" controls="" preload=""></audio></td>
            <td><audio src="wavs\dengziqi_64.wav" controls="" preload=""></audio></td>
        </tr>
</tbody>
</table>
   
    
    
<h3> Here we present the synthesized audios from different models, which are trained with real-world noisy dataset.</h3>
<table>
    <tr>
      <th style="text-align: left">Models</th>
      <td style="text-align: left">居然故意引我说错话。</td>
      <td style="text-align: left">极速向宠物医院骑去。</td>
    </tr>
  
    <tr>
      <th style="text-align: left"><strong>Base-FS</strong></th>
      <td style="text-align: left"><audio src="wavs\dzq-fs1.wav" controls="" preload=""></audio></td>
      <td style="text-align: left"><audio src="wavs\dzq-fs2.wav" controls="" preload=""></audio></td>
    </tr>
  
    <tr>
      <th style="text-align: left"><strong>Base-Utt</strong></th>
      <td style="text-align: left"><audio src="wavs\dzq-baseline1.wav" controls="" preload=""></audio></td>
      <td style="text-align: left"><audio src="wavs\dzq-baseline2.wav" controls="" preload=""></audio></td>
    </tr>
  
    <tr>
      <th style="text-align: left"><strong>Proposed(w/o advpitch)</strong></th>
      <td style="text-align: left"><audio src="wavs\dzq-advenr1.wav" controls="" preload=""></audio></td>
      <td style="text-align: left"><audio src="wavs\dzq-advenr2.wav" controls="" preload=""></audio></td>
    </tr>
  
    <tr>
      <th style="text-align: left"><strong>Proposed</strong></th>
      <td style="text-align: left"><audio src="wavs\dzq-proposed1.wav" controls="" preload=""></audio></td>
      <td style="text-align: left"><audio src="wavs\dzq-proposed2.wav" controls="" preload=""></audio></td>
    </tr>
  
</table>

    
    
<h2>3. Synthesized samples -- Few-shot Real World<a name="fewshot-realworld"></a></h2>
    
<h3>Here we present noisy audios from a male, whose noisy audios are from real-world. </h3>
<table class="table">
<tbody>
         <tr>
            <td>Male</td>
            <td><audio src="wavs\许嵩_24.wav" controls="" preload=""></audio></td>
            <td><audio src="wavs\许嵩_25.wav" controls="" preload=""></audio></td>
        </tr>
</tbody>
</table>
    
    
<h3>Here we present the synthesized audios from different models, which are trained with real-world noisy dataset.</h3>    
<table>
    <tr>
      <th style="text-align: left">Models</th>
      <td style="text-align: left">在每趟长途挑运之后。</td>
      <td style="text-align: left">这样费时费力更危险。</td>
    </tr>
  
    <tr>
      <th style="text-align: left"><strong>Base-FS</strong></th>
      <td style="text-align: left"><audio src="wavs\xs-fs1.wav" controls="" preload=""></audio></td>
      <td style="text-align: left"><audio src="wavs\xs-fs2.wav" controls="" preload=""></audio></td>
    </tr>
  
    <tr>
      <th style="text-align: left"><strong>Base-Utt</strong></th>
      <td style="text-align: left"><audio src="wavs\xs-baseline1.wav" controls="" preload=""></audio></td>
      <td style="text-align: left"><audio src="wavs\xs-baseline2.wav" controls="" preload=""></audio></td>
    </tr>
  
    <tr>
      <th style="text-align: left"><strong>Proposed(w/o advpitch)</strong></th>
      <td style="text-align: left"><audio src="wavs\xs-advenr1.wav" controls="" preload=""></audio></td>
      <td style="text-align: left"><audio src="wavs\xs-advenr2.wav" controls="" preload=""></audio></td>
    </tr>
  
    <tr>
      <th style="text-align: left"><strong>Proposed</strong></th>
      <td style="text-align: left"><audio src="wavs\xs-proposed2.wav" controls="" preload=""></audio></td>
      <td style="text-align: left"><audio src="wavs\xs-proposed1.wav" controls="" preload=""></audio></td>
    </tr>
  
</table>  
    
    
  </body>
</html>


