---
layout: home
title: Home
order: 1
---

<style>
  /* --- 🌌 GLOBAL COSMIC THEME 🌌 --- */
  body {
    background-color: #0b0d17; /* Deep Space Black */
    background-image: 
      radial-gradient(white, rgba(255,255,255,.2) 2px, transparent 3px),
      radial-gradient(white, rgba(255,255,255,.15) 1px, transparent 2px),
      radial-gradient(white, rgba(255,255,255,.1) 2px, transparent 3px);
    background-size: 550px 550px, 350px 350px, 250px 250px;
    background-position: 0 0, 40px 60px, 130px 270px;
    color: #e0e6ed;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }

  /* --- WIDE LAYOUT FIX --- */
  @media screen and (min-width: 1000px) {
    .wrapper {
      max-width: 1400px !important;
      width: 90% !important;
      padding: 0 !important;
    }
  }

  /* --- TYPOGRAPHY & NEON ACCENTS --- */
  h1, h2, h3 { 
    color: #4db5ff; /* Cyan Neon */
    text-shadow: 0 0 10px rgba(77, 181, 255, 0.5);
    letter-spacing: 1px;
  }
  strong { color: #ff9f43; } /* Orange Neon */
  a { color: #ff9f43; text-decoration: none; transition: all 0.3s; }
  a:hover { color: #fff; text-shadow: 0 0 10px #ff9f43; text-decoration: none; }

  /* --- 🚀 HERO SECTION (Sci-Fi Dashboard) --- */
  .hero-banner {
    background: rgba(16, 20, 35, 0.8);
    border: 1px solid #4db5ff;
    border-radius: 15px;
    padding: 60px 40px;
    text-align: center;
    position: relative;
    overflow: hidden;
    margin-bottom: 50px;
    box-shadow: 0 0 30px rgba(77, 181, 255, 0.2);
    backdrop-filter: blur(5px);
  }

  /* The "Hologram" Effect */
  .hero-banner::before {
    content: "";
    position: absolute;
    top: 0; left: 0; right: 0; height: 2px;
    background: linear-gradient(90deg, transparent, #4db5ff, transparent);
    animation: scanline 4s infinite linear;
  }

  @keyframes scanline {
    0% { top: 0; opacity: 1; }
    100% { top: 100%; opacity: 0; }
  }

  .hero-banner h1 { font-size: 3em; margin-bottom: 10px; }
  .hero-banner p { font-size: 1.2em; line-height: 1.6; color: #b3c5d5; }

  /* --- 🧪 RESEARCH MODULES (Card Style) --- */
  .box {
    background: rgba(255, 255, 255, 0.05);
    border-left: 4px solid #ff9f43;
    padding: 25px;
    margin-bottom: 25px;
    border-radius: 0 10px 10px 0;
    transition: transform 0.3s ease;
  }
  .box:hover {
    transform: translateX(10px); /* Slide effect */
    background: rgba(255, 255, 255, 0.1);
  }

  /* --- 🛠 TECH TAGS (Cyberpunk Chips) --- */
  .tech-tag {
    background: #1e272e;
    border: 1px solid #4db5ff;
    color: #4db5ff;
    padding: 5px 12px;
    border-radius: 20px;
    font-family: 'Courier New', monospace;
    font-size: 0.9em;
    display: inline-block;
    margin: 5px;
    box-shadow: 0 0 5px rgba(77, 181, 255, 0.3);
  }
  .tech-tag:hover {
    background: #4db5ff;
    color: #000;
    cursor: default;
  }

  /* --- 🔘 BUTTONS (Sci-Fi UI) --- */
  .btn-container { text-align: center; margin: 50px 0; }
  
  .btn-pub {
    position: relative;
    display: inline-block;
    padding: 15px 40px;
    color: #4db5ff;
    font-weight: bold;
    text-transform: uppercase;
    letter-spacing: 2px;
    text-decoration: none;
    font-size: 1.1em;
    overflow: hidden;
    transition: 0.2s;
    border: 2px solid #4db5ff;
    background: transparent;
    z-index: 1;
  }

  .btn-pub:hover {
    color: #111;
    background: #4db5ff;
    box-shadow: 0 0 40px #4db5ff;
  }

  /* --- 🎩 COMEDY FOOTER (Fun Twist) --- */
  .fun-fact {
    text-align: center;
    font-style: italic;
    color: #888;
    margin-top: 50px;
    font-size: 0.9em;
    border-top: 1px solid #333;
    padding-top: 20px;
  }

  /* --- 📨 FLOATING CONTACT (Orange Orb) --- */
  .email-widget {
    position: fixed;
    bottom: 30px;
    right: 30px;
    width: 65px;
    height: 65px;
    background: #ff9f43;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    box-shadow: 0 0 20px rgba(255, 159, 67, 0.6);
    transition: transform 0.3s;
    z-index: 999;
  }
  .email-widget:hover { transform: scale(1.2) rotate(10deg); background: #fff; }
  .email-icon { width: 30px; height: 30px; fill: #000; }

</style>

<div class="hero-banner">
  <h1>Hi, I'm Mazaharul 👋</h1>
  <p>
    <strong>PhD Research Scholar | Presidency University, Kolkata</strong>
    <br><br>
    Parsing the Universe, one equation at a time. I blend <strong>Theoretical Physics</strong> with <strong>Astronomical Data</strong> to figure out why the Universe is accelerating (and why Dark Energy is being so mysterious).
  </p>
</div>

---

### 🔭 Mission Control (Research Domain)
My primary objective is **Observational Cosmology**. I use data to act as a detective for the Universe's history.

<div class="box">
  <h3>⚡ Key Focus Areas</h3>
  <ul>
    <li><strong>Hunting Dark Energy:</strong> Reconstructing Hubble parameters to understand cosmic acceleration.</li>
    <li><strong>Letting Data Speak:</strong> Using <em>Machine Learning</em> & <em>Gaussian Processes</em> instead of guessing models.</li>
    <li><strong>Stress-Testing ΛCDM:</strong> Checking if the standard model holds up against new data (SNe Ia, DESI-BAO, CMB).</li>
  </ul>
</div>

---

### 📜 The Archives (Publications)
Documenting the expansion history of the universe.

<div class="btn-container">
  <a href="/publications/" class="btn-pub">Access Publication Data</a>
</div>

---

### 💻 The Toolkit (Methodology)

I don't just use math; I use computational brute force. My workflow involves Bayesian inference, MCMC sampling, and teaching computers to find patterns in the stars.

<div style="text-align: center;">
  <span class="tech-tag">Gaussian Processes</span>
  <span class="tech-tag">JAX</span>
  <span class="tech-tag">NumPyro</span>
  <span class="tech-tag">Artificial Neural Networks</span>
  <span class="tech-tag">CLASS</span>
  <span class="tech-tag">MontePython</span>
  <span class="tech-tag">Cobaya</span>
  <span class="tech-tag">MCMC</span>
</div>

---

### 🎭 The Human Element
When I'm not calculating the fate of the universe, I'm usually laughing at it.

Inspired by the physical comedy of **Charlie Chaplin** and **Mr. Bean**, I believe that life—like physics—requires a good sense of timing and a bit of absurdity.

<div class="btn-container">
  <a href="/gallery/" class="btn-pub" style="border-color: #ff9f43; color: #ff9f43;">View Life & Gallery</a>
</div>

<div class="fun-fact">
  "Life is a tragedy when seen in close-up, but a comedy in long-shot." — Charlie Chaplin
  <br>(And a mystery when seen through a telescope.)
</div>

<br><br>

<a href="mailto:mazaharul.rs@presiuniv.ac.in" class="email-widget" title="Send a Signal">
  <svg class="email-icon" viewBox="0 0 24 24">
    <path d="M20 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/>
  </svg>
</a>
