---
layout: splash
author_profile: false
---

<!-- # Robo-Saber: Full-body Physics-based User Modeling for Virtual Reality -->

<img src="/assets/images/website-title.svg" />

<style>
div {
    /* border: 1px solid black; */
}

div.author {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
}

div.affiliation {
    padding-left: 10px;
    font-size: 0.8rem;
    vertical-align: middle;
}

/* @media (min-width:320px) {
div.name {
    text-transform: uppercase;
    width: 100%;
}
} */

@media (min-width:600px) {
div.name {
    text-transform: uppercase;
    /* margin-right: auto; */
}
}

span.affiliation {
    size: 1px;
}
p.author {
    margin: 5px 0
}

div.teaser {
    overflow: hidden;
    align: center;
    text-align: center;
    padding-bottom: 10px;
    padding-top: 10px;
}

img.teaser {
    overflow: hidden;
    object-fit: cover;
    width:40%;
    min-width: 300px;
    /* min-height: 200px; */
    margin-top:-50px;
    margin-bottom: -50px;
    /* margin-left: auto;
    margin-right: auto; */
}

a {
  text-decoration: none;
}

ul.authors.links li {
	margin-top: 0.8rem;
	padding: 0 0.1rem;
}

/* Style buttons */
.btn {
	background-color: rgb(70, 139, 250);; /* Blue background */
	border: none; /* Remove borders */
	color: white; /* White text */
	padding: 8px 12px; /* Some padding */
	font-size: 14px; /* Set a font size */
	cursor: pointer; /* Mouse pointer on hover */
	border-radius: 18px;
}
  
  /* Darker background on mouse-over */
.btn:hover {
	background-color: rgb(70, 139, 250);;
        /* Blue background */
}

div.links {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    text-align: center;
    justify-content:center;
}

div.youtube {
    width: 80%;
    min-width: 320px;
    margin: auto;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    text-align: center;
    justify-content:center;
}

div.teaser {
    width: 100%;
    min-width: 320px;
    margin: auto;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    text-align: center;
    justify-content:center;
}

table.results {
    align-items: center;
    text-align: center;
}

table.teaser {
    align-items: center;
    text-align: center;
}

</style>

<div class="authors">
{% for author in site.data.authors %}

<div class="author">
<div class="name">
{% if author.website != "" %}
<a href="{{author.website}}">{{author.name}}</a>
{% else %}
{{author.name}}
{% endif %}
</div>
<div class="affiliation">{{author.affiliation}}</div>
</div>
{% endfor %}

<div class="links">
{% for link in site.data.links %}

    <a href="{{link.url}}" target="_blank ">
        <button class="btn "><i class="{{link.icon}} "></i> {{link.name}}</button>
    </a>

{% endfor %}

</div>

<div class="teaser">
<table class="teaser">
<tr>
<td>
<video width="100%" controls autoplay loop muted>
    <source src="https://users.aalto.fi/~kimn1/robo-saber/videos/4421.mp4" type="video/mp4">
</video>
</td>
</tr>
<tr>
<td>
<a href="https://beatsaver.com/maps/4421" target="_blank">Toby Fox - Megalovania (Normal)</a>
</td>
</tr>
</table>

We present the first full-body physically simulated AI player for VR games, demonstrated in simulated playtesting of Beat Saber maps.

</div>

</div>

## Results

<table class="results">
<tr>
<td>
<video width="320" controls>
    <source src="https://users.aalto.fi/~kimn1/robo-saber/videos/1a322.mp4" type="video/mp4">
</video>
</td>
<td>
<video width="320" controls>
    <source src="https://users.aalto.fi/~kimn1/robo-saber/videos/1ad3b.mp4" type="video/mp4">
</video>
</td>
</tr>
<tr>
<td>
<a href="https://beatsaver.com/maps/1a322" target="_blank">Camellia - Myths You Forgot (Expert+)</a>
</td>
<td>
<a href="https://beatsaver.com/maps/1ad3b" target="_blank">Toby Fox - Megalovania (Camellia Remix) (Expert+)</a>
</td>
</tr>
</table>

## Summary

We trained and evaluated **Robo-Saber**, a physics-based AI player for the VR game _Beat Saber_ using gameplay sequences from the BOXRR-23 dataset aligned with map files from BeatSaver. Robo-Saber is the first physics-based full-body player model for VR and capable of expert-level gameplay. Robo-Saber can simulate diverse and human-like gameplay behaviors which can be used for evaluating and playtesting brand-new maps with zero real players.

<style>
div.figure {
    width: 100%;
    margin-left: auto;
    margin-right: auto;
    align: center;
    text-align: center;
    padding-bottom: 10px;
}
</style>

<div class="figure">
<img src="{{'/assets/images/BeatyFigs-v7.png' | relative_url }}"/>
</div>
<div>
We combine a kinematic 3p motion generator with a physics-based tracking controller to build a robot player. For kinematic generation, we build on Categorical Codebook Matching [Starke et al., 2024]. For 3p tracking, we fine-tune PHC [Luo et al., 2023] with custom motion capture data featuring Beat Saber gameplay movements.
</div>

<div class="figure">
<img src="{{'/assets/images/ccm-v1.png' | relative_url }}"/>
</div>
<div>
Our kinematic 3p generator uses a transformer architecture for both input signal encoder and Gumbel-Softmax VAE. Beat Saber game objects, i.e., colored notes, bomb notes, and obstacles, as well as the history of generated output are used as input signal. The Gumbel-Softmax VAE auto-encodes reference 3p motion segments. The latent categorical distributions resulting from the input signal and the Gumbel-Softmax VAE are matched using a Jensen-Shannon divergence-based loss.
</div>

## Cite Us

<div style="display: flex;">
<pre style="line-height: 1.4; overflow: auto; font-size: 0.5rem; ">
@inproceedings{kim2025robo,
    title={Robo-Saber: Full-body Physics-based User Modeling for Virtual Reality},
    author={Kim, Nam Hee and Liu, May and H{\"a}m{\"a}l{\"a}inen, Perttu and O'Brien, James and Peng, Xue Bin},
    booktitle={arXiv preprint},
    pages={1--10},
    year={2025}
}
</pre>
</div>

## Acknowledgements

We would like to thank Vivek Nair and CyberRamen for technical discussions during the primary stage of this project. We forked AllPoland's ArcViewer for visualization. Credits for all songs and maps appearing in our study are to be attributed to the original authors.
