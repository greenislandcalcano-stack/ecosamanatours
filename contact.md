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
    <!-- ✅ This is the ONLY form on the page -->
    <form
      action="https://formspree.io/f/mananaqj"
      method="POST"
      class="contact-form"
    >
      <!-- optional subject line -->
      <input type="hidden" name="_subject" value="New inquiry from Eco-Samaná website">

      <div class="field">
        <label for="email">Your email*</label>
        <input id="email" type="email" name="email" required>
      </div>

      <div class="field">
        <label for="message">Your message*</label>
        <textarea id="message" name="message" rows="5" required></textarea>
      </div>

      <!-- simple spam honeypot -->
      <input type="text" name="_gotcha" style="display:none">

      <button type="submit" class="btn">Send</button>
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
.contact-form textarea {
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
