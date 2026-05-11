---
layout: splash
author_profile: false
---

<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-XXXXXXXXXX');
</script>

<!-- Swiper CSS -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@12.1.3/swiper-bundle.min.css">

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
  font-variant-caps: small-caps;
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
  min-width: 0;
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
  font-size: 0.63rem;
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
  padding: 0.3rem 1rem 0.8rem 1rem;
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
  letter-spacing: 0;
  font-variant-caps: small-caps;
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
.results-card {
  background: #fff;
  border: 1px solid #eaeaea;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.05);
  transition: transform 0.3s cubic-bezier(0.4, 0, 0.2, 1), box-shadow 0.3s ease;
  width: 100%;
  display: flex;
  flex-direction: column;
  height: 100%;
}

.results-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
}

.results-card video,
.results-card iframe {
  width: 100%;
  display: block;
  border-bottom: 1px solid #f0f0f0;
  aspect-ratio: 16 / 9;
  object-fit: cover;
  border: none;
}

.results-card-content {
  padding: 0.2rem 0.5rem;
  text-align: center;
  flex-grow: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #fff;
}

.results-card-title {
  font-size: 0.78rem;
  font-weight: 600;
  color: #4361ee;
  line-height: 1.2;
  text-decoration: none;
}

.results-card-title:hover {
  color: #3a0ca3;
  text-decoration: underline;
}

.carousel-container {
  position: relative;
  padding: 0 0 3.5rem 0;
  box-sizing: border-box;
  margin-top: 1rem;
}

.carousel-container .swiper-slide {
  display: flex;
  justify-content: center;
  height: auto;
  opacity: 0.25;
  transform: scale(0.92);
  transition: opacity 0.4s ease, transform 0.4s ease;
}

.carousel-container .swiper-slide-active {
  opacity: 1;
  transform: scale(1);
}

.carousel-nav,
.store-media-thumb-nav {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 2rem;
  border: 1px solid #e0e0e0;
  background: #fff;
  color: #4361ee;
  cursor: pointer;
  font-family: 'Noto Sans', sans-serif;
  font-size: 1.8rem;
  line-height: 1;
  transition: border-color 0.2s ease, background 0.2s ease, opacity 0.2s ease;
}

.carousel-nav:hover,
.carousel-nav:focus,
.store-media-thumb-nav:hover,
.store-media-thumb-nav:focus {
  background: #f6f8fa;
  border-color: #4361ee;
  outline: none;
}

.carousel-nav.swiper-button-disabled,
.store-media-thumb-nav.swiper-button-disabled {
  cursor: default;
  opacity: 0.35;
}

.carousel-nav.swiper-button-lock,
.store-media-main-nav.swiper-button-lock,
.store-media-thumb-nav.swiper-button-lock {
  display: flex !important;
}

.carousel-nav span,
.store-media-main-nav span,
.store-media-thumb-nav span {
  display: block;
  line-height: 1;
}

.carousel-nav {
  position: absolute;
  top: 43%;
  z-index: 3;
  height: 4rem;
  transform: translateY(-50%);
}

.carousel-prev {
  left: 0;
}

.carousel-next {
  right: 0;
}

.carousel-scrollbar.swiper-scrollbar,
.store-media-thumb-scrollbar.swiper-scrollbar {
  position: relative !important;
  left: auto !important;
  bottom: auto !important;
  width: 100% !important;
  height: 4px !important;
  margin-top: 0.55rem;
  background: #e0e0e0;
  border-radius: 999px;
}

.carousel-scrollbar .swiper-scrollbar-drag,
.store-media-thumb-scrollbar .swiper-scrollbar-drag {
  background: #4361ee;
}

.carousel-scrollbar.swiper-scrollbar-lock,
.store-media-thumb-scrollbar.swiper-scrollbar-lock {
  display: block !important;
}

/* — Store Media Carousel — */
div.store-media {
  width: 100%;
  min-width: 280px;
  max-width: 900px;
  margin: 0.6rem auto 2rem auto;
  padding: 0.8rem;
  box-sizing: border-box;
  background: #fff;
  border: 1px solid #eaeaea;
  border-radius: 8px;
  box-shadow: 0 6px 24px rgba(0, 0, 0, 0.07);
}

.store-media-heading {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem 0.8rem;
  align-items: center;
  justify-content: space-between;
  padding: 0 0.15rem 0.65rem 0.15rem;
}

.store-media-heading-count {
  padding: 0.18rem 0.5rem;
  border: 1px solid #e0e0e0;
  border-radius: 999px;
  color: #555;
  font-size: 0.76rem;
  line-height: 1.2;
}

.store-media-heading-title,
.store-media-label,
.store-media-thumbs-heading,
.store-media-thumb-type {
  font-weight: 700;
  text-transform: uppercase;
}

.store-media-heading-title,
.store-media-label,
.store-media-thumbs-heading {
  color: #777;
  letter-spacing: 0.08em;
}

.store-media-heading-title {
  font-size: 0.74rem;
}

.store-media-carousel {
  position: relative;
  overflow: hidden;
}

.store-media-carousel .swiper-slide {
  height: auto;
}

.store-media-frame {
  position: relative;
  background: #000;
  border-radius: 4px;
  overflow: hidden;
  box-shadow: 0 0 0 1px #eaeaea;
}

.store-media-frame::before {
  content: "";
  display: block;
  padding-top: 56.25%;
}

.store-media-frame .responsive-video-container {
  position: absolute;
  inset: 0;
  width: 100%;
  max-width: none;
  height: 100%;
  padding-bottom: 0;
  margin-bottom: 0;
}

.store-media-frame iframe,
.store-media-frame video {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
  border-radius: 4px;
}

.store-media-thumb-media img,
.store-media-thumb-media video {
  display: block;
  width: 100%;
  object-fit: cover;
}

.store-media-frame video {
  aspect-ratio: 16 / 9;
  background: #000;
}

.store-media-caption {
  display: flex;
  flex-wrap: wrap;
  gap: 0.4rem 0.8rem;
  align-items: center;
  justify-content: space-between;
  padding: 0.7rem 0.2rem 0.2rem 0.2rem;
  color: #333;
  font-size: 0.9rem;
  line-height: 1.45;
}

.store-media-caption a {
  color: #4361ee;
  font-weight: 600;
}

.store-media-label {
  font-size: 0.72rem;
}

.store-media-main-nav-layer {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 0;
  padding-top: 56.25%;
  z-index: 3;
  opacity: 0;
  pointer-events: none;
  transition: opacity 0.18s ease;
}

.store-media-carousel:hover .store-media-main-nav-layer,
.store-media-carousel:focus-within .store-media-main-nav-layer {
  opacity: 1;
}

.store-media-main-nav {
  display: flex;
  align-items: center;
  justify-content: center;
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  width: 44px;
  height: 72px;
  padding: 0;
  background: transparent !important;
  border: 0;
  border-radius: 0;
  color: #fff;
  cursor: pointer;
  font-family: 'Noto Sans', sans-serif;
  font-size: 3rem;
  line-height: 1;
  text-shadow: 0 2px 10px rgba(0, 0, 0, 0.75);
  pointer-events: auto;
}

.store-media-main-nav:hover,
.store-media-main-nav:focus {
  color: #fff;
  outline: none;
}

.store-media-main-nav.swiper-button-disabled {
  cursor: default;
  opacity: 0.25;
}

.store-media-main-prev {
  left: 0;
}

.store-media-main-next {
  right: 0;
}

.store-media-thumbs-heading {
  margin-top: 0.75rem;
  font-size: 0.72rem;
}

.store-media-thumbs-wrap {
  display: grid;
  grid-template-columns: 2rem minmax(0, 1fr) 2rem;
  gap: 0.35rem;
  align-items: stretch;
  margin-top: 0.35rem;
}

.store-media-thumbs {
  min-width: 0;
  padding-bottom: 0.7rem;
  overflow: hidden;
}

.store-media-thumbs .swiper-wrapper {
  align-items: stretch;
}

.store-media-thumb-button {
  min-width: 0;
  width: 215px !important;
  height: auto;
  padding: 0;
  background: #fff !important;
  border: 1px solid #e0e0e0 !important;
  border-radius: 3px;
  color: #333 !important;
  cursor: pointer;
  font-family: 'Noto Sans', sans-serif;
  text-align: left;
  transition: border-color 0.2s ease, background 0.2s ease;
}

.store-media-thumb-button.is-active,
.store-media-thumb-button.swiper-slide-thumb-active,
.store-media-thumb-button:hover,
.store-media-thumb-button:focus {
  background: #f6f8fa !important;
  border-color: #4361ee !important;
  outline: none;
}

.store-media-thumb-button:focus-visible {
  box-shadow: 0 0 0 2px rgba(67, 97, 238, 0.25);
}

.store-media-thumb {
  display: grid !important;
  grid-template-columns: 5.4rem minmax(0, 1fr);
  gap: 0.55rem;
  align-items: center;
  width: auto !important;
  padding: 0.45rem;
  background: transparent !important;
  border-radius: 0 !important;
}

.store-media-thumb,
.store-media-thumb-media,
.store-media-thumb-type,
.store-media-thumb-title {
  height: auto !important;
  margin: 0 !important;
}

.store-media-thumb-media {
  display: block !important;
  width: 100% !important;
  aspect-ratio: 16 / 9;
  overflow: hidden;
  background: #000 !important;
  border-radius: 2px !important;
}

.store-media-thumb-media img,
.store-media-thumb-media video {
  height: 100%;
}

.store-media-thumb-type,
.store-media-thumb-title {
  display: block !important;
  width: auto !important;
  background: transparent !important;
  border-radius: 0 !important;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}

.store-media-thumb-type {
  color: #4361ee;
  font-size: 0.68rem;
  letter-spacing: 0.07em;
}

.store-media-thumb-title {
  margin-top: 0.12rem;
  color: #333;
  font-size: 0.82rem;
}

.store-media-summary {
  margin-top: 0.65rem;
  color: #555;
  font-size: 0.9rem;
  line-height: 1.55;
}

@media (hover: none), (pointer: coarse) {
  .store-media-main-nav-layer {
    opacity: 1;
  }
}

/* — Abstract — */
div.abstract {
  max-width: 800px;
  margin: 0.5rem auto 2rem auto;
  padding: 0 1rem;
  box-sizing: border-box;
  color: #444;
  line-height: 1.75;
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
  div.store-media {
    max-width: 95%;
    padding: 0.55rem;
  }
  .store-media-main-nav {
    width: 34px;
    height: 56px;
    font-size: 2.4rem;
  }
  .store-media-thumbs-wrap {
    grid-template-columns: 1.8rem minmax(0, 1fr) 1.8rem;
  }
  .store-media-thumb-nav {
    width: 1.8rem;
  }
  .store-media-thumb-button {
    width: 82% !important;
  }
  .store-media-thumb {
    grid-template-columns: 4.8rem minmax(0, 1fr);
  }
  .store-media-caption {
    align-items: flex-start;
  }
  .store-media-caption a {
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

<!-- Swiper -->
<script src="https://cdn.jsdelivr.net/npm/swiper@12.1.3/swiper-bundle.min.js"></script>

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

<!-- ===== Store Media Carousel ===== -->
<div class="store-media">
<div class="store-media-heading">
<span class="store-media-heading-title">Videos</span>
<span class="store-media-heading-count" aria-live="polite"><span class="store-media-current">1</span> / {{ site.data.show_website_teaser.size | plus: 2 }} videos</span>
</div>
<div class="store-media-carousel swiper">
<div class="swiper-wrapper">
<div class="swiper-slide">
<div class="store-media-frame fitvidsignore">
{% include video id="urABYGfCeAc" provider="youtube" %}
</div>
<div class="store-media-caption">
<span class="store-media-label">Video</span>
<span>Eurographics 2026 Fast-Forward</span>
</div>
</div>
<div class="swiper-slide">
<div class="store-media-frame fitvidsignore">
{% include video id="rjWQRB7w2LI" provider="youtube" %}
</div>
<div class="store-media-caption">
<span class="store-media-label">Video</span>
<span>Supplementary Video</span>
</div>
</div>
{% for row in site.data.show_website_teaser %}
<div class="swiper-slide">
<div class="store-media-frame fitvidsignore">
<video controls loop muted playsinline>
    <source src="https://users.aalto.fi/~kimn1/robo-saber/videos/{{row.hash}}_{{row.difficulty}}.mp4" type="video/mp4">
</video>
</div>
<div class="store-media-caption">
<span class="store-media-label">Gameplay</span>
<a href="https://beatsaver.com/maps/{{row.id}}" target="_blank">{{row.name}} ({{row.difficulty}})</a>
</div>
</div>
{% endfor %}
</div>
<div class="store-media-main-nav-layer">
<button class="store-media-main-nav store-media-main-prev" type="button" aria-label="Previous video"><span aria-hidden="true">&lsaquo;</span></button>
<button class="store-media-main-nav store-media-main-next" type="button" aria-label="Next video"><span aria-hidden="true">&rsaquo;</span></button>
</div>
</div>
<div class="store-media-thumbs-wrap">
<button class="store-media-thumb-nav store-media-thumb-prev" type="button" aria-label="Previous playlist item"><span aria-hidden="true">&lsaquo;</span></button>
<div class="store-media-thumbs swiper">
<div class="swiper-wrapper">
<button class="store-media-thumb-button swiper-slide is-active" type="button" data-store-media-index="0" aria-label="Show video" aria-current="true">
<span class="store-media-thumb">
<span class="store-media-thumb-media"><img src="https://img.youtube.com/vi/urABYGfCeAc/mqdefault.jpg" alt=""></span>
<span>
<span class="store-media-thumb-type">Video</span>
<span class="store-media-thumb-title">Eurographics 2026 Fast-Forward</span>
</span>
</span>
</button>
<button class="store-media-thumb-button swiper-slide" type="button" data-store-media-index="1" aria-label="Show video">
<span class="store-media-thumb">
<span class="store-media-thumb-media"><img src="https://img.youtube.com/vi/rjWQRB7w2LI/mqdefault.jpg" alt=""></span>
<span>
<span class="store-media-thumb-type">Video</span>
<span class="store-media-thumb-title">Supplementary Video</span>
</span>
</span>
</button>
{% for row in site.data.show_website_teaser %}
<button class="store-media-thumb-button swiper-slide" type="button" data-store-media-index="{{ forloop.index | plus: 1 }}" aria-label="Show video">
<span class="store-media-thumb">
<span class="store-media-thumb-media">
<video muted playsinline preload="metadata">
    <source src="https://users.aalto.fi/~kimn1/robo-saber/videos/{{row.hash}}_{{row.difficulty}}.mp4#t=0.1" type="video/mp4">
</video>
</span>
<span>
<span class="store-media-thumb-type">Gameplay</span>
<span class="store-media-thumb-title">Example</span>
</span>
</span>
</button>
{% endfor %}
</div>
<div class="store-media-thumb-scrollbar swiper-scrollbar"></div>
</div>
<button class="store-media-thumb-nav store-media-thumb-next" type="button" aria-label="Next playlist item"><span aria-hidden="true">&rsaquo;</span></button>
</div>
<div class="store-media-summary">
Robo-Saber is a player model for VR games, demonstrated in simulated Beat Saber playtesting.
</div>
</div>
## Abstract

<div class="abstract" markdown="1">
We present the first motion generation system for playtesting virtual reality (VR) games. Our player model generates VR headset and handheld controller movements from in-game object arrangements, guided by style exemplars and aligned to maximize simulated gameplay score. We train on the large BOXRR-23 dataset and apply our framework on the popular VR game Beat Saber. The resulting model Robo-Saber produces skilled gameplay and captures diverse player behaviors, mirroring the skill levels and movement patterns specified by input style exemplars. Robo-Saber demonstrates promise in synthesizing rich gameplay data for predictive applications and enabling a physics-based whole-body VR playtesting agent.
</div>

## Results: Generation + Tracking

<div class="results-main-carousel carousel-container swiper">
<div class="swiper-wrapper">
{% for row in site.data.show_website %}
<div class="swiper-slide">
  <div class="results-card">
    <video controls muted playsinline preload="metadata">
        <source src="https://users.aalto.fi/~kimn1/robo-saber/videos/{{row.hash}}_{{row.difficulty}}.mp4" type="video/mp4">
    </video>
    <div class="results-card-content">
      <a class="results-card-title" href="https://beatsaver.com/maps/{{row.id}}" target="_blank">{{row.name}} ({{row.difficulty}})</a>
    </div>
  </div>
</div>
{% endfor %}
</div>
<button class="carousel-nav carousel-prev results-main-prev" type="button" aria-label="Previous result"><span aria-hidden="true">&lsaquo;</span></button>
<button class="carousel-nav carousel-next results-main-next" type="button" aria-label="Next result"><span aria-hidden="true">&rsaquo;</span></button>
<div class="results-main-pagination swiper-pagination"></div>
<div class="results-main-scrollbar carousel-scrollbar swiper-scrollbar"></div>
</div>

## 3p Generation and Stylization

<div class="generation-carousel carousel-container swiper">
<div class="swiper-wrapper">
<div class="swiper-slide">
  <div class="results-card">
    <iframe src="https://drive.google.com/file/d/1vu14Ir-rlGDVhvl2033tvufXVhQcdKC_/preview"></iframe>
    <div class="results-card-content">
      <span class="results-card-title">Generation Example 1</span>
    </div>
  </div>
</div>
<div class="swiper-slide">
  <div class="results-card">
    <iframe src="https://drive.google.com/file/d/1yCyU8SIShV5il-97tnT5IJkFBFuk1yEd/preview"></iframe>
    <div class="results-card-content">
      <span class="results-card-title">Generation Example 2</span>
    </div>
  </div>
</div>
<div class="swiper-slide">
  <div class="results-card">
    <iframe src="https://drive.google.com/file/d/1ecCP2X-YM2oFPSLt3B600Or2k41VF5Hs/preview"></iframe>
    <div class="results-card-content">
      <span class="results-card-title">Generation Example 3</span>
    </div>
  </div>
</div>
<div class="swiper-slide">
  <div class="results-card">
    <iframe src="https://drive.google.com/file/d/1Kfeeh8fiAxTl8GVZuq7baHZPTWcPnUyV/preview"></iframe>
    <div class="results-card-content">
      <span class="results-card-title">Generation Example 4</span>
    </div>
  </div>
</div>
<div class="swiper-slide">
  <div class="results-card">
    <iframe src="https://drive.google.com/file/d/1inIv7G-siFwyVtBmHsm3D50Jq9fIe0zF/preview"></iframe>
    <div class="results-card-content">
      <span class="results-card-title">Generation Example 5</span>
    </div>
  </div>
</div>
<div class="swiper-slide">
  <div class="results-card">
    <iframe src="https://drive.google.com/file/d/1aiMmkk_ksz91JSpzhsRu9G7Ew8vrdRvS/preview"></iframe>
    <div class="results-card-content">
      <span class="results-card-title">Generation Example 6</span>
    </div>
  </div>
</div>
</div>
<button class="carousel-nav carousel-prev generation-prev" type="button" aria-label="Previous result"><span aria-hidden="true">&lsaquo;</span></button>
<button class="carousel-nav carousel-next generation-next" type="button" aria-label="Next result"><span aria-hidden="true">&rsaquo;</span></button>
<div class="generation-pagination swiper-pagination"></div>
<div class="generation-scrollbar carousel-scrollbar swiper-scrollbar"></div>
</div>

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
The generated _3p_ trajectories can optionally drive a physics-based full-body tracking controller (PHC, [Luo et al., 2023](https://arxiv.org/abs/2305.06456)), fine-tuned on custom _Beat Saber_ motion capture data, for whole-body gameplay simulation.

<video width="100%" controls loop muted>
    <source src="https://users.aalto.fi/~kimn1/robo-saber/videos/humans_side_by_side_short.mp4" type="video/mp4">
</video>

Our training data comprises millions of gameplay sequences accumulated from over 70k players in [BOXRR-23](https://rdi.berkeley.edu/metaverse/boxrr-23/), aligned with map files from [BeatSaver](https://beatsaver.com/).
Naturally, different players move differently in terms of how and how well they can play.

<table class="teaser">
<tr>
<td style="width:50%; padding-right:8px;" markdown="1">

![](https://users.aalto.fi/~kimn1/robo-saber/videos/supervised_learning_in.png)

</td>
<td style="width:50%; padding-left:8px;">
<video width="100%" controls loop muted>
    <source src="https://users.aalto.fi/~kimn1/robo-saber/videos/supervised_learning_gt_cropped.mp4" type="video/mp4">
</video>
</td>
</tr>
</table>

We formulate generative motion planning as a simple supervised learning problem: given the in-game object arrangements and the headset/handheld controller state (left), we task our model with predicting the 1-second future trajectory (right).

However, the key question remains: how should we represent the individual players' variability in gameplay styles?

<table class="teaser">
<tr>
<td style="width:50%;">
<video width="100%" controls loop muted>
    <source src="https://users.aalto.fi/~kimn1/robo-saber/videos/left_0.mp4" type="video/mp4">
</video>
</td>
<td style="width:50%;">
<video width="100%" controls loop muted>
    <source src="https://users.aalto.fi/~kimn1/robo-saber/videos/left_1.mp4" type="video/mp4">
</video>
</td>
</tr>
</table>

Our idea is to use short sample clips of actual gameplay (we dub "contextual exemplars") to represent individual players' gameplay skills and movement patterns. For example, a skilled expert player's contextual exemplars (left) show confident and aggressive swings, while a novice player's (right) shows cautious and small swings.

<div class="figure">
<img src="{{'/assets/images/ccm-v2.png' | relative_url }}"/>
</div>

Our generative model extends Categorical Codebook Matching (CCM, [Starke et al., 2024](https://dl.acm.org/doi/10.1145/3658209)) with two key contributions.
First, we introduce a Transformer-based style encoder that embeds contextual exemplars into a style conditioning signal, added alongside a Transformer-based game encoder that predicts the latent categorical distribution for the next _3p_ motion chunk from the game state and pose history.
Second, we replace CCM's MSE-based matching loss with a Jensen-Shannon divergence (JSD) loss for a more principled alignment between the Gumbel-Softmax VAE's encoding of the target motion and the game encoder's prediction.

<table class="teaser">
<tr>
<td style="width:50%;">
<video width="100%" controls loop muted>
    <source src="https://users.aalto.fi/~kimn1/robo-saber/videos/comparison_0.mp4" type="video/mp4">
</video>
</td>
</tr>
</table>

By feeding the contextual exemplars along with in-game object arrangements and player model state to the model, we can produce output consistent with the target skill level and movement output. The generated trajectory (right) reflects the confident and fast swings of the exemplars (left).

<table class="teaser">
<tr>
<td style="width:50%;">
<video width="100%" controls loop muted>
    <source src="https://users.aalto.fi/~kimn1/robo-saber/videos/comparison_1.mp4" type="video/mp4">
</video>
</td>
</tr>
</table>

Similarly, the model can produce novice-like movements by feeding a novice player's contextual exemplars.

The resulting model achieves elite-level _Beat Saber_ gameplay and, by conditioning on a few reference segments, correlates strongly with individual players' scores on held-out maps (_r_ = 0.789), enabling personalized score prediction for brand-new content.

## Cite Us

<div class="citation-block">
<pre>
@inproceedings{kim2026robo,
  title={Robo-Saber: Generating and Simulating Virtual Reality Players},
  author={Kim, Nam Hee and Liu, Jingjing May and Lehtinen, Jaakko and H{\"a}m{\"a}l{\"a}inen, Perttu and O'Brien, James F. and Peng, Xue Bin},
  booktitle={Computer Graphics Forum},
  pages={e70353},
  year={2026},
  organization={Wiley Online Library}
}
</pre>
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
    var storeMediaThumbs = document.querySelectorAll('.store-media-thumb-button');

    var storeThumbsSwiper = new Swiper('.store-media-thumbs', {
        loop: false,
        slidesPerView: 'auto',
        spaceBetween: 8,
        freeMode: true,
        watchSlidesProgress: true,
        slideToClickedSlide: true,
        navigation: {
            nextEl: '.store-media-thumb-next',
            prevEl: '.store-media-thumb-prev'
        },
        scrollbar: {
            el: '.store-media-thumb-scrollbar',
            draggable: true,
            hide: false
        }
    });

    var storeMediaSwiper = new Swiper('.store-media-carousel', {
        loop: false,
        slidesPerView: 1,
        spaceBetween: 0,
        navigation: {
            nextEl: '.store-media-main-next',
            prevEl: '.store-media-main-prev'
        },
        thumbs: {
            swiper: storeThumbsSwiper
        },
        on: {
            slideChange: function () {
                var currentIndex = this.realIndex;
                storeMediaThumbs.forEach(function (thumb, index) {
                    thumb.classList.toggle('is-active', index === currentIndex);
                    thumb.setAttribute('aria-current', index === currentIndex ? 'true' : 'false');
                });
                document.querySelector('.store-media-current').textContent = currentIndex + 1;
            }
        }
    });

    var resultsSwiper = new Swiper('.results-main-carousel', {
        loop: true,
        centeredSlides: true,
        slidesPerView: 1.2,
        spaceBetween: 16,
        navigation: {
            nextEl: '.results-main-next',
            prevEl: '.results-main-prev'
        },
        pagination: {
            el: '.results-main-pagination',
            clickable: true
        },
        scrollbar: {
            el: '.results-main-scrollbar',
            draggable: true,
            hide: false
        },
        breakpoints: {
            768: {
                slidesPerView: 1.4,
                spaceBetween: 24
            },
            1024: {
                slidesPerView: 1.6,
                spaceBetween: 32
            }
        }
    });

    var generationSwiper = new Swiper('.generation-carousel', {
        loop: true,
        centeredSlides: true,
        slidesPerView: 1.2,
        spaceBetween: 16,
        navigation: {
            nextEl: '.generation-next',
            prevEl: '.generation-prev'
        },
        pagination: {
            el: '.generation-pagination',
            clickable: true
        },
        scrollbar: {
            el: '.generation-scrollbar',
            draggable: true,
            hide: false
        },
        breakpoints: {
            768: {
                slidesPerView: 1.4,
                spaceBetween: 24
            },
            1024: {
                slidesPerView: 1.6,
                spaceBetween: 32
            }
        }
    });
});
</script>
