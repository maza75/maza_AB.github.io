---
layout: page
title: Publications
permalink: /publications/
order: 2
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Space+Mono&family=vt323&display=swap');

  /* --- 🌌 GLOBAL SYSTEM SETTINGS 🌌 --- */
  body {
    background-color: #050505;
    background: radial-gradient(circle at center, #0b0d17 0%, #000000 100%);
    color: #a8b2d1;
    font-family: 'Space Mono', monospace;
    overflow-x: hidden;
    cursor: crosshair;
  }

  /* --- CRT SCANLINE OVERLAY --- */
  body::before {
    content: " ";
    display: block;
    position: fixed; top: 0; left: 0; bottom: 0; right: 0;
    background: linear-gradient(rgba(18, 16, 16, 0) 50%, rgba(0, 0, 0, 0.25) 50%), linear-gradient(90deg, rgba(255, 0, 0, 0.06), rgba(0, 255, 0, 0.02), rgba(0, 0, 255, 0.06));
    z-index: 9999;
    background-size: 100% 2px, 3px 100%;
    pointer-events: none;
  }

  /* --- WIDE LAYOUT FIX --- */
  @media screen and (min-width: 1000px) {
    .wrapper { max-width: 1400px !important; width: 92% !important; padding: 0 !important; }
  }

  /* --- HUD TOP BAR --- */
  .hud-bar {
    border-bottom: 1px solid #333;
    padding: 10px 0;
    margin-bottom: 30px;
    display: flex;
    justify-content: space-between;
    font-family: 'Orbitron', sans-serif;
    font-size: 0.8em;
    color: #555;
    text-transform: uppercase;
  }
  .hud-alert { color: #ff00ff; animation: blink 1s infinite; }
  @keyframes blink { 50% { opacity: 0; } }

  /* --- TYPOGRAPHY --- */
  h2, h3 { 
    font-family: 'Orbitron', sans-serif; 
    color: #00d2ff; 
    text-transform: uppercase; 
    letter-spacing: 2px;
  }
  
  /* --- 📂 DECRYPTED FILE CARDS --- */
  .pub-card {
    background: #0d0d12;
    border: 1px solid #1f1f2e;
    border-left: 4px solid #ff00ff;
    padding: 30px;
    margin-bottom: 40px;
    position: relative;
    transition: 0.3s;
  }
  .pub-card:hover {
    border-color: #00d2ff;
    box-shadow: 0 0 25px rgba(0, 210, 255, 0.15);
    transform: translateX(5px);
  }
  .pub-card::after {
    content: "ACCESS_GRANTED";
    position: absolute; top: 10px; right: 10px;
    font-family: 'Orbitron'; font-size: 0.6em; color: #00d2ff; opacity: 0.7;
  }

  .paper-title {
    font-size: 1.4em;
    font-weight: bold;
    color: #fff;
    display: block;
    margin-bottom: 10px;
    text-shadow: 0 0 5px rgba(255, 255, 255, 0.3);
  }

  .authors { color: #888; font-style: italic; margin-bottom: 15px; }
  .authors strong { color: #ff00ff; }

  /* --- 📟 TERMINAL HIGHLIGHTS --- */
  .terminal-box {
    background: #000;
    border: 1px dashed #333;
    padding: 20px;
    font-family: 'vt323', monospace;
    font-size: 1.2em;
    color: #0f0; /* Green Text */
    margin-top: 20px;
  }
  .terminal-box::before {
    content: "> RUN_SUMMARY.EXE";
    display: block; color: #555; font-size: 0.8em; margin-bottom: 10px; font-family: 'Space Mono';
  }
  .terminal-box strong { color: #00d2ff; }

  /* --- 🔗 BUTTONS --- */
  .data-link {
    display: inline-block;
    padding: 8px 16px;
    border: 1px solid #00d2ff;
    color: #00d2ff;
    font-family: 'Orbitron';
    font-size: 0.8em;
    margin-right: 10px;
    text-decoration: none;
    text-transform: uppercase;
    transition: 0.3s;
  }
  .data-link:hover {
    background: #00d2ff;
    color: #000;
    box-shadow: 0 0 15px #00d2ff;
  }

  /* --- 🔙 NAV BUTTON --- */
  .nav-btn {
    display: inline-block; padding: 10px 20px; border: 2px solid #ff9f43;
    color: #ff9f43; font-family: 'Orbitron'; font-weight: bold; margin-bottom: 30px;
    text-transform: uppercase; letter-spacing: 2px; text-decoration: none;
  }
  .nav-btn:hover { background: #ff9f43; color: #000; box-shadow: 0 0 20px #ff9f43; }

</style>

<div class="hud-bar">
  <span>Archive Status: <span style="color:#00d2ff">DECRYPTED</span></span>
  <span>Security Level: <span class="hud-alert">ZERO</span></span>
</div>

<a href="/" class="nav-btn">← Return to Mainframe</a>

<div style="text-align: center; margin-bottom: 50px;">
  <h2>CLASSIFIED ARCHIVES</h2>
  <p style="color: #666;">"Here lies the proof that I convert caffeine into algebra."</p>
</div>

---

### // LOG ENTRY: 2025

<div class="pub-card">
  <span class="paper-title">In Search of an Interaction in the Dark Sector through Gaussian Process and ANN Approaches</span>
  <div class="authors">
    <strong>Mazaharul Abedin</strong>, Guo-Jian Wang, Yin-Zhe Ma, Supriya Pan
  </div>
  <div style="color: #00d2ff; font-weight: bold; margin-bottom: 15px;">
    MNRAS (The Royal Astronomical Society)
  </div>
  
  <div style="margin-bottom: 20px;">
    <a href="https://doi.org/10.1093/mnras/staf762" class="data-link">📡 DOI Link</a>
    <a href="https://arxiv.org/abs/2505.04336" class="data-link">📄 ArXiv File</a>
  </div>

  <div class="terminal-box">
    <strong>> THE GIST:</strong><br>
    We used AI (Neural Networks) to spy on the Universe. We wanted to know if Dark Matter and Dark Energy are secretly gossiping (interacting).<br><br>
    <strong>> RESULT:</strong><br>
    Detecting interaction signals. The standard model is sweating nervously.
  </div>
</div>

<div class="pub-card">
  <span class="paper-title">When Dark Matter Heats Up: A Model-Independent Search for Non-Cold Behavior</span>
  <div class="authors">
    <strong>Mazaharul Abedin</strong>, Luis A. Escamilla, Supriya Pan, Eleonora Di Valentino, Weiqiang Yang
  </div>
  <div style="color: #00d2ff; font-weight: bold; margin-bottom: 15px;">
    Preprint / ArXiv
  </div>
  
  <div style="margin-bottom: 20px;">
    <a href="https://arxiv.org/abs/2505.09470" class="data-link">📄 ArXiv File</a>
  </div>

  <div class="terminal-box">
    <strong>> THE GIST:</strong><br>
    Everyone assumes Dark Matter is "Cold" (slow and boring). We checked if maybe it has some pressure (is it getting hot in here?).<br><br>
    <strong>> RESULT:</strong><br>
    Evidence is mild, but we can't rule it out. Dark Matter remains the Universe's most annoying mystery.
  </div>
</div>

---

<div style="text-align: center; margin-top: 50px;">
  <a href="/" class="nav-btn">← Return to Mainframe</a>
</div>
