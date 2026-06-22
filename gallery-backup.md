<div class="gallery-wrap">
{% for section in site.data.gallery.sections %}

<section id="{{ section.id }}" class="gallery-section reveal-up">
  <h2>{{ section.title }}</h2>

  {% if section.id == "whales" %}
  <p class="section-desc">
    Every winter, Samaná becomes the stage of one of Earth’s greatest migrations:
    <strong>thousands of humpback whales</strong> arrive to breed, sing, and raise their newborn calves.
    These images capture tender encounters — tails, jumps, close contacts — moments our guests never forget.
  </p>
  {% endif %}

  {% if section.id == "waterfalls" %}
  <p class="section-desc">
    Deep inside the green mountains lies <strong>El Limón Waterfall</strong>, a 50-meter cascade surrounded by tropical forest.
    Horses, jungle paths, smiling local guides, natural pools — this is one of Samaná’s most iconic adventures.
  </p>
  {% endif %}

  {% if section.id == "beaches" %}
  <p class="section-desc">
    Secret beaches, turquoise coves, golden sands, and untouched corners of the peninsula.
    These photos show the hidden Samaná we love sharing — quiet, dreamy, and postcard-perfect.
  </p>
  {% endif %}

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

{% if section.id == "beaches" %}
<section class="tour-gallery cayo-levantado-feature reveal-up">
  <div class="feature-head">
    <span class="feature-kicker">Island Escape</span>
    <h2 class="tour-gallery-title">Cayo Levantado Experience</h2>
    <p class="section-desc">
      A dreamy island jewel in Samaná Bay — white sand, palms, turquoise water, and postcard views in every direction.
    </p>
  </div>

  <div class="tour-gallery-grid">
    <figure class="card">
      <img src="/assets/images/cayo-levantado-drone.jpg" alt="Cayo Levantado aerial view Samana">
    </figure>
    <figure class="card">
      <img src="/assets/images/cayo-levantado-beach.jpg" alt="Cayo Levantado white sand beach">
    </figure>
    <figure class="card">
      <img src="/assets/images/cayo-levantado-palms.jpg" alt="Palm trees Cayo Levantado beach">
    </figure>
    <figure class="card">
      <img src="/assets/images/cayo-levantado-samana-bay.jpg" alt="Samana bay view from Cayo Levantado">
    </figure>
    <figure class="card">
      <img src="/assets/images/cayo-levantado-paradise.jpg" alt="Cayo Levantado tropical paradise">
    </figure>
  </div>
</section>
{% endif %}

{% endfor %}
</div>
