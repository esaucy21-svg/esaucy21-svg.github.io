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

  <a href="#" onclick="openLight('{{ site.url }}/assets/images/ph4.jpeg'); return false;">
    <img src="{{ site.url }}/assets/images/ph4.jpeg" alt="Photo 4">
  </a>

  <a href="#" onclick="openLight('{{ site.url }}/assets/images/ph5.jpeg'); return false;">
    <img src="{{ site.url }}/assets/images/ph5.jpeg" alt="Photo 5">
  </a>

  <a href="#" onclick="openLight('{{ site.url }}/assets/images/ph6.jpeg'); return false;">
    <img src="{{ site.url }}/assets/images/ph6.jpeg" alt="Photo 6">
  </a>

  <a href="#" onclick="openLight('{{ site.url }}/assets/images/ph7.jpeg'); return false;">
    <img src="{{ site.url }}/assets/images/ph7.jpeg" alt="Photo 7">
  </a>

  <a href="#" onclick="openLight('{{ site.url }}/assets/images/ph8.jpeg'); return false;">
    <img src="{{ site.url }}/assets/images/ph8.jpeg" alt="Photo 8">
  </a>
 
  <a href="#" onclick="openLight('{{ site.url }}/assets/images/ph9.jpeg'); return false;">
    <img src="{{ site.url }}/assets/images/ph9.jpeg" alt="Photo 9">
  </a>

  <a href="#" onclick="openLight('{{ site.url }}/assets/images/ph10.jpeg'); return false;">
    <img src="{{ site.url }}/assets/images/ph10.jpeg" alt="Photo 10">
  </a>

   <a href="#" onclick="openLight('{{ site.url }}/assets/images/ph11.jpeg'); return false;">
    <img src="{{ site.url }}/assets/images/ph11.jpeg" alt="Photo 11">
  </a>

   <a href="#" onclick="openLight('{{ site.url }}/assets/images/ph12.jpeg'); return false;">
    <img src="{{ site.url }}/assets/images/ph12.jpeg" alt="Photo 12">
  </a>

   <a href="#" onclick="openLight('{{ site.url }}/assets/images/ph13.jpeg'); return false;">
    <img src="{{ site.url }}/assets/images/ph13.jpeg" alt="Photo 13">
  </a>

   <a href="#" onclick="openLight('{{ site.url }}/assets/images/ph14.jpeg'); return false;">
    <img src="{{ site.url }}/assets/images/ph14.jpeg" alt="Photo 14">
  </a>

   <a href="#" onclick="openLight('{{ site.url }}/assets/images/ph15.jpeg'); return false;">
    <img src="{{ site.url }}/assets/images/ph15.jpeg" alt="Photo 15">
  </a>

   <a href="#" onclick="openLight('{{ site.url }}/assets/images/ph16.jpeg'); return false;">
    <img src="{{ site.url }}/assets/images/ph16.jpeg" alt="Photo 16">
  </a>

   <a href="#" onclick="openLight('{{ site.url }}/assets/images/ph17.jpeg'); return false;">
    <img src="{{ site.url }}/assets/images/ph17.jpeg" alt="Photo 17">
  </a>

   <a href="#" onclick="openLight('{{ site.url }}/assets/images/ph18.jpeg'); return false;">
    <img src="{{ site.url }}/assets/images/ph18.jpeg" alt="Photo 18">
  </a>

   <a href="#" onclick="openLight('{{ site.url }}/assets/images/ph19.jpeg'); return false;">
    <img src="{{ site.url }}/assets/images/ph19.jpeg" alt="Photo 19">
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