---
layout: page
title: "Eco-Samaná Adventures Gallery | Whales, Waterfalls & Beaches"
permalink: /gallery/
description: "Explore stunning eco-tours in Samaná — whale watching, waterfalls, mangroves, secret beaches, snorkeling, and catamaran adventures."
keywords: "Eco Samaná Adventures, Dominican Republic travel, whale watching Samaná, El Limón waterfall, mangrove kayaking, snorkeling Samaná, hidden beaches Dominican Republic"
image: /assets/images/docking-samana-3.jpg
---

# Eco-Samaná Adventures Gallery  
*A visual journey through our beautiful peninsula — whales, waterfalls, hidden beaches, family adventures & island life.*

Welcome, explorer 🌊  
This gallery is organized in curated sections. Each one represents a different side of Samaná — its people, its oceans, its forests, and the small stories we share with guests.

Use the quick navigation below:

<nav class="gallery-toc">
  {% for section in site.data.gallery.sections %}
    <a href="#{{ section.id }}">{{ section.title }}</a>
  {% endfor %}
</nav>

<div class="gallery-wrap">
{% for section in site.data.gallery.sections %}

---

<section id="{{ section.id }}" class="gallery-section">
  <h2>{{ section.title }}</h2>

  {% if section.id == "whales" %}
  <p class="section-desc">
    Every winter, Samaná becomes the stage of one of Earth’s greatest migrations:  
    **thousands of humpback whales** arrive to breed, sing, and raise their newborn calves.  
    These images capture tender encounters — tails, jumps, close contacts — moments our guests never forget.
  </p>
  {% endif %}

  {% if section.id == "waterfalls" %}
  <p class="section-desc">
    Deep inside the green mountains lies **El Limón Waterfall**, a 50-meter cascade surrounded by tropical forest.  
    Horses, jungle paths, smiling local guides, natural pools — this is one of Samaná’s most iconic adventures.
  </p>
  {% endif %}

  {% if section.id == "beaches" %}
  <p class="section-desc">
    Secret beaches, turquoise coves, golden sands, and untouched corners of the peninsula.  
    These photos show the “hidden Samaná” we take travelers to — quiet, dreamy, postcard-perfect.
  </p>
  {% endif %}
<section class="tour-gallery">

<h2 class="tour-gallery-title">Cayo Levantado Experience</h2>

<div class="tour-gallery-grid">

<img src="/assets/images/cayo-levantado-drone.jpg" alt="Cayo Levantado aerial view Samana">

<img src="/assets/images/cayo-levantado-beach.jpg" alt="Cayo Levantado white sand beach">

<img src="/assets/images/cayo-levantado-palms.jpg" alt="Palm trees Cayo Levantado beach">

<img src="/assets/images/cayo-levantado-samana-bay.jpg" alt="Samana bay view from Cayo Levantado">

<img src="/assets/images/cayo-levantado-paradise.jpg" alt="Cayo Levantado tropical paradise">

</div>

</section>
  {% if section.id == "boats-catamarans" %}
  <p class="section-desc">
    Our boats explore Samaná Bay, Los Haitises National Park, Cayo Levantado, and remote islands.  
    Here's a blend of videos, catamarans, docking adventures, and ocean moments we love.
  </p>
  {% endif %}

  {% if section.id == "samana-life" %}
  <p class="section-desc">
    A tribute to daily life in Samaná — fishermen docking at sunrise, colorful churches, rural trails,  
    children waving from the pier, coffee farmers, and the warm soul of our community.
  </p>
  {% endif %}

  {% if section.id == "buggies" %}
  <p class="section-desc">
    The Eco-Buggy trails take travelers through rivers, cacao farms, rural communities, and hilltop views.  
    Mud, dust, laughter — pure Caribbean adrenaline mixed with Dominican countryside charm.
  </p>
  {% endif %}

  {% if section.id == "caves" %}
  <p class="section-desc">
    Samaná’s coastline hides old Taíno caves, soft-sand caverns, and mangrove tunnels.  
    Each photo whispers old stories carved by wind, waves, and ancient cultures.
  </p>
  {% endif %}

  {% if section.id == "boats-catamarans" %}
  <!-- Special Boats & Catamarans Layout -->
  <div class="gallery-media-row">
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

    <div class="gallery-image-grid">
      {% for item in section.items %}
      <figure class="card">
        <a href="{{ item.src | relative_url }}">
          <img
            loading="lazy"
            src="{{ (item.thumb | default: item.src) | relative_url }}"
            alt="{{ item.alt | escape }}">
        </a>
        {% if item.caption %}
        <figcaption>{{ item.caption }}</figcaption>
        {% endif %}
      </figure>
      {% endfor %}
    </div>
  </div>

  {% else %}
  <!-- Normal grid layout -->
  <div class="grid">
    {% for item in section.items %}
    <figure class="card">
      <a href="{{ item.src | relative_url }}">
        <img
          loading="lazy"
          src="{{ (item.thumb | default: item.src) | relative_url }}"
          alt="{{ item.alt | escape }}">
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

<br><br>

---

# 📸 About This Gallery  
Every photograph here was taken in **Samaná, Dominican Republic**, during real Eco-Samaná excursions, community visits, and field explorations.  
We keep expanding this collection to show the heart of our region — its nature, its people, its colors.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "ImageGallery",
  "name": "EcoSamana Adventures Gallery",
  "description": "Photo gallery of whale watching, waterfalls, beaches, boats, catamarans, and eco-adventures in Samaná, Dominican Republic.",
  "image": [
    "{{ '/assets/images/whale-watching-01.jpg' | relative_url }}",
    "{{ '/assets/images/waterfall-el-limon-01.jpg' | relative_url }}",
    "{{ '/assets/images/catamaran-samana-01.jpg' | relative_url }}",
    "{{ '/assets/images/galleria/heart-of-samana.jpg' | relative_url }}",
    "{{ '/assets/images/galleria/samana-ranch-el-limon.jpg' | relative_url }}"
  ],
  "author": {
    "@type": "Organization",
    "name": "EcoSamana Adventures"
  },
  "contentLocation": {
    "@type": "Place",
    "name": "Samaná, Dominican Republic"
  }
}
</script>


