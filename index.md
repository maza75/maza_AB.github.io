---
layout: home
title: Home
order: 1
---

<style>
  /* --- 🌌 FONTS & IMPORTS --- */
  @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Share+Tech+Mono&family=Rajdhani:wght@300;500;700&display=swap');

  /* --- ⚙️ SYSTEM CORE VARIABLES --- */
  :root {
    --neon-cyan: #00f3ff;
    --neon-pink: #bc13fe;
    --neon-green: #0aff0a;
    --void-bg: #050505;
    --glass-panel: rgba(13, 13, 18, 0.7);
    --border-color: rgba(255, 255, 255, 0.1);
  }

  /* --- 🚀 GLOBAL PHYSICS --- */
  html, body {
    margin: 0; padding: 0;
    width: 100%; overflow-x: hidden;
    background-color: var(--void-bg);
    color: #a8b2d1;
    font-family: 'Share Tech Mono', monospace; /* More code-like font */
  }

  /* --- 🌐 MOVING 3D GRID BACKGROUND --- */
  body {
    background-image: 
      linear-gradient(rgba(0, 243, 255, 0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0, 243, 255, 0.03) 1px, transparent 1px);
    background-size: 40px 40px;
    background-position: center top;
  }

  /* --- 📺 CRT INTERFACE OVERLAY --- */
  body::after {
    content: " ";
    display: block;
    position: fixed; top: 0; left: 0; bottom: 0; right: 0;
    background: linear-gradient(rgba(18, 16, 16, 0) 50%, rgba(0, 0, 0, 0.15) 50%), 
                linear-gradient(90deg, rgba(255, 0, 0, 0.06), rgba(0, 255, 0, 0.02), rgba(0, 0, 255, 0.06));
    z-index: 9999;
    background-size: 100% 3px, 3px 100%;
    pointer-events: none;
  }

  /* --- 📐 DYNAMIC WRAPPER (Responsive Engine) --- */
  .wrapper {
    width: 100%;
    max-width: 1200px; /* Wider for laptops */
    margin: 0 auto;
    padding: 0 20px;
    box-sizing: border-box;
    position: relative;
    z-index: 2;
  }

  /* --- 🎛️ HUD STATUS BAR (Glass) --- */
  .hud-bar {
    display: flex;
    justify-content: space-between;
    padding: 15px;
    border-bottom: 1px solid var(--border-color);
    background: rgba(0,0,0,0.5);
    backdrop-filter: blur(5px);
    font-family: 'Orbitron', sans-serif;
    font-size: 0.75rem;
    letter-spacing: 2px;
    color: #555;
    margin-bottom: 40px;
  }
  .hud-item { display: flex; align-items: center; gap: 8px; }
  .status-dot { width: 8px; height: 8px; background: var(--neon-green); border-radius: 50%; box-shadow: 0 0 10px var(--neon-green); }
  .status-alert { width: 8px; height: 8px; background: red; border-radius: 50%; animation: blink 1s infinite; }

  /* --- 🧪 TYPOGRAPHY --- */
  h1 {
    font-family: 'Orbitron', sans-serif;
    font-weight: 900;
    /* DYNAMIC FONT SIZING: Scales between 2rem (mobile) and 4rem (desktop) */
    font-size: clamp(2rem, 5vw, 4.5rem); 
    line-height: 1;
    margin-bottom: 10px;
    color: #fff;
    text-transform: uppercase;
    position: relative;
    text-shadow: 2px 2px 0px var(--neon-pink);
  }

  h2 {
    font-family: 'Rajdhani', sans-serif;
    font-size: clamp(1.5rem, 3vw, 2rem);
    color: #fff;
    border-bottom: 2px solid var(--neon-cyan);
    display: inline-block;
    padding-bottom: 5px;
    margin-top: 50px;
    margin-bottom: 25px;
    text-transform: uppercase;
  }

  p { font-size: 1.1rem; line-height: 1.6; color: #b4c0d6; }
  strong { color: var(--neon-cyan); }
  a { color: var(--neon-pink); text-decoration: none; border-bottom: 1px dashed var(--neon-pink); transition: 0.3s; }
  a:hover { background: var(--neon-pink); color: #fff; border-bottom: none; box-shadow: 0 0 15px var(--neon-pink); }

  /* --- ⚡ GLITCH EFFECT FOR NAME --- */
  .glitch { position: relative; color: white; }
  .glitch::before, .glitch::after {
    content: attr(data-text); position: absolute; top: 0; left: 0; width: 100%; height: 100%; background: var(--void-bg);
  }
  .glitch::before { left: 2px; text-shadow: -1px 0 red; clip: rect(24px, 550px, 90px, 0); animation: glitch-anim-2 3s infinite linear alternate-reverse; }
  .glitch::after { left: -2px; text-shadow: -1px 0 blue; clip: rect(85px, 550px, 140px, 0); animation: glitch-anim 2.5s infinite linear alternate-reverse; }
  @keyframes glitch-anim { 0% { clip: rect(14px, 9999px, 121px, 0); } 100% { clip: rect(69px, 9999px, 34px, 0); } }
  @keyframes glitch-anim-2 { 0% { clip: rect(129px, 9999px, 36px, 0); } 100% { clip: rect(2px, 9999px, 86px, 0); } }

  /* --- 📂 HOLOGRAPHIC PANELS --- */
  .holo-card {
    background: var(--glass-panel);
    border: 1px solid var(--border-color);
    padding: 30px;
    border-radius: 4px;
    position: relative;
    backdrop-filter: blur(10px); /* Blurs the grid behind it */
    box-shadow: 0 0 20px rgba(0,0,0,0.5);
    transition: transform 0.3s, border-color 0.3s;
    overflow: hidden;
  }
  
  /* Corner Accents */
  .holo-card::before {
    content: ''; position: absolute; top: 0; left: 0; width: 20px; height: 20px;
    border-top: 2px solid var(--neon-cyan); border-left: 2px solid var(--neon-cyan);
  }
  .holo-card::after {
    content: ''; position: absolute; bottom: 0; right: 0; width: 20px; height: 20px;
    border-bottom: 2px solid var(--neon-cyan); border-right: 2px solid var(--neon-cyan);
  }

  .holo-card:hover {
    transform: translateY(-5px);
    border-color: rgba(0, 243, 255, 0.3);
    box-shadow: 0 10px 30px rgba(0, 243, 255, 0.1);
  }

  /* --- 🧬 TECH GRID (Mobile & Laptop Optimized) --- */
  .tech-wrapper {
    display: grid;
    /* Auto-fit makes it responsive without media queries */
    grid-template-columns: repeat(auto-fit, minmax(120px, 1fr)); 
    gap: 15px;
    margin-top: 20px;
  }
  
  .tech-node {
    background: rgba(255,255,255,0.03);
    border: 1px solid #333;
    padding: 10px;
    text-align: center;
    font-size: 0.9rem;
    color: var(--neon-cyan);
    transition: 0.2s;
    cursor: crosshair;
  }
  .tech-node:hover {
    background: var(--neon-cyan);
    color: #000;
    box-shadow: 0 0 15px var(--neon-cyan);
  }

  /* --- 🤣 HAZARD ZONE (COMEDY) --- */
  .hazard-zone {
    background: repeating-linear-gradient(
      45deg,
      #1a1a1a,
      #1a1a1a 10px,
      #222 10px,
      #222 20px
    );
    border: 2px dashed #ff9f43;
    padding: 30px;
    margin-top: 60px;
    text-align: center;
    position: relative;
  }
  .hazard-title {
    background: #ff9f43; color: #000; padding: 5px 15px;
    font-family: 'Orbitron'; font-weight: bold;
    position: absolute; top: -15px; left: 50%; transform: translateX(-50%);
  }

  /* --- 🕹️ BUTTONS --- */
  .btn-main {
    display: inline-block;
    padding: 15px 40px;
    margin-top: 20px;
    border: 2px solid var(--neon-pink);
    color: var(--neon-pink);
    font-family: 'Orbitron';
    text-transform: uppercase;
    letter-spacing: 2px;
    position: relative;
    overflow: hidden;
    z-index: 1;
    transition: 0.3s;
    border-bottom: 2px solid var(--neon-pink); /* Override global */
  }
  .btn-main::before {
    content: ''; position: absolute; top: 0; left: -100%; width: 100%; height: 100%;
    background: var(--neon-pink); transition: 0.4s; z-index: -1;
  }
  .btn-main:hover::before { left: 0; }
  .btn-main:hover { color: #fff; box-shadow: 0 0 20px var(--neon-pink); }

  /* --- 📱 MOBILE SPECIFIC TWEAKS --- */
  @media screen and (max-width: 768px) {
    .hud-bar { padding: 10px; font-size: 0.6rem; }
    .holo-card { padding: 20px; }
    /* Hide specific decorative elements if screen is too small */
    .holo-card::before, .holo-card::after { width: 10px; height: 10px; }
  }

  @keyframes blink { 0%, 100% { opacity: 1; } 50% { opacity: 0; } }
</style>

<div class="wrapper">

  <div class="hud-bar">
    <div class="hud-item"><div class="status-dot"></div> SYSTEM: ONLINE</div>
    <div class="hud-item">LOC: KOLKATA [EARTH-982]</div>
    <div class="hud-item"><div class="status-alert"></div> CAFFEINE: CRITICAL</div>
  </div>

  <div style="margin-bottom: 60px;">
    <h1 class="glitch" data-text="MAZAHARUL ABEDIN">MAZAHARUL ABEDIN</h1>
    
    <p style="border-left: 3px solid var(--neon-pink); padding-left: 15px; font-size: 1.2rem; color: #fff;">
      > PhD Research Scholar | Cosmetic Architect | Void Stare-er<br>
      > Investigating <strong>Dark Energy</strong> & <strong>Cosmic Expansion</strong>
    </p>

    <div class="holo-card" style="margin-top: 30px;">
      <p style="margin: 0;">
        <strong>// INITIALIZING GREETING PROTOCOL...</strong><br><br>
        Operating out of the <strong>Department of Mathematics, Presidency University</strong> under the command of <strong>Dr. Supriya Pan</strong>. 
        I combine Theoretical Physics with Astronomical Observations to ask the Universe why it is running away from us so fast.
      </p>
    </div>
  </div>

  <section>
    <h2><span style="color:var(--neon-cyan)">01.</span> CASE FILE: COSMOLOGY</h2>
    
    <div class="holo-card">
      <p>
        I employ both <strong>parametric</strong> (testing theories) and <strong>non-parametric</strong> (letting data speak) methodologies.
        

[Image of cosmic expansion timeline]

      </p>
      
      <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px; margin-top: 20px;">
        <div style="border: 1px dashed #333; padding: 15px;">
          <strong style="color:var(--neon-pink)">TARGET: Dark Energy</strong>
          <p style="font-size: 0.9rem; margin-top: 5px;">Reconstructing Hubble parameters to understand late-time acceleration.</p>
        </div>
        <div style="border: 1px dashed #333; padding: 15px;">
          <strong style="color:var(--neon-pink)">TARGET: ΛCDM</strong>
          <p style="font-size: 0.9rem; margin-top: 5px;">Hunting for cracks in the standard model using SNe Ia & DESI-BAO data.</p>
        </div>
      </div>
    </div>
  </section>

  <section>
    <h2><span style="color:var(--neon-cyan)">02.</span> THE ARSENAL</h2>
    <p>When the math gets too abstract, I make the GPU do the work.</p>

    <div class="holo-card">
      <p style="font-family: 'Orbitron'; color: #666; font-size: 0.8rem; margin-bottom: 5px;">// LOAD MODULE: MACHINE_LEARNING</p>
      <div class="tech-wrapper">
        <div class="tech-node">Gaussian Proc</div>
        <div class="tech-node">Gapp</div>
        <div class="tech-node">JAX</div>
        <div class="tech-node">NumPyro</div>
        <div class="tech-node">ANNs</div>
        <div class="tech-node">tinygp</div>
      </div>

      <div style="height: 20px;"></div> <p style="font-family: 'Orbitron'; color: #666; font-size: 0.8rem; margin-bottom: 5px;">// LOAD MODULE: COSMOLOGY_SIMS</p>
      <div class="tech-wrapper">
        <div class="tech-node">CLASS</div>
        <div class="tech-node">MontePython</div>
        <div class="tech-node">Cobaya</div>
        <div class="tech-node">emcee</div>
        <div class="tech-node">Colfi</div>
      </div>
    </div>
  </section>

  <section>
    <div class="hazard-zone">
      <span class="hazard-title">⚠ HUMAN SIMULATION MODE ⚠</span>
      <p style="color: #ff9f43; font-size: 1.1rem; margin-bottom: 20px;">
        <strong>System Warning:</strong> Prolonged exposure to Friedmann equations may cause hallucinations.
      </p>
      <p style="color: #ccc;">
        To prevent overheating, I switch to <strong>Comedy Protocol</strong>. Inspired by <strong>Charlie Chaplin</strong> and <strong>Mr. Bean</strong>, I navigate the chaos of life with maximum awkwardness.
      </p>
      <div style="margin-top: 20px; display: flex; justify-content: center; gap: 20px; flex-wrap: wrap;">
        <span style="border: 1px solid #ff9f43; padding: 5px 15px; color: #ff9f43;">🏏 CRICKET</span>
        <span style="border: 1px solid #ff9f43; padding: 5px 15px; color: #ff9f43;">🎬 CINEMA</span>
        <span style="border: 1px solid #ff9f43; padding: 5px 15px; color: #ff9f43;">🎨 DESIGN</span>
      </div>
    </div>
  </section>

  <div style="text-align: center; margin: 80px 0;">
    <a href="mailto:mazaharul.rs@presiuniv.ac.in" class="btn-main">
      INITIATE UPLINK (EMAIL)
    </a>
    <br><br>
    <p style="font-size: 0.8rem; color: #555;">// END OF TRANSMISSION //</p>
  </div>

</div>
