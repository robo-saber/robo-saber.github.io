---
layout: splash
author_profile: false
---

# Robo-Saber: A Full-body Physics-based Virtual Reality Playtesting Agent

<!-- <img src="/assets/images/website-title.svg" /> -->

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/OwlCarousel2/2.3.4/assets/owl.carousel.min.css">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/OwlCarousel2/2.3.4/assets/owl.theme.default.min.css">
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

/_ @media (min-width:320px) {
div.name {
text-transform: uppercase;
width: 100%;
}
} _/

@media (min-width:600px) {
div.name {
text-transform: uppercase;
/_ margin-right: auto; _/
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
/_ min-height: 200px; _/
margin-top:-50px;
margin-bottom: -50px;
/_ margin-left: auto;
margin-right: auto; _/
}

a {
text-decoration: none;
}

ul.authors.links li {
margin-top: 0.8rem;
padding: 0 0.1rem;
}

/_ Style buttons _/
.btn {
background-color: rgb(70, 139, 250);; /_ Blue background _/
border: none; /_ Remove borders _/
color: white; /_ White text _/
padding: 8px 12px; /_ Some padding _/
font-size: 14px; /_ Set a font size _/
cursor: pointer; /_ Mouse pointer on hover _/
border-radius: 18px;
}

/_ Darker background on mouse-over _/
.btn:hover {
background-color: rgb(70, 139, 250);;
/_ Blue background _/
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

<script src="https://code.jquery.com/jquery-3.7.1.min.js" integrity="sha256-/JqT3SQfawRcv/BIHPThkBvs0OEvtFFmqPF/lYI/Cxo=" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/OwlCarousel2/2.3.4/owl.carousel.min.js"></script>

<script>
$('.owl-carousel').owlCarousel({
    loop:true,
    margin:10,
    nav:true,
    responsive:{
        0:{
            items:1
        },
        600:{
            items:3
        },
        1000:{
            items:5
        }
    }
})
</script>

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

<div class="owl-carousel owl-theme">
{% for row in site.data.show_website %}
<div class="item">
<table class="results">
<tr>
<td>
<video width="320" controls>
    <source src="https://users.aalto.fi/~kimn1/robo-saber/videos/{{row.hash}}_{{row.difficulty}}.mp4" type="video/mp4">
</video>
</td>

</tr>
<tr>
<td>
<a href="https://beatsaver.com/maps/{{row.id}}" target="_blank">{{row.name}} ({{row.difficulty}})</a>
</td>
</tr>
</table>
</div>
{% endfor %}
</div>
<script>
$('.owl-carousel').owlCarousel({
    loop:false,
    margin:10,
    nav:true,
    lazyLoad:true,
    responsive:{
        0:{
            items:1
        },
        600:{
            items:2
        },
        1000:{
            items:3
        }
    }
})
</script>

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
