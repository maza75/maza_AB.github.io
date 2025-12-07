---
layout: home
title: Home
order: 1
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Space+Mono&family=vt323&display=swap');

  /* --- 🌌 GLOBAL SYSTEM SETTINGS 🌌 --- */
  html, body {
    overflow-x: hidden;
    max-width: 100%;
  }

  body {
    background-color: #050505;
    background: radial-gradient(circle at center, #1a1a2e 0%, #000000 100%);
    color: #a8b2d1;
    font-family: 'Space Mono', monospace;
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

  /* --- 📱 RESPONSIVE LAYOUT LOGIC 📱 --- */
  .wrapper { 
    width: 95% !important; 
    padding: 0 10px !important; 
    max-width: 100% !important;
  }

  @media screen and (min-width: 1000px) {
    .wrapper { 
      max-width: 1400px !important; 
      width: 92% !important; 
      padding: 0 !important; 
    }
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
  .hud-status { color: #0f0; text-shadow: 0 0 5px #0f0; }

  /* --- TYPOGRAPHY --- */
  h1, h2, h3 { 
    font-family: 'Orbitron', sans-serif; 
    text-transform: uppercase;
    letter-spacing: 2px;
  }
  
  h1 { 
    font-weight: 900; 
    background: -webkit-linear-gradient(#00d2ff, #3a7bd5);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    filter: drop-shadow(0 0 10px rgba(0,210,255,0.5));
    font-size: 2em;
    line-height: 1.2;
  }

  h3 { color: #ff00ff; border-left: 5px solid #00d2ff; padding-left: 15px; font-size: 1.2em; }

  strong { color: #00d2ff; }
  a { color: #ff00ff; text-decoration: none; border-bottom: 1px dashed #ff00ff; transition: 0.3s; }
  a:hover { background: #ff00ff; color: #000; text-decoration: none; border-bottom: none; }

  /* --- 🛸 HERO SECTION --- */
  .hero-panel {
    background: rgba(10, 10, 15, 0.8);
    border: 1px solid #333;
    padding: 30px 15px;
    border-radius: 20px;
    text-align: center;
    position: relative;
    box-shadow: 0 0 30px rgba(0, 210, 255, 0.05);
    margin-bottom: 40px;
  }

  .hero-panel::before {
    content: ''; position: absolute; top: -2px; left: -2px; right: -2px; bottom: -2px;
    background: linear-gradient(45deg, #ff00ff, #000, #00d2ff, #000);
    z-index: -1;
    border-radius: 22px;
    background-size: 400%;
    animation: glowing 20s linear infinite;
  }
  @keyframes glowing { 0% { background-position: 0 0; } 50% { background-position: 400% 0; } 100% { background-position: 0 0; } }

  .typewriter {
    display: inline-block;
    margin: 0 auto;
  }
  .typewriter p {
    font-size: 1em; 
    color: #fff;
    margin: 0;
  }

  /* --- 🧪 DATA MODULES --- */
  .box {
    background: #0d0d12;
    border: 1px solid #1f1f2e;
    padding: 20px;
    margin-bottom: 30px;
    transition: 0.3s;
    position: relative;
  }
  .box:hover {
    border-color: #00d2ff;
    box-shadow: 0 0 20px rgba(0, 210, 255, 0.2);
  }
  .box::after {
    content: " [SECURE]";
    position: absolute; top: 10px; right: 10px;
    font-size: 0.7em; color: #333; font-family: 'Orbitron';
  }

  /* --- 🕹️ BUTTONS --- */
  .btn-container { text-align: center; margin: 40px 0; }
  
  .cyber-btn {
    background: transparent;
    color: #00d2ff;
    font-family: 'Orbitron';
    font-size: 1em;
    padding: 12px 20px;
    border: 2px solid #00d2ff;
    text-transform: uppercase;
    letter-spacing: 1px;
    position: relative;
    transition: 0.3s;
    text-decoration: none;
    border-bottom: 2px solid #00d2ff;
    display: inline-block;
    margin-top: 10px;
  }
  .cyber-btn:hover {
    background: #00d2ff;
    color: #000;
    box-shadow: 0 0 30px #00d2ff;
  }

  /* --- 🤣 COMEDY WARNING BOX --- */
  .warning-box {
    background: repeating-linear-gradient(45deg, #1a1a1a, #1a1a1a 10px, #222 10px, #222 20px);
    border: 2px solid #ff9f43;
    color: #ff9f43;
    padding: 20px;
    text-align: center;
    font-style: italic;
    margin-top: 50px;
  }
  .warning-icon { font-size: 2em; display: block; margin-bottom: 10px; }

  /* --- 📡 BLING BLING SIGNAL BEACON --- */
  .signal-beacon {
    position: fixed; bottom: 20px; right: 20px;
    width: 60px; height: 60px;
    background: radial-gradient(circle, #ff55ff 10%, #ff00ff 100%); /* Shiny Gradient */
    border-radius: 50%;
    display: flex; justify-content: center; align-items: center;
    box-shadow: 0 0 20px #ff00ff, 0 0 40px rgba(255, 0, 255, 0.4);
    z-index: 10000;
    border: 2px solid white;
    animation: bounce 2s infinite ease-in-out;
  }
  
  /* The Ripple Effect (Radar Ping) */
  .signal-beacon::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0; bottom: 0;
    border-radius: 50%;
    border: 2px solid #ff00ff;
    animation: ripple 1.5s infinite ease-out;
    z-index: -1;
  }

  .signal-beacon:hover { 
    transform: scale(1.1); 
    background: #fff; 
    border-color: #ff00ff;
  }
  .signal-beacon:hover .icon-svg { fill: #ff00ff; }
  
  .icon-svg { width: 30px; fill: #fff; transition: 0.3s; }

  /* --- ANIMATIONS --- */
  @keyframes ripple {
    0% { transform: scale(1); opacity: 1; }
    100% { transform: scale(2.5); opacity: 0; }
  }
  
  @keyframes bounce {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-5px); }
  }

  /* --- 📱 MOBILE SPECIFIC --- */
  @media screen and (max-width: 768px) {
    .hud-bar { flex-direction: column; text-align: center; gap: 5px; }
    h1 { font-size: 1.8em; }
    .hero-panel p { font-size: 0.95em; }
    .typewriter p { white-space: normal; border: none; animation: none; }
    .toolkit-span { display: block !important; margin: 5px auto !important; width: 80%; }
  }

  @media screen and (min-width: 1000px) {
    .hero-panel { padding: 50px; }
    h1 { font-size: 3em; }
    .typewriter {
      overflow: hidden; white-space: nowrap; animation: typing 3.5s steps(40, end); border-right: .15em solid orange;
    }
    @keyframes typing { from { width: 0 } to { width: 100% } }
  }

</style>

<div class="hud-bar">
  <span>System: <span class="hud-status">ONLINE</span></span>
  <span>Loc: EARTH-982</span>
  <span>Caffeine: <span style="color:red">CRITICAL</span></span>
</div>

<div class="content-box">
    <p>
        <strong>Greetings, Observer.</strong> 👋
    </p>
    <p>
        I am a PhD Research Scholar at the <strong>Department of Mathematics, Presidency University, Kolkata</strong>. 
        Under the guidance of <strong>Dr. Supriya Pan</strong>, I investigate the underlying fabric of the cosmos.
    </p>
    <p>
        My research sits at the intersection of <strong>Theoretical Physics</strong> and <strong>Astronomical Observation</strong>. 
        My goal? To reconstruct the expansion history of the Universe and figure out if <strong>Dark Energy</strong> is real, or if the Universe is just pranking us.
    </p>
</div>

<div class="section-header">
    <span class="icon">📂</span>
    <h2>Case File: Cosmology</h2>
</div>
<div class="content-box">
    <p>
        I employ both <strong>parametric</strong> (testing theories) and <strong>non-parametric</strong> (letting data speak) methodologies. 
        I combine rigorous math with data from distant galaxies, CMB radiation, and large-scale structures to answer one question: <em>What is the ultimate fate of the Universe?</em>
    </p>
    
    <div class="box" style="margin-top: 20px;">
        <strong>Key Objectives:</strong>
        <ul>
            <li><strong>Dark Energy Forensics:</strong> Reconstructing the Hubble and deceleration parameters to understand late-time acceleration.</li>
            <li><strong>Testing ΛCDM:</strong> The "Standard Model" is robust, but I look for the cracks (deviations) using datasets like SNe Ia and DESI-BAO.</li>
            <li><strong>Model-Independent Recon:</strong> Using Machine Learning to extract cosmic signals without theoretical bias.</li>
        </ul>
    </div>
</div>

<div class="section-header">
    <span class="icon">🛠</span>
    <h2>The Arsenal (Methodology)</h2>
</div>
<div class="content-box">
    <p>
        To model the Universe, I rely on Bayesian inference and modern computation. 
        I often use <strong>Gaussian Processes</strong> to find patterns in chaos and <strong>MCMC sampling</strong> to find the truth in the noise.
    </p>
    
    <div style="margin-top: 15px;">
        <span class="code-font" style="color: #888;">// MACHINE LEARNING & STATS</span>
        <div class="tech-grid">
            <span class="tech-tag">Gaussian Processes</span>
            <span class="tech-tag">Gapp</span>
            <span class="tech-tag">tinygp</span>
            <span class="tech-tag">JAX</span>
            <span class="tech-tag">NumPyro</span>
            <span class="tech-tag">ANNs</span>
        </div>
    </div>

    <div style="margin-top: 15px;">
        <span class="code-font" style="color: #888;">// COSMOLOGY PACKAGES</span>
        <div class="tech-grid">
            <span class="tech-tag">CLASS</span>
            <span class="tech-tag">MontePython</span>
            <span class="tech-tag">Cobaya</span>
            <span class="tech-tag">Colfi</span>
            <span class="tech-tag">emcee</span>
        </div>
    </div>
</div>

<div class="section-header">
    <span class="icon">🎭</span>
    <h2>Human Simulation Mode</h2>
</div>
<div class="warning-box">
    <span class="warning-label">STATUS: OFFLINE</span>
    <p>
        <strong>Balance is key.</strong> When the code compiles (or crashes), I switch contexts.
    </p>
    <p>
        I thrive on creativity, movement, and laughter. Inspired by the timeless humor of <strong>Charlie Chaplin</strong> and <strong>Mr. Bean</strong>, I believe that a little absurdity is necessary to understand a chaotic Universe.
    </p>
    <p>
        <strong>Current Activities:</strong><br>
        🏏 <strong>Sports:</strong> Keeping the kinetic energy high.<br>
        🎬 <strong>Cinema:</strong> From thought-provoking dramas to light-hearted comedies.<br>
        🎨 <strong>Digital Content:</strong> Blending storytelling with imagination.
    </p>
</div>
