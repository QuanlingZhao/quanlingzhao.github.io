---
layout: default
title: Photography
permalink: /photography/
---

<style>
.photo-page {
  max-width: 1050px;
  margin: 0 auto;
  padding: 12px 20px 60px;
}

.photo-header {
  margin-bottom: 30px;
}

.photo-back {
  display: inline-block;
  margin-bottom: 24px;
  font-size: 14px;
  color: var(--global-text-color-light);
  text-decoration: none;
}

.photo-back:hover {
  color: var(--global-theme-color);
  text-decoration: none;
}

.photo-title {
  margin: 0 0 5px 0;
  font-size: 28px;
  font-weight: 600;
  color: var(--global-text-color);
}

.photo-subtitle {
  margin: 0;
  font-size: 15px;
  color: var(--global-text-color-light);
  font-style: italic;
}


/* Gallery */

.photo-gallery {
  column-count: 3;
  column-gap: 12px;
}

.photo-item {
  display: block;
  margin: 0 0 12px 0;
  break-inside: avoid;
  text-decoration: none;
}

.photo-item img {
  display: block;
  width: 100%;
  height: auto;
  border-radius: 3px;
  transition:
    transform 0.18s ease,
    opacity 0.18s ease;
}

.photo-item:hover img {
  transform: scale(1.008);
  opacity: 0.94;
}


/* Responsive */

@media (max-width: 850px) {
  .photo-gallery {
    column-count: 2;
  }
}

@media (max-width: 560px) {
  .photo-page {
    padding-left: 12px;
    padding-right: 12px;
  }

  .photo-gallery {
    column-count: 1;
  }

  .photo-title {
    font-size: 25px;
  }
}
</style>


<div class="photo-page">

<div class="photo-header">

<a class="photo-back" href="/">← Quanling Zhao</a>

<div class="photo-title">Photography</div>

<p class="photo-subtitle">
A few moments I've captured along the way.
</p>

</div>


<div class="photo-gallery">

<a class="photo-item" href="/assets/photo/1.jpg" target="_blank">
<img src="/assets/photo/1.jpg" alt="Photograph 1">
</a>

<a class="photo-item" href="/assets/photo/2.JPG" target="_blank">
<img src="/assets/photo/2.JPG" alt="Photograph 2">
</a>

<a class="photo-item" href="/assets/photo/3.JPG" target="_blank">
<img src="/assets/photo/3.JPG" alt="Photograph 3">
</a>

<a class="photo-item" href="/assets/photo/4.JPG" target="_blank">
<img src="/assets/photo/4.JPG" alt="Photograph 4">
</a>

<a class="photo-item" href="/assets/photo/5.jpg" target="_blank">
<img src="/assets/photo/5.jpg" alt="Photograph 5">
</a>

<a class="photo-item" href="/assets/photo/6.JPG" target="_blank">
<img src="/assets/photo/6.JPG" alt="Photograph 6">
</a>

<a class="photo-item" href="/assets/photo/7.jpg" target="_blank">
<img src="/assets/photo/7.jpg" alt="Photograph 7">
</a>

<a class="photo-item" href="/assets/photo/8.jpg" target="_blank">
<img src="/assets/photo/8.jpg" alt="Photograph 8">
</a>

<a class="photo-item" href="/assets/photo/9.jpg" target="_blank">
<img src="/assets/photo/9.jpg" alt="Photograph 9">
</a>

</div>

</div>



