---
layout: page
title: "Contact Eco-Samaná Adventures | Tours & Reservations"
permalink: /contact/
description: "Contact Eco-Samaná Adventures for tour reservations, questions about whale watching, El Limón waterfall, snorkeling, eco-buggies and more in Samaná."
---

<section class="contact-page container" aria-labelledby="contactTitle">
  <header class="contact-hero">
    <h1 id="contactTitle">Plan Your Eco Adventure in Samaná</h1>
    <p class="lead">
      Whale watching, waterfalls, jungle tours & private adventures in Samaná.
      We reply fast and help you choose the perfect experience for your trip.
    </p>

    <a
      class="btn-whatsapp"
      href="https://wa.me/15046572553?text=Hello%20Eco-Samana%20Adventures!%20I%E2%80%99d%20like%20to%20book%20a%20tour%20in%20Samana.%20What%20availability%20do%20you%20have%3F"
      target="_blank"
      rel="noopener"
      id="whatsappPrimary"
      aria-label="Chat on WhatsApp (fast reply)"
    >
      <span class="wa-dot" aria-hidden="true"></span>
      Chat on WhatsApp – Fast Reply
    </a>

    <p class="contact-note">📲 Most travelers contact us via WhatsApp for quick answers and availability.</p>

    <div class="trust-grid" role="list" aria-label="Why book with us">
      <div class="trust-item" role="listitem">✔ Local guides</div>
      <div class="trust-item" role="listitem">✔ Eco-friendly & small groups</div>
      <div class="trust-item" role="listitem">✔ Real nature experiences</div>
      <div class="trust-item" role="listitem">✔ Personalized attention</div>
    </div>
  </header>

  <div class="contact-layout">
    <!-- Email form (secondary) -->
    <div class="contact-card" aria-labelledby="emailTitle">
      <h2 id="emailTitle">Prefer email?</h2>
      <p class="muted">Send us a message and we’ll get back to you shortly.</p>

      <form
        action="https://formspree.io/f/mananaqj"
        method="POST"
        class="contact-form"
        id="contactForm"
      >
        <input type="hidden" name="_subject" value="New inquiry from Eco-Samaná website">

        <div class="field">
          <label for="email">Your email*</label>
          <input id="email" type="email" name="email" required autocomplete="email" placeholder="your@email.com">
        </div>

        <div class="field">
          <label for="message">Your message*</label>
          <textarea id="message" name="message" rows="5" required placeholder="Tell us your dates, group size, and which tour you want…"></textarea>
        </div>

        <input type="text" name="_gotcha" style="display:none">

        <button type="submit" class="btn">Send Message</button>
        <p class="fineprint">Tip: Include travel dates + group size for faster booking.</p>
      </form>
    </div>

    <aside class="contact-info" aria-labelledby="otherWaysTitle">
      <h2 id="otherWaysTitle">Other Ways to Reach Us</h2>

      <p class="contact-line">
        <strong>Email:</strong>
        <a href="mailto:ecosamanadventures@gmail.com?subject=Eco-Saman%C3%A1%20Tour%20Inquiry">ecosamanadventures@gmail.com</a>
      </p>

      <p class="contact-line">
        <strong>WhatsApp:</strong>
        <a
          href="https://wa.me/15046572553?text=Hello%20Eco-Samana%20Adventures!%20I%E2%80%99d%20like%20to%20book%20a%20tour%20in%20Samana."
          target="_blank"
          rel="noopener"
          id="whatsappSecondary"
        >+1 (504) 657-2553</a>
      </p>

      <p class="contact-line"><strong>Location:</strong> Samaná, Dominican Republic</p>

      <div class="season-box">
        <p class="season-title">🐋 Whale Watching Season</p>
        <p class="muted">January – March</p>
        <p class="muted">Tours available year-round</p>
      </div>
    </aside>
  </div>
</section>

<!-- Sticky WhatsApp button -->
<a
  class="wa-sticky"
  href="https://wa.me/15046572553?text=Hello%20Eco-Samana%20Adventures!%20I%E2%80%99d%20like%20to%20book%20a%20tour%20in%20Samana."
  target="_blank"
  rel="noopener"
  id="whatsappSticky"
  aria-label="Chat with us on WhatsApp"
>
  <span class="wa-sticky-icon" aria-hidden="true">💬</span>
  <span class="wa-sticky-text">WhatsApp</span>
</a>

<style>
/* Layout */
.contact-hero{ text-align:center; padding: 0.75rem 0 0; }
.contact-layout{
  display:grid;
  grid-template-columns: minmax(0, 2fr) minmax(0, 1.3fr);
  gap: 2rem;
  margin-top: 1.25rem;
}
@media (max-width: 768px){ .contact-layout{ grid-template-columns: 1fr; } }

/* WhatsApp primary button */
.btn-whatsapp{
  display:inline-flex;
  align-items:center;
  justify-content:center;
  gap:10px;
  padding: 14px 16px;
  border-radius: 14px;
  text-decoration:none;
  font-weight: 800;
  font-size: 1.05rem;
  background: linear-gradient(180deg, #25D366, #1fb65a);
  color: #08210f;
  box-shadow: 0 14px 30px rgba(37,211,102,.25);
  border: 1px solid rgba(0,0,0,.12);
}
.btn-whatsapp:focus{ outline:3px solid rgba(37,211,102,.55); outline-offset:3px; }

.wa-dot{
  width:10px; height:10px; border-radius:999px;
  background: rgba(0,0,0,.25);
  box-shadow: 0 0 0 0 rgba(37,211,102,.6);
  animation: pulse 1.8s infinite;
}
@keyframes pulse{
  0%{ box-shadow: 0 0 0 0 rgba(37,211,102,.55); }
  70%{ box-shadow: 0 0 0 14px rgba(37,211,102,0); }
  100%{ box-shadow: 0 0 0 0 rgba(37,211,102,0); }
}

.contact-note{ margin:.7rem 0 1rem; opacity:.9; }

/* Trust bullets */
.trust-grid{
  display:grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: .6rem;
  max-width: 760px;
  margin: 0 auto 1rem;
  text-align:left;
}
@media (max-width: 640px){ .trust-grid{ grid-template-columns: 1fr; } }
.trust-item{
  border:1px solid rgba(0,0,0,.08);
  background: rgba(0,0,0,.03);
  padding: .7rem .8rem;
  border-radius: 12px;
}

/* Cards */
.contact-card, .contact-info{
  border:1px solid rgba(0,0,0,.08);
  background: rgba(0,0,0,.02);
  border-radius: 14px;
  padding: 1rem;
}
.muted{ opacity:.8; margin:.25rem 0 .75rem; }
.fineprint{ font-size:.9rem; opacity:.8; margin: .5rem 0 0; }

/* Form styling (keeps your current vibe) */
.contact-form .field{ margin-bottom: 1rem; }
.contact-form label{ display:block; font-weight: 600; margin-bottom: .25rem; }
.contact-form input,
.contact-form textarea{
  width:100%;
  padding:.6rem .65rem;
  border-radius:.6rem;
  border:1px solid #d4d4d4;
  font: inherit;
}
.contact-form button.btn{ margin-top: .25rem; }

/* Right column */
.contact-line{ margin: .5rem 0; }
.season-box{
  margin-top: 1rem;
  padding: .85rem;
  border-radius: 12px;
  border: 1px dashed rgba(0,0,0,.18);
  background: rgba(37,211,102,.06);
}
.season-title{ margin:0 0 .2rem; font-weight:800; }

/* Sticky WhatsApp */
.wa-sticky{
  position: fixed;
  right: 16px;
  bottom: 16px;
  z-index: 9999;
  display: inline-flex;
  align-items: center;
  gap: 10px;
  padding: 12px 14px;
  border-radius: 999px;
  background: linear-gradient(180deg, #25D366, #1fb65a);
  color: #08210f;
  text-decoration: none;
  font-weight: 900;
  box-shadow: 0 16px 34px rgba(37,211,102,.28);
  border: 1px solid rgba(0,0,0,.12);
}
.wa-sticky:focus{ outline:3px solid rgba(37,211,102,.55); outline-offset:3px; }
.wa-sticky-icon{ font-size: 18px; }
.wa-sticky-text{ font-size: 16px; }
@media (max-width: 640px){ .wa-sticky-text{ display:none; } }
</style>

<script>
/* GA4 events (only if gtag exists) */
function trackGA(eventName, params){
  try{ if (typeof gtag === "function") gtag("event", eventName, params || {}); }catch(e){}
}

document.getElementById("whatsappPrimary")?.addEventListener("click", () => {
  trackGA("whatsapp_click", { placement: "contact_primary" });
});
document.getElementById("whatsappSecondary")?.addEventListener("click", () => {
  trackGA("whatsapp_click", { placement: "contact_secondary" });
});
document.getElementById("whatsappSticky")?.addEventListener("click", () => {
  trackGA("whatsapp_click", { placement: "sticky_button" });
});
document.getElementById("contactForm")?.addEventListener("submit", () => {
  trackGA("contact_form_submit", { page: "contact" });
});
</script>


.contact-info h2 {
  margin-top: 0;
}
</style>
