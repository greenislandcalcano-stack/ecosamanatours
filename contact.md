---
layout: page
title: "Contact Eco-Samaná Adventures | Tours & Reservations"
permalink: /contact/
description: "Contact Eco-Samaná Adventures for tour reservations, questions about whale watching, El Limón waterfall, snorkeling, eco-buggies and more in Samaná."
---

<section class="contact-page container">
  <h1>Contact Eco-Samaná Adventures</h1>
  <p class="lead">
    Send us a message about tour reservations, custom group trips, or any questions
    you have about Samaná. We’ll get back to you as soon as possible.
  </p>

  <div class="contact-layout">
    <form
      action="https://formspree.io/f/mananaqj)"
      method="POST"
      class="contact-form"
    >
      <!-- replace YOUR_FORMSPREE_ID with the ID from your Formspree dashboard -->

      <!-- optional: subject line for the email -->
      <input type="hidden" name="_subject" value="New inquiry from Eco-Samaná website">

      <div class="field">
        <label for="name">Your Name*</label>
        <input id="name" name="name" type="text" required>
      </div>

      <div class="field">
        <label for="email">Your Email*</label>
        <input id="email" name="email" type="email" required>
      </div>

      <div class="field">
        <label for="phone">WhatsApp / Phone (optional)</label>
        <input id="phone" name="phone" type="text">
      </div>

      <div class="field">
        <label for="tour">Interested in</label>
        <select id="tour" name="tour">
          <option value="">Choose a tour (optional)</option>
          <option>Whale Watching</option>
          <option>El Limón Waterfall</option>
          <option>Treasure Hunt & Snorkeling</option>
          <option>Eco-Buggies & Beach</option>
          <option>Caves & Boating</option>
          <option>Other / Custom Trip</option>
        </select>
      </div>

      <div class="field">
        <label for="message">Message*</label>
        <textarea id="message" name="message" rows="5" required></textarea>
      </div>

      <!-- simple spam honeypot -->
      <input type="text" name="_gotcha" style="display:none">

      <!-- where to redirect after successful submit (optional) -->
      <!-- <input type="hidden" name="_redirect" value="https://eco-samana.com/thank-you/"> -->

      <button type="submit" class="btn">Send Message</button>
    </form>

    <aside class="contact-info">
      <h2>Other Ways to Reach Us</h2>
      <p><strong>Email:</strong> ecosamanaadventures@gmail.com</p>
      <p><strong>WhatsApp:</strong> <a href="https://wa.me/15046572553">+1 (504) 657-2553</a></p>
      <p><strong>Location:</strong> Samaná, Dominican Republic</p>
    </aside>
  </div>
</section>

<style>
.contact-layout {
  display: grid;
  grid-template-columns: minmax(0, 2fr) minmax(0, 1.3fr);
  gap: 2rem;
  margin-top: 1.5rem;
}
@media (max-width: 768px) {
  .contact-layout {
    grid-template-columns: 1fr;
  }
}

.contact-form .field {
  margin-bottom: 1rem;
}
.contact-form label {
  display: block;
  font-weight: 600;
  margin-bottom: .25rem;
}
.contact-form input,
.contact-form textarea,
.contact-form select {
  width: 100%;
  padding: .5rem .6rem;
  border-radius: .5rem;
  border: 1px solid #d4d4d4;
  font: inherit;
}
.contact-form button.btn {
  margin-top: .5rem;
}

.contact-info h2 {
  margin-top: 0;
}
</style>
