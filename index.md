---
layout: home
title: Home
order: 1
---

<style>
  /* --- 🌌 IMPORT FONTS --- */
  @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Space+Mono:ital,wght@0,400;0,700;1,400&family=Share+Tech+Mono&display=swap');

  /* --- 🚀 CORE SYSTEM --- */
  :root {
    --neon-blue: #00f3ff;
    --neon-pink: #ff00ff;
    --matrix-green: #0f0;
    --void-bg: #050505;
    --panel-bg: #0d0d12;
    --border-color: #1f1f2e;
  }

  html, body {
    overflow-x: hidden;
    max-width: 100%;
    background-color: var(--void-bg);
    background-image: 
      radial-gradient(circle at 50% 50%, #1a1a2e 0%, #000000 100%);
    color: #a8b2d1;
    font-family: 'Space Mono', monospace;
  }

  /* --- 📺 CRT SCANLINE OVERLAY --- */
  body::after {
    content: " ";
    display: block;
    position: fixed; top: 0; left: 0; bottom: 0; right: 0;
    background: linear-gradient(rgba(18, 16, 16, 0) 50%, rgba(0, 0, 0, 0.1) 50%), linear-gradient(90deg, rgba(255, 0, 0, 0.06), rgba(0, 255, 0, 0.02), rgba(0, 0, 255, 0.06));
    z-index: 9999;
    background-size: 100% 2px, 3px 100%;
    pointer-events: none;
  }

  /* --- 📐 LAYOUT UTILITIES --- */
  .container {
    max-width: 1000px;
    margin: 0 auto;
    padding: 20px;
  }

  /* --- 📟 HEADERS & TYPOGRAPHY --- */
  h1, h2, h3 {
    font-family: 'Orbitron', sans-serif;
    text-transform: uppercase;
    letter-spacing: 2px;
  }

  h1 {
    font-size: 2.5em;
    font-weight: 900;
    background: -webkit-linear-gradient(var(--neon-blue), #3a7bd5);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    text-shadow: 0 0 15px rgba(0, 243, 255, 0.3);
    margin-bottom: 5px;
  }

  h2 {
    color: var(--neon-pink);
    border-bottom: 1px solid var(--neon-pink);
    padding-bottom: 10px;
    margin-top: 40px;
    font-size: 1.4em;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  a {
    color: var(--neon-blue);
    text-decoration: none;
    border-bottom: 1px dashed var(--neon-blue);
    transition: 0.3s;
  }
  a:hover {
    background: var(--neon-blue);
    color: #000;
    text-decoration: none;
    border-bottom: none;
  }

  /* --- 🎛️ HUD STATUS BAR --- */
  .hud-bar {
    display: flex;
    justify-content: space-between;
    border: 1px solid var(--border-color);
    background: rgba(0,0,0,0.5);
    padding: 10px 15px;
    font-family: 'Share Tech Mono', monospace;
    font-size: 0.85em;
    color: #666;
    margin-bottom: 30px;
    border-radius: 4px;
  }
  .status-ok { color: var(--matrix-green); text-shadow: 0 0 5px var(--matrix-green); }
  .status-warn { color: var(--neon-pink); animation: blink 2s infinite; }

  @keyframes blink { 0% {opacity: 1;} 50% {opacity: 0.3;} 100% {opacity: 1;} }

  /* --- 📦 CONTENT BOXES --- */
  .terminal-box {
    background: var(--panel-bg);
    border: 1px solid var(--border-color);
    border-left: 4px solid var(--neon-blue);
    padding: 20px;
    margin-bottom: 25px;
    position: relative;
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .terminal-box:hover {
    transform: translateX(5px);
    box-shadow: -5px 5px 0px rgba(0, 243, 255, 0.1);
  }
  
  .terminal-box.warning {
    border-left: 4px solid var(--neon-pink);
    background: repeating-linear-gradient(
      45deg,
      #131313,
      #131313 10px,
      #1a1a1a 10px,
      #1a1a1a 20px
    );
  }

  /* --- 🏷️ TECH TAGS --- */
  .tech-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 10px;
  }
  .tech-tag {
    background: rgba(0, 243, 255, 0.1);
    border: 1px solid var(--neon-blue);
    color: var(--neon-blue);
    padding: 4px 10px;
    font-size: 0.8em;
    font-family: 'Share Tech Mono', monospace;
    border-radius: 2px;
  }
  .tech-tag:hover {
    background: var(--neon-blue);
    color: #000;
    cursor: crosshair;
  }

  /* --- 🖱️ BUTTON --- */
  .btn-cyber {
    display: inline-block;
    margin-top: 15px;
    padding: 10px 25px;
    border: 1px solid var(--neon-pink);
    color: var(--neon-pink);
    font-family: 'Orbitron';
    text-transform: uppercase;
    font-size: 0.9em;
    letter-spacing: 1px;
    transition: 0.3s;
    border-bottom: 1px solid var(--neon-pink); /* Overrides global link style */
  }
  .btn-cyber:hover {
    background: var(--neon-pink);
    color: #fff;
    box-shadow: 0 0 15px var(--neon-pink);
  }

  /* --- 💫 GLITCH TEXT EFFECT --- */
  .glitch-wrapper { position: relative; display: inline-block; }
  .user-role { font-size: 1.1em; color: #fff; margin-bottom: 20px; display: block;}

  /* --- 📱 MOBILE --- */
  @media screen and (max-width: 768px) {
    h1 { font-size: 1.8em; }
    .hud-bar { flex-direction: column; text-align: center; gap: 5px; }
  }
</style>

<div class="container">

  <div class="hud-bar">
    <span>SYSTEM: <span class="status-ok">ONLINE</span></span>
    <span>LOC: EARTH-982 (Kolkata)</span>
    <span>COFFEE LEVEL: <span class="status-warn">CRITICAL (12%)</span></span>
  </div>

  <header>
    <h1>MAZAHARUL ABEDIN</h1>
    <span class="user-role">> Ph.D. Research Scholar | Cosmetic Architect | Void Stare-er</span>
    
    <div class="terminal-box">
      <p>
        <strong>[INITIATING GREETING PROTOCOL...]</strong><br><br>
        Greetings, carbon-based lifeform. 👋 <br>
        I am currently operating out of the <strong>Department of Mathematics, Presidency University</strong> under the command of <strong>Dr. Supriya Pan</strong>.
      </p>
      <p>
        My primary directive is to investigate the <strong>fabric of the Universe</strong>. I spend my days asking the Cosmos why it is expanding so fast, and the Cosmos usually responds with "SegFault: Core Dumped."
      </p>
    </div>
  </header>

  <section>
    <h2><span style="filter: grayscale(1);">🔭</span> CASE FILE: COSMOLOGY</h2>
    
    <div class="terminal-box">
      <p>The Universe is 95% dark stuff we don't understand. My job is to fix that using <strong>Theoretical Physics</strong> and <strong>Astronomical Observations</strong>.</p>
      
      <p><strong>CURRENT MISSION OBJECTIVES:</strong></p>
      <ul>
        <li><strong>Dark Energy Forensics:</strong> Reconstructing Hubble parameters to figure out why the Universe is stepping on the gas pedal.</li>
        <li><strong>Interrogating the Data:</strong> Using Machine Learning to make the data confess its secrets without using theoretical torture methods (Model-Independent Reconstruction).</li>
        <li><strong>Breaking the ΛCDM Model:</strong> The standard model is cool, but have you tried breaking it with SNe Ia and DESI-BAO data? Fun times.</li>
      </ul>
    </div>
  </section>

  <section>
    <h2><span style="filter: grayscale(1);">🛠</span> THE ARSENAL</h2>
    <p>When math gets too hard, I make the computer do it.</p>

    <div class="terminal-box">
      <span style="color: #666; font-size: 0.8em;">// LOADED_MODULES: STATS_&_ML</span>
      <div class="tech-grid">
        <span class="tech-tag">Gaussian Processes</span>
        <span class="tech-tag">Gapp</span>
        <span class="tech-tag">JAX</span>
        <span class="tech-tag">NumPyro</span>
        <span class="tech-tag">ANNs</span>
        <span class="tech-tag">Bayesian Inference</span>
      </div>

      <br>
      <span style="color: #666; font-size: 0.8em;">// LOADED_MODULES: COSMO_SIMS</span>
      <div class="tech-grid">
        <span class="tech-tag">CLASS</span>
        <span class="tech-tag">MontePython</span>
        <span class="tech-tag">Cobaya</span>
        <span class="tech-tag">emcee</span>
      </div>
    </div>
  </section>

  <section>
    <h2><span style="filter: grayscale(1);">🎭</span> SIMULATION ERROR: HUMANITY DETECTED</h2>
    
    <div class="terminal-box warning">
      <p style="color: #ff9f43; font-weight: bold;">⚠ WARNING: LOGIC FAILURE IMMINENT</p>
      <p>
        If I stare at the Friedmann equations for too long, I start hallucinating Greek letters. To prevent system overheating, I engage in <strong>"Fun"</strong>.
      </p>
      <p>
        I believe the Universe is a cosmic comedy, and we are the punchline. Inspired by the chaotic energy of <strong>Mr. Bean</strong> and the silent genius of <strong>Charlie Chaplin</strong>, I try to navigate life with maximum awkwardness and minimum grace.
      </p>
      <p>
        <strong>Status Report:</strong><br>
        🏏 <strong>Sports:</strong> Running away from my responsibilities.<br>
        🎬 <strong>Cinema:</strong> Watching movies to forget that $H(z)$ is hard to reconstruct.<br>
        🎨 <strong>Art:</strong> Creating posters that make no sense, much like Quantum Mechanics.
      </p>
    </div>
  </section>

  <section style="text-align: center; margin-top: 50px; margin-bottom: 50px;">
    <p style="font-family: 'Orbitron'; font-size: 1.2em;"> ٹ END OF TRANSMISSION ٹ </p>
    <a href="mailto:mazaharul.rs@presiuniv.ac.in" class="btn-cyber">ESTABLISH UPLINK (EMAIL)</a>
    <br><br>
    <a href="https://github.com/maza75" style="font-size: 0.9em;">[ACCESS GITHUB REPOSITORY]</a>
  </section>

</div>
