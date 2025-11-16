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

    {%- comment -%}
    Special layout for Boats & Catamarans: video + image grid
    Make sure the id in gallery.yml matches "boats-catamarans"
    {%- endcomment -%}
    {% if section.id == "boats-catamarans" %}
      <div class="gallery-media-row">
        <!-- Left: video column -->
        <div class="gallery-video-col">
          <h3>Video Highlights</h3>
          <div class="video-wrapper">
            <iframe
              src="https://www.youtube.com/embed/6ikHQZfu1JM"
              title="Eco-Samaná Boats & Catamarans Video"
              frameborder="0"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
              allowfullscreen>
            </iframe>
          </div>
        </div>

        <!-- Right: images from data file -->
        <div class="gallery-image-grid">
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
      </div>
    {% else %}
      <!-- Default layout for other sections: simple responsive grid -->
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
    {% endif %}
  </section>
  {% endfor %}
</div>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TouristAttraction",
  "name": "Eco-Samaná Tours Gallery",
  "description": "Stunning eco-tours in Samaná, Dominican Republic — whale watching, snorkeling, waterfalls, and secret beaches.",
  "image": [
    "{{ '/assets/images/catamaran-samana-01.jpg' | relative_url }}",
    "{{ '/assets/images/whale-watching-01.jpg' | relative_url }}",
    "{{ '/assets/images/waterfall-el-limon-01.jpg' | relative_url }}"
  ],
  "touristType": "Eco Tourism",
  "address": {
    "@type": "PostalAddress",
    "addressLocality": "Samaná",
    "addressCountry": "Dominican Republic"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 19.2056,
    "longitude": -69.3361
  }
}
</script>

<style>
/* --- Minimal, responsive gallery styles --- */
.gallery-toc {
  display: flex;
  flex-wrap: wrap;
  gap: .5rem;
  margin: 0 0 1rem 0;
}
.gallery-toc a {
  padding: .4rem .7rem;
  border: 1px solid var(--border, #ddd);
  border-radius: 999px;
  text-decoration: none;
  font-size: .95rem;
}

.gallery-wrap { --gap: .75rem; }
.gallery-section { margin: 2rem 0; }
.gallery-section h2 {
  margin: .5rem 0 1rem;
  font-size: clamp(1.25rem, 2vw, 1.6rem);
}

/* Default image grid for most sections */
.grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: var(--gap);
}
@media (min-width: 720px) {
  .grid { grid-template-columns: repeat(3, 1fr); }
}
@media (min-width: 1080px) {
  .grid { grid-template-columns: repeat(4, 1fr); }
}

.card {
  background: var(--card, #fff);
  border-radius: .75rem;
  overflow: hidden;
  border: 1px solid var(--border, #e5e5e5);
}
.card img {
  width: 100%;
  height: 220px;
  object-fit: cover;
  display: block;
}
.card figcaption {
  font-size: .9rem;
  padding: .5rem .6rem .7rem;
  color: #333;
}

/* Special layout for Boats & Catamarans: video + image grid */
.gallery-media-row {
  display: flex;
  flex-wrap: wrap;
  gap: 2rem;
}

.gallery-video-col {
  flex: 1 1 320px;
}

/* Right-side grid for boats images */
.gallery-image-grid {
  flex: 2 1 400px;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
  gap: 1.25rem;
}

/* Responsive 16:9 video wrapper */
.video-wrapper {
  position: relative;
  padding-bottom: 56.25%; /* 16:9 ratio */
  height: 0;
  overflow: hidden;
  border-radius: 16px;
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.08);
}

.video-wrapper iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  border: 0;
}

/* Optional thumbnail style if reused elsewhere */
.video-thumb {
  width: 100%;
  height: auto;
  border-radius: 16px;
  display: block;
}

/* Mobile adjustments */
@media (max-width: 768px) {
  .gallery-section h2 {
    text-align: center;
  }
  .gallery-media-row {
    flex-direction: column;
  }
}
  
/* Optional: light “zoom” behavior */
.gallery-wrap a { display: block; position: relative; }
.gallery-wrap a[href^="#"] { cursor: zoom-in; }
</style>

<script>
/* Simple behavior: opens images in a new tab */
document.querySelectorAll('.gallery-wrap a').forEach(a => {
  if (a.getAttribute('href')?.match(/\.(jpg|jpeg|png|webp|avif)(\?.*)?$/i)) {
    a.addEventListener('click', (e) => {
      e.preventDefault();
      window.open(a.getAttribute('href'), '_blank', 'noopener');
    });
  }
});
</script>
