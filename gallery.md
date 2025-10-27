---
layout: page
title: "Samaná Eco-Tour Gallery | Whales, Waterfalls & Beaches"
permalink: /gallery/
description: "Explore stunning eco-tours in Samaná — whale watching, waterfalls, mangroves, secret beaches, snorkeling, and catamaran adventures. Discover paradise in the Dominican Republic."
keywords: "Samaná eco tours, Dominican Republic travel, whale watching Samaná, El Limón waterfall, mangrove kayaking, snorkeling Samaná, hidden beaches Dominican Republic"
image: /assets/images/catamaran-samana-01.jpg
---

<nav class="gallery-toc">
  {% for section in site.data.gallery.sections %}
    <a href="#{{ section.id }}">{{ section.title }}</a>
  {% endfor %}
</nav>

<div class="gallery-wrap">
  {% for section in site.data.gallery.sections %}
  <section id="{{ section.id }}" class="gallery-section">
    <h2>{{ section.title }}</h2>
    <div class="grid">
      {% for item in section.items %}
      <figure class="card">
        
        <a href="{{ item.src | relative_url }}">
  <img
    loading="lazy"
    src="{{ (item.thumb | default: item.src) | relative_url }}"
    alt="{{ item.alt | escape }}"
  >
</a>

       
        {% if item.caption %}
          <figcaption>{{ item.caption }}</figcaption>
        {% endif %}
      </figure>
      {% endfor %}
    </div>
  </section>
  {% endfor %}
</div>

<style>
/* --- Minimal, responsive gallery styles --- */
.gallery-toc {
  display:flex;
  flex-wrap:wrap;
  gap:.5rem;
  margin: 0 0 1rem 0;
}
.gallery-toc a {
  padding:.4rem .7rem;
  border:1px solid var(--border, #ddd);
  border-radius:999px;
  text-decoration:none;
  font-size:.95rem;
}

.gallery-wrap { --gap: .75rem; }
.gallery-section { margin: 2rem 0; }
.gallery-section h2 { margin: .5rem 0 1rem; font-size: clamp(1.25rem, 2vw, 1.6rem); }

.grid {
  display:grid;
  grid-template-columns: repeat(2, 1fr);
  gap: var(--gap);
}
@media (min-width: 720px) { .grid { grid-template-columns: repeat(3, 1fr); } }
@media (min-width: 1080px){ .grid { grid-template-columns: repeat(4, 1fr); } }

.card {
  background: var(--card, #fff);
  border-radius: .75rem;
  overflow:hidden;
  border: 1px solid var(--border, #e5e5e5);
}
.card img {
  width:100%;
  height: 220px;
  object-fit: cover;
  display:block;
}
.card figcaption {
  font-size:.9rem;
  padding:.5rem .6rem .7rem;
  color:#333;
}

/* Optional: light “zoom” behavior */
.gallery-wrap a { display:block; position:relative; }
.gallery-wrap a[href^="#"]{ cursor: zoom-in; }
</style>

<script>
/* Simple behavior: opens images in a new tab */
document.querySelectorAll('.gallery-wrap a').forEach(a=>{
  a.addEventListener('click', (e)=>{
    if (a.getAttribute('href')?.match(/\.(jpg|jpeg|png|webp|avif)(\?.*)?$/i)) {
      e.preventDefault();
      window.open(a.getAttribute('href'), '_blank', 'noopener');
    }
  });
});
</script>

 
