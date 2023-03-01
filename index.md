
<html lang="en-US">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="theme-color" content="#157878">
    <link rel="stylesheet" href="/assets/css/style.css?v=e27bf585b9c641a881074e09853cb11204774c97">
  </head>
  <body>

<h2>Title<a name="title"></a></h2>
    
<h2>Abstract<a name="abstract"></a></h2>

<p>Zero-shot text-to-speech aims to clone target speaker’s voice with only a few data of any target speakers even unseen in training set. Existing multi-speaker systems are capable of preforming high-fidelity speech generation, but clone unseen speakers’ voices is still a challenging task. To generalize to new speakers, previous works use speaker encoder to obtain fixed-size speaker embedding from single reference audio. However single reference audio dose not contain sufficient timbre information of the target speaker, and ignores the correlation between different speech representations during training, which causes leakage of content information into the speaker representation and thus degrades text-to-speech performances. In this paper, we propose to mitigate these two problems by using multiple reference audios and use content encoder and speaker encoder to obtain content embedding and speaker embedding of reference audios. To get more disentangled representations, the proposed method further uses mutual information minimization between the two embeddings to remove entangled information within each embedding. Experiments on VCTK dataset indicate that our method can improve synthesized speech both in similarity and naturalness even unseen people.</p>

<h2>Contents</h2>
<ol>
  <li><a href="#multi-speaker">Synthesized samples: Multi-speaker</a></li>
  <li><a href="#fewshot-artificial">Synthesized samples: Few-shot+Artificial</a></li>
  <li><a href="#fewshot-realworld">Synthesized samples: Few-shot+Real-World</a></li>
</ol>

    
    
    
<h2>1. Synthesized samples -- Multi-speaker<a name="multi-speaker"></a></h2>
<h3> Using three reference audios </h3>
<table>
    <tr>
      <th style="text-align: left">Models</th>
      <td style="text-align: left">居然故意引我说错话。</td>
      <td style="text-align: left">极速向宠物医院骑去。</td>
    </tr>
  
    <tr>
      <th style="text-align: left"><strong>FS2</strong></th>
      <td style="text-align: left"><audio src="wavs\dzq-fs1.wav" controls="" preload=""></audio></td>
      <td style="text-align: left"><audio src="wavs\dzq-fs2.wav" controls="" preload=""></audio></td>
    </tr>
  
    <tr>
      <th style="text-align: left"><strong>Baseline</strong></th>
      <td style="text-align: left"><audio src="wavs\dzq-baseline1.wav" controls="" preload=""></audio></td>
      <td style="text-align: left"><audio src="wavs\dzq-baseline2.wav" controls="" preload=""></audio></td>
    </tr>
  
    <tr>
      <th style="text-align: left"><strong>Proposed-advenr-advpitch</strong></th>
      <td style="text-align: left"><audio src="wavs\dzq-advenr1.wav" controls="" preload=""></audio></td>
      <td style="text-align: left"><audio src="wavs\dzq-advenr2.wav" controls="" preload=""></audio></td>
    </tr>
  
    <tr>
      <th style="text-align: left"><strong>Proposed-advpitch</strong></th>
      <td style="text-align: left"><audio src="wavs\dzq-advenr1.wav" controls="" preload=""></audio></td>
      <td style="text-align: left"><audio src="wavs\dzq-advenr2.wav" controls="" preload=""></audio></td>
    </tr>
  
    <tr>
      <th style="text-align: left"><strong>Proposed</strong></th>
      <td style="text-align: left"><audio src="wavs\dzq-proposed1.wav" controls="" preload=""></audio></td>
      <td style="text-align: left"><audio src="wavs\dzq-proposed2.wav" controls="" preload=""></audio></td>
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
      <th style="text-align: left"><strong>FS2</strong></th>
      <td style="text-align: left"><audio src="wavs\dzq-fs1.wav" controls="" preload=""></audio></td>
      <td style="text-align: left"><audio src="wavs\dzq-fs2.wav" controls="" preload=""></audio></td>
    </tr>
  
    <tr>
      <th style="text-align: left"><strong>Baseline</strong></th>
      <td style="text-align: left"><audio src="wavs\dzq-baseline1.wav" controls="" preload=""></audio></td>
      <td style="text-align: left"><audio src="wavs\dzq-baseline2.wav" controls="" preload=""></audio></td>
    </tr>
  
    <tr>
      <th style="text-align: left"><strong>Proposed-advpitch</strong></th>
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
      <th style="text-align: left"><strong>FS2</strong></th>
      <td style="text-align: left"><audio src="wavs\xs-fs1.wav" controls="" preload=""></audio></td>
      <td style="text-align: left"><audio src="wavs\xs-fs2.wav" controls="" preload=""></audio></td>
    </tr>
  
    <tr>
      <th style="text-align: left"><strong>Baseline</strong></th>
      <td style="text-align: left"><audio src="wavs\xs-baseline1.wav" controls="" preload=""></audio></td>
      <td style="text-align: left"><audio src="wavs\xs-baseline2.wav" controls="" preload=""></audio></td>
    </tr>
  
    <tr>
      <th style="text-align: left"><strong>Proposed-advpitch</strong></th>
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


