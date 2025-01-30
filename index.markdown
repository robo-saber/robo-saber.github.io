---
layout: splash
author_profile: false
---

# Robo-Saber: Physics-based Full-body User Modeling in Virtual Reality

_Submitted to SIGGRAPH 2025_

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

div.video {
    width: 100%;
    min-width: 320px;
    margin: auto;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    text-align: center;
    justify-content:center;
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

<div class="video">
<video width="100%" controls autoplay loop muted>
    <source src="https://users.aalto.fi/~kimn1/robo-saber/videos/1ad3b_comp.mp4" type="video/mp4">
</video>
We present the first full-body physically simulated AI player for VR games, demonstrated in simulated playtesting of Beat Saber maps.
</div>
</div>

## Results

TODO

## Summary

We trained and evaluated **Robo-Saber**, a physics-based AI player for the VR game _Beat Saber_ using gameplay sequences from the BOXRR-23 dataset aligned with map files from BeatSaver. Robo-Saber is the first physics-based full-body player model for VR and capable of expert-level gameplay. Robo-Saber can simulate diverse and human-like gameplay behaviors which can be used for evaluating and playtesting brand-new maps with zero real players.

<!-- ## Abstract

The use of physics-based character controllers has emerged as a general-purpose approach for modeling embodied interaction such as virtual reality (VR) games. A key promise here is that VR designers can conveniently test and optimize their creations in silico, using AI playtesting to augment the time-consuming and expensive traditional user testing. However, models thus far have been limited to simple interaction tasks and to partial body models, such as a single arm. To tackle this limitation, we present Robo-Saber, the first physics-based full-body VR user simulation model capable of playing Beat Saber, a popular VR game that requires complex and spatio-temporally precise full-body movements. Our technical solution combines 1) a custom kinematic generative model for the three-point (3p) position and orientation movements of the VR headset and hand trackers and 2) a finetuned 3p tracking controller for reconstructing the movements of the player’s body in a physically plausible manner. By training our model on the large BOXRR-23 dataset, our system is able to exhibit human-like gameplay behavior that generalizes to new game maps. We validate the embodied player model’s simulated behaviors by 1) comparing the model’s gameplay capability to human players, and 2) predicting the human scores of Beat Saber maps not included in the training data, which demonstrates the model’s utility for user modeling. Our results suggest that Robo-Saber could assist the designers of novel Beat Saber maps. Our combination of 3p kinematic generation and full-body physics-based tracking should also be applicable for modeling VR scenarios beyond Beat Saber. -->

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
    title={Robo-Saber: Physics-based Full-body User Modeling in Virtual Reality},
    author={Kim, Nam Hee and Liu, May and H{\"a}m{\"a}l{\"a}inen, Perttu and O'Brien, James and Peng, Xue Bin},
    booktitle={arXiv preprint},
    pages={1--10},
    year={2025}
}
</pre>
</div>

## Acknowledgements

We would like to thank Vivek Nair and CyberRamen for technical discussions during the primary stage of this project. We forked AllPoland's ArcViewer for visualization. Credits for all songs and maps appearing in our study are attributed to the original authors.
