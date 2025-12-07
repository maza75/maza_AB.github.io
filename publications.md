---
layout: page
title: Publications
permalink: /publications/
order: 2
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Space+Mono&display=swap');

  /* --- 🌌 DEEP SPACE THEME 🌌 --- */
  body {
    background: radial-gradient(ellipse at bottom, #1b2735 0%, #090a0f 100%);
    color: #a0a0a0;
    font-family: 'Space Mono', monospace;
    overflow-x: hidden;
  }

  /* Animated Stars Background */
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
  h1, h2, h3 { font-family: 'Orbitron', sans-serif; color: #00d2ff; text-transform: uppercase; letter-spacing: 2px; }
  strong { color: #fff; text-shadow: 0 0 5px #fff; }
  a { color: #ff00ff; text-decoration: none; transition: 0.3s; }
  a:hover { color: #00d2ff; text-shadow: 0 0 8px #00d2ff; }

  /* --- 🛸 HOLOGRAPHIC DATA CARDS --- */
  .publication-item {
    background: rgba(20, 20, 30, 0.6); /* Semi-transparent */
    backdrop-filter: blur(5px);
    border: 1px solid rgba(0, 210, 255, 0.3);
    border-left: 4px solid #ff00ff; /* Neon Pink accent */
    padding: 30px;
    margin-bottom: 40px;
    border-radius: 15px;
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
    transition: transform 0.3s, box-shadow 0.3s;
    position: relative;
  }

  .publication-item:hover {
    transform: translateY(-5px);
    box-shadow: 0 0 30px rgba(255, 0, 255, 0.2);
    border-color: #ff00ff;
  }

  .paper-title { 
    font-family: 'Orbitron', sans-serif;
    font-size: 1.4em; 
    color: #fff; 
    display: block; 
    margin-bottom: 10px;
    text-shadow: 0 0 10px rgba(255, 255, 255, 0.3);
  }
  
  .authors { color: #888; font-style: italic; margin-bottom: 15px; font-size: 1em; }
  .journal-info { color: #00d2ff; font-weight: bold; margin-bottom: 15px; text-transform: uppercase; letter-spacing: 1px; }

  /* --- 📟 TERMINAL HIGHLIGHTS --- */
  .highlights {
    background: #000;
    border: 1px solid #333;
    padding: 20px;
    border-radius: 5px;
    font-family: 'Courier New', monospace;
    color: #0f0; /* Terminal Green */
    margin-top: 20px;
    position: relative;
  }
  .highlights::before {
    content: "> ANALYSIS_OUTPUT_LOG:";
    display: block;
    color: #555;
    font-size: 0.8em;
    margin-bottom: 10px;
  }
  .highlights strong { color: #00d2ff; text-shadow: none; }
  .highlights em { color: #ff00ff; font-style: normal; }

  /* --- 🔗 BUTTONS --- */
  .links a {
    display: inline-block;
    padding: 8px 16px;
    border: 1px solid #00d2ff;
    color: #00d2ff;
    font-size: 0.85em;
    margin-right: 10px;
    border-radius: 4px;
    text-transform: uppercase;
    font-weight: bold;
  }
  .links a:hover {
    background: #00d2ff;
    color: #000;
    box-shadow: 0 0 15px #00d2ff;
  }

  /* --- 🔙 NAVIGATION BTN --- */
  .nav-btn {
    display: inline-block; padding: 10px 20px; border: 2px solid #ff9f43;
    color: #ff9f43; border-radius: 5px; font-weight: bold; margin-bottom: 30px;
    text-transform: uppercase; letter-spacing: 2px;
  }
  .nav-btn:hover { background: #ff9f43; color: #000; box-shadow: 0 0 20px #ff9f43; }

</style>

<div class="stars"></div>

<a href="/" class="nav-btn">← Return to Base</a>

## 📂 Mission Logs & Data Streams
*Decoded Transmissions from the Department of Mathematics.*

---

### // STARDATE 2025

<div class="publication-item">
  <span class="paper-title">In Search of an Interaction in the Dark Sector through Gaussian Process and ANN Approaches</span>
  <div class="authors">
    <strong>Mazaharul Abedin</strong>, Guo-Jian Wang, Yin-Zhe Ma, Supriya Pan
  </div>
  <div class="journal-info">
    Monthly Notices of the Royal Astronomical Society (MNRAS)
  </div>
  
  <div class="links">
    <a href="https://doi.org/10.1093/mnras/staf762">📡 DOI Link</a>
    <a href="https://arxiv.org/abs/2505.04336">📄 ArXiv Data</a>
  </div>

  <div class="highlights">
    <strong>🔍 EXEC_SUMMARY:</strong><br>
    Deployed <em>Gaussian Process Regression (GP)</em> and <em>Neural Networks (ANN)</em> to detect if Dark Matter and Dark Energy are talking to each other behind our backs.
    <ul>
      <li><strong>Input Data:</strong> Cosmic Chronometers (CC) & Pantheon+ Supernovae.</li>
      <li><strong>Result:</strong> Interaction detected? Analyzing dependency on Dark Energy EOS...</li>
    </ul>
  </div>
</div>

<div class="publication-item">
  <span class="paper-title">When Dark Matter Heats Up: A Model-Independent Search for Non-Cold Behavior</span>
  <div class="authors">
    <strong>Mazaharul Abedin</strong>, Luis A. Escamilla, Supriya Pan, Eleonora Di Valentino, Weiqiang Yang
  </div>
  <div class="journal-info">
    Preprint / ArXiv
  </div>
  
  <div class="links">
    <a href="https://arxiv.org/abs/2505.09470">📄 ArXiv Data</a>
  </div>

  <div class="highlights">
    <strong>🔍 EXEC_SUMMARY:</strong><br>
    Investigated if Dark Matter has "pressure" (is it getting hot in here?) using model-independent reconstruction.
    <ul>
      <li><strong>Objective:</strong> Testing for non-cold behavior in standard models.</li>
      <li><strong>Verdict:</strong> Evidence is mild, but we can't rule it out. The Universe keeps its secrets.</li>
    </ul>
  </div>
</div>

---

<div style="text-align: center; margin-top: 30px;">
  <a href="/" class="nav-btn">← Return to Base</a>
</div>
