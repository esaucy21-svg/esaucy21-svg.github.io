---
layout: default
title: Photos
permalink: /photos/
---

## My Photos

<style>
.photo-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 12px; margin-top: 20px; }
.photo-grid a img { width: 100%; border-radius: 8px; cursor: pointer; transition: transform 0.2s, opacity 0.2s; }
.photo-grid a img:hover { transform: scale(1.03); opacity: 0.85; }

#lightbox { display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%;
  background: rgba(0,0,0,0.9); z-index: 9999; justify-content: center; align-items: center; }
#lightbox.active { display: flex; }
#lightbox img { max-width: 90%; max-height: 90vh; border-radius: 10px; box-shadow: 0 0 30px #000; }
#lightbox-close { position: fixed; top: 20px; right: 30px; color: #fff; font-size: 2.5rem;
  cursor: pointer; z-index: 10000; line-height: 1; }
</style>

<div id="lightbox" onclick="this.classList.remove('active')">
  <span id="lightbox-close">&times;</span>
  <img id="lightbox-img" src="" alt="">
</div>

<div class="photo-grid">
  <a href="#" onclick="openLight('{{ site.url }}/assets/images/ph1.jpeg'); return false;">
    <img src="{{ site.url }}/assets/images/ph1.jpeg" alt="Photo 1">
  </a>
  <a href="#" onclick="openLight('{{ site.url }}/assets/images/ph2.jpeg'); return false;">
    <img src="{{ site.url }}/assets/images/ph2.jpeg" alt="Photo 2">
  </a>
  <a href="#" onclick="openLight('{{ site.url }}/assets/images/ph3.jpeg'); return false;">
    <img src="{{ site.url }}/assets/images/ph3.jpeg" alt="Photo 3">
  </a>
</div>

<script>
function openLight(src) {
  document.getElementById('lightbox-img').src = src;
  document.getElementById('lightbox').classList.add('active');
}
document.addEventListener('keydown', function(e) {
  if (e.key === 'Escape') document.getElementById('lightbox').classList.remove('active');
});
</script>