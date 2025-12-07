---
layout: page
title: Publications
permalink: /publications/
order: 2
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Space+Mono&display=swap');

  /* --- 🌌 DEEP SPACE BACKGROUND 🌌 --- */
  body {
    background: radial-gradient(ellipse at bottom, #0b0d17 0%, #000000 100%);
    color: #a0a0a0;
    font-family: 'Space Mono', monospace;
    overflow-x: hidden;
  }

  /* Animated Stars */
  .stars {
    position: fixed; top: 0; left: 0; width: 100%; height: 100%;
    background: transparent; z-index: -1;
  }
  .stars::after {
    content: " "; position: absolute; top: 2000px; width: 1px; height: 1px;
    background: transparent;
    box-shadow: 100px 200px #FFF, 230px 400px #FFF, 500px 100px #FFF, 900px 1000px #FFF;
    animation: animStar 50s linear infinite;
  }
  @keyframes animStar { from { transform: translateY(-2000px); } to { transform: translateY(0px); } }

  /* --- 💻 LAPTOP FULL WIDTH FIX --- */
  @media screen and (min-width: 1000px) {
    .wrapper { max-width: 1400px !important; width: 92% !important; padding: 0 !important; }
  }

  /* --- TYPOGRAPHY --- */
  h2, h3 { 
    font-family: 'Orbitron', sans-serif; 
    color: #00d2ff; 
    text-transform: uppercase; 
    letter-spacing: 3px;
    text-shadow: 0 0 10px rgba(0, 210, 255, 0.4);
  }
  
  /* --- 🛸 HOLOGRAPHIC DATA CARDS --- */
  .pub-card {
    background: rgba(16, 20, 30, 0.7); /* See-through dark glass */
    backdrop-filter: blur(10px);        /* Blur effect behind it */
    border: 1px solid rgba(0, 210, 255, 0.2);
    padding: 30px;
    margin-bottom: 40px;
    position: relative;
    border-radius: 4px;
    transition: 0.3s;
    overflow: hidden;
  }

  .pub-card:hover {
    border-color: #00d2ff;
    box-shadow: 0 0 30px rgba(0, 210, 255, 0.15);
    transform: scale(1.01);
  }

  /* Tactical Corner Brackets */
  .pub-card::before {
    content: ""; position: absolute; top: 0; left: 0; width: 20px; height: 20px;
    border-top: 2px solid #ff00ff; border-left: 2px solid #ff00ff;
  }
  .pub-card::after {
    content: ""; position: absolute; bottom: 0; right: 0; width: 20px; height: 20px;
    border-bottom: 2px solid #ff00ff; border-right: 2px solid #ff00ff;
  }

  /* Status Tag */
  .status-tag {
    position: absolute; top: 15px; right: 15px;
    font-size: 0.6em; color: #555; font-family: 'Orbitron'; letter-spacing: 1px;
    border: 1px solid #333; padding: 2px 6px;
  }
  .pub-card:hover .status-tag { color: #00d2ff; border-color: #00d2ff; }

  /* Content Styling */
  .paper-title {
    font-family: 'Orbitron', sans-serif;
    font-size: 1.5em;
    color: #fff;
    display: block;
    margin-bottom: 15px;
    line-height: 1.4;
  }

  .authors { color: #888; font-style: italic; margin-bottom: 15px; display: block; }
  .authors strong { color: #ff00ff; font-weight: bold; }
  .journal-info { color: #00d2ff; font-weight: bold; margin-bottom: 20px; display: block; text-transform: uppercase; }

  /* --- 📟 TERMINAL "GIST" BOX --- */
  .terminal-log {
    background: #000;
    border-left: 3px solid #00d2ff;
    padding: 20px;
    font-family: 'Courier New', monospace;
    color: #ccc; 
    margin-top: 25px;
  }
  .terminal-log strong { color: #00d2ff; text-shadow: none; font-family: 'Orbitron'; font-size: 0.8em; }
  .terminal-log em { color: #ff9f43; font-style: normal; }

  /* --- 🔗 BUTTONS --- */
  .data-btn {
    display: inline-block;
    padding: 10px 20px;
    border: 1px solid #00d2ff;
    color: #00d2ff;
    font-family: 'Orbitron';
    font-size: 0.8em;
    margin-right: 15px;
    text-decoration: none;
    text-transform: uppercase;
    letter-spacing: 1px;
    transition: 0.3s;
    position: relative;
    overflow: hidden;
  }
  .data-btn:hover {
    background: #00d2ff;
    color: #000;
    box-shadow: 0 0 20px #00d2ff;
  }

  /* --- 🔙 NAV BUTTON --- */
  .nav-btn {
    display: inline-block; padding: 12px 25px; border: 2px solid #ff9f43;
    color: #ff9f43; font-family: 'Orbitron'; font-weight: bold; margin-bottom: 40px;
    text-transform: uppercase; letter-spacing: 2px; text-decoration: none;
  }
  .nav-btn:hover { background: #ff9f43; color: #000; box-shadow: 0 0 25px #ff9f43; }

</style>

<div class="stars"></div>

<a href="/" class="nav-btn">← Return to Base</a>

<div style="text-align: center; margin-bottom: 60px;">
  <h2>RESEARCH_DATABASE // DECRYPTED</h2>
  <p style="color: #666; font-size: 0.9em; letter-spacing: 1px;">"Proof that I spend my weekends calculating the end of the world."</p>
</div>

---

### // SYSTEM LOG: 2025

<div class="pub-card">
  <div class="status-tag">STATUS: PUBLISHED</div>
  <span class="paper-title">In Search of an Interaction in the Dark Sector through Gaussian Process and ANN Approaches</span>
  
  <span class="journal-info">MNRAS (The Royal Astronomical Society)</span>
  
  <span class="authors">
    <strong>Mazaharul Abedin</strong>, Guo-Jian Wang, Yin-Zhe Ma, Supriya Pan
  </span>
  
  <div style="margin-top: 15px;">
    <a href="https://doi.org/10.1093/mnras/staf762" class="data-btn">📡 Access DOI</a>
    <a href="https://arxiv.org/abs/2505.04336" class="data-btn">📄 ArXiv Data</a>
  </div>

  <div class="terminal-log">
    <strong>> EXEC_SUMMARY:</strong><br>
    We deployed <em>Artificial Neural Networks</em> to spy on the Universe. The goal? To find out if Dark Matter and Dark Energy are secretly gossiping (interacting) behind our backs.<br><br>
    <strong>> RESULT:</strong><br>
    Interaction detected. Standard Cosmology models are currently panicking.
  </div>
</div>

<div class="pub-card">
  <div class="status-tag">STATUS: PREPRINT</div>
  <span class="paper-title">When Dark Matter Heats Up: A Model-Independent Search for Non-Cold Behavior</span>
  
  <span class="journal-info">Preprint / ArXiv</span>
  
  <span class="authors">
    <strong>Mazaharul Abedin</strong>, Luis A. Escamilla, Supriya Pan, Eleonora Di Valentino, Weiqiang Yang
  </span>
  
  <div style="margin-top: 15px;">
    <a href="https://arxiv.org/abs/2505.09470" class="data-btn">📄 ArXiv Data</a>
  </div>

  <div class="terminal-log">
    <strong>> EXEC_SUMMARY:</strong><br>
    Everyone assumes Dark Matter is "Cold" (slow and boring). We checked if maybe it has some <em>pressure</em> (is it getting hot in here?) using model-independent reconstruction.<br><br>
    <strong>> RESULT:</strong><br>
    Evidence is mild, but we can't rule it out. Dark Matter remains the Universe's most annoying mystery.
  </div>
</div>

---

<div style="text-align: center; margin-top: 50px;">
  <a href="/" class="nav-btn">← Return to Base</a>
</div>
