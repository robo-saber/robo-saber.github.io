---
layout: splash
author_profile: false
---

<!-- OwlCarousel CSS -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/OwlCarousel2/2.3.4/assets/owl.carousel.min.css">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/OwlCarousel2/2.3.4/assets/owl.theme.default.min.css">

<style>
/* ==========================================================
   Robo-Saber Project Page — Polished Academic Aesthetic
   Inspired by successful SIGGRAPH / Eurographics project pages
   ========================================================== */

/* — Global — */
body {
  font-family: 'Noto Sans', -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  color: #2b2b2b;
  max-width: 980px;
  margin-left: auto;
  margin-right: auto;
  width: 100%;
  line-height: 1.7;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

/* Override theme defaults for splash page */
.page__content {
  font-size: 1rem;
}

/* — Masthead polish — */
.masthead {
  border-bottom: 1px solid #eaeaea;
}
.greedy-nav a.site-title {
  font-family: 'Noto Sans', sans-serif;
  font-weight: 700;
  letter-spacing: -0.01em;
}

/* — Title Section — */
div.title {
  text-align: center;
  padding: 2.5rem 1rem 0.3rem 1rem;
}

.main-title {
  font-family: 'Noto Sans', sans-serif;
  font-weight: 800;
  font-size: 2.8rem;
  line-height: 1.15;
  color: #1a1a1a;
  letter-spacing: -0.025em;
  margin: 0;
}

.subtitle {
  font-family: 'Noto Sans', sans-serif;
  font-weight: 400;
  font-size: 1.3rem;
  color: #555;
  margin-top: 0.55rem;
  line-height: 1.45;
}

/* — Venue Badge — */
div.venue {
  text-align: center;
  margin: 0.9rem 0 1.2rem 0;
}

div.venue span {
  display: inline-block;
  background: linear-gradient(135deg, #4361ee 0%, #6930c3 100%);
  color: #fff;
  padding: 0.3rem 1.1rem;
  border-radius: 20px;
  font-size: 0.82rem;
  font-weight: 600;
  letter-spacing: 0.05em;
  text-transform: uppercase;
}

/* — Authors (2×3 grid) — */
div.authors {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 0.6rem 1.5rem;
  padding: 0.2rem 1rem 1.2rem 1rem;
  max-width: 720px;
  margin: 0 auto;
  text-align: center;
}

div.author {
  text-align: center;
}

div.name {
  font-weight: 600;
  font-size: 0.92rem;
  line-height: 1.35;
  white-space: nowrap;
}

div.name a {
  color: #4361ee;
  text-decoration: none;
  transition: color 0.2s ease;
}

div.name a:hover {
  color: #3a0ca3;
  text-decoration: underline;
}

div.affiliation {
  font-size: 0.7rem;
  color: #777;
  padding-left: 0;
  margin-top: 0.1rem;
  font-weight: 400;
  line-height: 1.3;
  white-space: nowrap;
}

/* — Action Buttons — */
div.links {
  display: flex;
  flex-wrap: wrap;
  gap: 0.6rem;
  align-items: center;
  justify-content: center;
  padding: 0.3rem 1rem 2rem 1rem;
}

.btn {
  display: inline-flex;
  align-items: center;
  gap: 0.4rem;
  background-color: #4361ee;
  border: none;
  color: #fff !important;
  padding: 0.55rem 1.25rem;
  font-size: 0.88rem;
  font-family: 'Noto Sans', sans-serif;
  font-weight: 500;
  cursor: pointer;
  border-radius: 24px;
  transition: all 0.25s cubic-bezier(0.4, 0, 0.2, 1);
  box-shadow: 0 2px 8px rgba(67, 97, 238, 0.22);
  text-decoration: none;
  line-height: 1.4;
}

.btn:hover {
  background-color: #3a56d4;
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(67, 97, 238, 0.32);
  color: #fff !important;
}

.btn i {
  font-size: 1rem;
}

/* — Teaser Video — */
div.teaser {
  width: 100%;
  max-width: 800px;
  min-width: 280px;
  margin: 1.2rem auto 2rem auto;
  display: block;
  text-align: center;
}

table.teaser {
  width: 100%;
  border-collapse: collapse;
  text-align: center;
}

table.teaser td {
  border: none;
  padding: 0.3rem 0;
}

table.teaser a {
  font-size: 0.9rem;
  color: #4361ee;
  font-weight: 500;
}

div.teaser video {
  border-radius: 12px;
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.10);
  width: 100%;
}

div.teaser figcaption {
  margin-top: 1rem;
  font-size: 0.92rem;
  color: #666;
  font-style: italic;
  line-height: 1.6;
  max-width: 680px;
  margin-left: auto;
  margin-right: auto;
}

/* — Section Headings — */
h2 {
  font-family: 'Noto Sans', sans-serif;
  font-weight: 700;
  font-size: 1.7rem;
  color: #1a1a1a;
  margin-top: 3rem;
  margin-bottom: 1rem;
  padding-bottom: 0.4rem;
  border-bottom: 2.5px solid #e0e0e0;
  letter-spacing: -0.01em;
}

/* — Body Paragraphs — */
article.splash p,
.page__content p {
  font-size: 1.02rem;
  line-height: 1.78;
  color: #333;
  max-width: 800px;
  margin-left: auto;
  margin-right: auto;
}

/* — Figures — */
div.figure {
  width: 100%;
  max-width: 900px;
  margin: 2rem auto;
  text-align: center;
  padding: 1rem 0;
}

div.figure img {
  max-width: 100%;
  height: auto;
  border-radius: 10px;
  box-shadow: 0 6px 24px rgba(0, 0, 0, 0.07);
  transition: box-shadow 0.3s ease;
}

div.figure img:hover {
  box-shadow: 0 10px 36px rgba(0, 0, 0, 0.12);
}

/* — Results Carousel — */
table.results {
  text-align: center;
  border-collapse: collapse;
}

table.results td {
  border: none;
  padding: 0.25rem 0;
}

table.results video {
  border-radius: 10px;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.08);
}

table.results a {
  font-size: 0.85rem;
  color: #4361ee;
  font-weight: 500;
}

.owl-carousel .item {
  padding: 0.4rem;
}

.owl-nav button span {
  font-size: 2rem;
  color: #4361ee;
}

/* — YouTube Embed — */
div.youtube {
  width: 80%;
  min-width: 280px;
  max-width: 720px;
  margin: 2rem auto;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}

/* — Citation Block — */
div.citation-block {
  background: #f6f8fa;
  border-radius: 12px;
  padding: 1.2rem 1.6rem;
  border-left: 4px solid #4361ee;
  max-width: 800px;
  margin: 1.2rem auto;
  overflow-x: auto;
}

div.citation-block pre {
  font-family: 'Fira Code', 'Source Code Pro', Consolas, monospace;
  font-size: 0.76rem;
  line-height: 1.65;
  color: #2b2b2b;
  margin: 0;
  padding: 0;
  background: transparent;
  border: none;
  white-space: pre-wrap;
  word-wrap: break-word;
  overflow: visible;
}

/* — Links — */
a {
  color: #4361ee;
  text-decoration: none;
  transition: color 0.2s ease;
}

a:hover {
  color: #3a0ca3;
}

/* — Acknowledgements — */
.acknowledgements-text {
  max-width: 800px;
  margin: 0.5rem auto 2rem auto;
  font-size: 0.95rem;
  color: #555;
  line-height: 1.7;
}

/* — Footer polish — */
.page__footer {
  border-top: 1px solid #eaeaea;
  margin-top: 3rem;
}

/* — Responsive — */
@media (max-width: 768px) {
  .main-title {
    font-size: 2rem;
  }
  .subtitle {
    font-size: 1.05rem;
  }
  div.authors {
    grid-template-columns: repeat(3, 1fr);
    gap: 0.5rem 0.8rem;
  }
  h2 {
    font-size: 1.35rem;
    margin-top: 2.2rem;
  }
  div.teaser {
    max-width: 95%;
  }
  div.figure {
    padding: 0.5rem 0;
  }
  div.citation-block {
    padding: 1rem 1rem;
  }
}

@media (max-width: 480px) {
  .main-title {
    font-size: 1.6rem;
  }
  .subtitle {
    font-size: 0.95rem;
  }
  body {
    padding: 0 0.5rem;
  }
  div.authors {
    grid-template-columns: repeat(2, 1fr);
  }
  .btn {
    padding: 0.45rem 0.9rem;
    font-size: 0.82rem;
  }
  div.citation-block pre {
    font-size: 0.68rem;
  }
}
</style>

<!-- jQuery & OwlCarousel -->
<script src="https://code.jquery.com/jquery-3.7.1.min.js" integrity="sha256-/JqT3SQfawRcv/BIHPThkBvs0OEvtFFmqPF/lYI/Cxo=" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/OwlCarousel2/2.3.4/owl.carousel.min.js"></script>

<!-- ===== Title ===== -->
<div class="title">
<div class="main-title">Robo-Saber</div>
<div class="subtitle">Generating and Simulating Virtual Reality Players</div>
</div>

<!-- ===== Venue Badge ===== -->
<div class="venue">
<span>Eurographics 2026</span>
</div>

<!-- ===== Authors ===== -->
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
</div>

<!-- ===== Action Buttons ===== -->
<div class="links">
{% for link in site.data.links %}
    {% if link.url == "" %}
        <button class="btn"><i class="{{link.icon}}"></i> {{link.name}}</button>
    {% else %}
        <a href="{{link.url}}" target="_blank">
            <button class="btn"><i class="{{link.icon}}"></i> {{link.name}}</button>
        </a>
    {% endif %}
{% endfor %}
</div>

<!-- ===== Teaser Video ===== -->
<div class="teaser">
<table class="teaser">
{% for row in site.data.show_website_teaser %}
<tr>
<td>
<video width="100%" controls autoplay loop muted>
    <source src="https://users.aalto.fi/~kimn1/robo-saber/videos/{{row.hash}}_{{row.difficulty}}.mp4" type="video/mp4">
</video>
</td>
</tr>
<tr>
<td>
<a href="https://beatsaver.com/maps/{{row.id}}" target="_blank">{{row.name}} ({{row.difficulty}})</a></td>
</tr>
{% endfor %}
</table>
<figcaption>
Robo-Saber is a player model for VR games, demonstrated in simulated Beat Saber playtesting.
</figcaption>
</div>

## Results

<div class="owl-carousel owl-theme">
{% for row in site.data.show_website %}
<div class="item">
<table class="results">
<tr>
<td>
<video width="320" controls>
    <source class="owl-lazy" src="https://users.aalto.fi/~kimn1/robo-saber/videos/{{row.hash}}_{{row.difficulty}}.mp4" type="video/mp4">
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
    video:true,
    center:true,
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

**Robo-Saber** is the first motion generation system for playtesting virtual reality (VR) games.
Given in-game object configurations—colored notes, bomb notes, and obstacles in _Beat Saber_—Robo-Saber generates three-point (_3p_) trajectories for the VR headset and two handheld controllers, guided by short style reference gameplay examples (_contextual exemplars_) from the same player.
We train on the large-scale [BOXRR-23](https://rdi.berkeley.edu/metaverse/boxrr-23/) dataset paired with map files from [BeatSaver](https://beatsaver.com/), producing a style-conditioned model that captures diverse skill levels and movement patterns across the player population.

<div class="figure">
<img src="{{'/assets/images/BeatyFigs-v9.png' | relative_url }}"/>
</div>

Robo-Saber follows a **generate–simulate–select** pipeline.
A reference-conditioned generative model samples multiple candidate _3p_ trajectories.
Each candidate is then evaluated using TorchSaber, a custom GPU-accelerated _Beat Saber_ simulator we develop.
The highest-scoring trajectory is selected and fed back autoregressively, producing minutes-long gameplay sequences on entirely new maps.
The generated _3p_ trajectories can optionally drive a physics-based full-body tracking controller (PHC, Luo et al., 2023), fine-tuned on custom _Beat Saber_ motion capture data, for whole-body gameplay simulation.

<div class="figure">
<img src="{{'/assets/images/ccm-v1.png' | relative_url }}"/>
</div>

Our generative model extends Categorical Codebook Matching (CCM, Starke et al., 2024) with two key contributions.
First, we introduce a Transformer-based style encoder that embeds contextual exemplars into a style conditioning signal, added alongside a Transformer-based game encoder that predicts the latent categorical distribution for the next _3p_ motion chunk from the game state and pose history.
Second, we replace CCM's MSE-based matching loss with a Jensen-Shannon divergence (JSD) loss for a more principled alignment between the Gumbel-Softmax VAE's encoding of the target motion and the game encoder's prediction.
The resulting model achieves elite-level _Beat Saber_ gameplay and, by conditioning on a few reference segments, correlates strongly with individual players' scores on held-out maps (_r_ = 0.789), enabling personalized score prediction for brand-new content.

## Cite Us

<div class="citation-block">
<pre>
@inproceedings{kim2026robo,
    title={Robo-Saber: Generating and Simulating Virtual Reality Players},
    author={Kim, Nam Hee and Liu, Jingjing May and Lehtinen, Jaakko and H{\"a}m{\"a}l{\"a}inen, Perttu and O'Brien, James and Peng, Xue Bin}, booktitle={arXiv preprint},
    pages={1--10},
    year={2025}
}
</pre>
</div>

