---
layout: page
title: Contact / Book
permalink: /contact/
description: Reach out to plan your eco-adventure in Samaná.
---

<!-- Contact cards -->
<div class="card-grid mt-2">
  <div class="card">
    <h3>WhatsApp</h3>
    <p><a class="btn" href="https://wa.me/15046572553" target="_blank" rel="noopener">+1 (504) 657-2553</a></p>
  </div>
  <div class="card">
    <h3>Email</h3>
    <p><a class="btn" href="mailto:{{ site.email | default: 'ecalcano@eco-samana.com' }}">{{ site.email | default: 'ecalcano@eco-samana.com' }}</a></p>
  </div>
  <div class="card">
    <h3>Instagram</h3>
    <p><a class="btn" href="{{ site.social.instagram }}" target="_blank" rel="noopener">Follow @Eco_Samana</a></p>
  </div>
</div>

## Quick message
<form name="contact" method="POST" data-netlify="true">
  <p><label>Your Name<br><input type="text" name="name" required></label></p>
  <p><label>Email<br><input type="email" name="email" required></label></p>
  <p><label>Phone / WhatsApp<br><input type="tel" name="phone"></label></p>
  <p><label>Message<br><textarea name="message" rows="5" required></textarea></label></p>
  <p><button class="btn" type="submit">Send</button></p>
</form>

## Find us
<p class="text-center">
  <img class="hero-image" src="{{ '/assets/images/misc/map-placeholder.jpg' | relative_url }}" alt="Map of Samaná" loading="lazy">
  <br><em>Santa Bárbara de Samaná, Dominican Republic</em>
</p>
