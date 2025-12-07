---
layout: page
title: Gallery & Interests
permalink: /gallery/
order: 3
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
  h2 { 
    font-family: 'Orbitron', sans-serif; 
    color: #00d2ff; 
    text-transform: uppercase; 
    letter-spacing: 2px;
    border-bottom: 2px solid #333;
    padding-bottom: 15px;
    margin-top: 50px;
  }
  p { font-size: 1em; color: #888; }
  em { color: #ff00ff; font-style: normal; }

  /* --- 📸 HOLOGRAPHIC GRID SYSTEM --- */
  .gallery-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
    margin-top: 30px;
  }

  .gallery-card {
    background: rgba(20, 20, 30, 0.6);
    backdrop-filter: blur(5px);
    border: 1px solid rgba(0, 210, 255, 0.3);
    border-radius: 10px;
    overflow: hidden;
    transition: transform 0.3s, box-shadow 0.3s;
    position: relative;
  }

  .gallery-card:hover {
    transform: scale(1.02);
    box-shadow: 0 0 25px rgba(0, 210, 255, 0.2);
    border-color: #00d2ff;
  }

  /* Tech Overlay Label */
  .gallery-card::before {
    content: "IMG_DATA";
    position: absolute; top: 10px; right: 10px;
    background: rgba(0,0,0,0.7);
    color: #00d2ff;
    font-size: 0.6em;
    padding: 2px 6px;
    border: 1px solid #00d2ff;
    z-index: 10;
  }

  .gallery-card img {
    width: 100%;
    height: 250px;
    object-fit: cover;
    border-bottom: 2px solid #00d2ff;
    filter: contrast(1.1) grayscale(0.2); /* Sci-Fi Filter */
    transition: 0.3s;
  }
  
  .gallery-card:hover img {
    filter: contrast(1) grayscale(0); /* Color returns on hover */
  }

  .caption {
    padding: 20px;
    text-align: center;
  }
  
  .caption h4 { 
    margin: 0; color: #fff; font-family: 'Orbitron'; font-size: 1.1em; 
    text-shadow: 0 0 5px rgba(255,255,255,0.5);
  }
  .caption span { font-size: 0.85em; color: #00d2ff; display: block; margin-top: 5px; }

  /* --- 🔙 NAVIGATION BTN --- */
  .nav-btn {
    display: inline-block; padding: 10px 20px; border: 2px solid #ff9f43;
    color: #ff9f43; border-radius: 5px; font-weight: bold; margin-bottom: 30px;
    text-transform: uppercase; letter-spacing: 2px; text-decoration: none;
  }
  .nav-btn:hover { background: #ff9f43; color: #000; box-shadow: 0 0 20px #ff9f43; }

</style>

<div class="stars"></div>

<a href="/" class="nav-btn">← Return to Base</a>

## 🏏 System Maintenance (Sports)
*"Keeping the biological hardware functional. Sometimes I hit a ball with a stick; physics says it should fly. Usually, it does."*

<div class="gallery-grid">
  <div class="gallery-card">
    <img src="https://images.unsplash.com/photo-1531415074968-036ba1b575da?q=80&w=800&auto=format&fit=crop" alt="Cricket">
    <div class="caption">
      <h4>Cricket Protocol</h4>
      <span>Calculating Trajectories (Weekends Only)</span>
    </div>
  </div>

  <div class="gallery-card">
    <img src="https://images.unsplash.com/photo-1517649763962-0c623066013b?q=80&w=800&auto=format&fit=crop" alt="Sports">
    <div class="caption">
      <h4>Kinetic Calibration</h4>
      <span>Running away from my problems (Literally)</span>
    </div>
  </div>
  
  <div class="gallery-card">
    <img src="https://images.unsplash.com/photo-1526676037777-05a232554f77?q=80&w=800&auto=format&fit=crop" alt="Team">
    <div class="caption">
      <h4>Team Unit</h4>
      <span>Collaborative Energy Expenditure</span>
    </div>
  </div>
</div>

---

## 🎭 Visual Data Input (Cinema)
*"Analyzing human behavior through projected light. Also, Chaplin is the only one who understands the absurdity of existence."*

<div class="gallery-grid">
  <div class="gallery-card">
    <img src="https://images.unsplash.com/photo-1485846234645-a62644f84728?q=80&w=800&auto=format&fit=crop" alt="Cinema">
    <div class="caption">
      <h4>Cinema Archives</h4>
      <span>The only place physics violations are allowed</span>
    </div>
  </div>

  <div class="gallery-card">
    <img src="https://upload.wikimedia.org/wikipedia/commons/3/34/Charlie_Chaplin_portrait.jpg" alt="Charlie Chaplin">
    <div class="caption">
      <h4>Core Inspiration</h4>
      <span>Charlie Chaplin (Humor Module V1.0)</span>
    </div>
  </div>
</div>

---

## 🎓 Data Upload Locations (Academic)
*"Where the math happens. Presidency University: My primary server location."*

<div class="gallery-grid">
  <div class="gallery-card">
    <img src="https://images.unsplash.com/photo-1523580494863-6f3031224c94?q=80&w=800&auto=format&fit=crop" alt="University">
    <div class="caption">
      <h4>Presidency University</h4>
      <span>Dept. of Mathematics (HQ)</span>
    </div>
  </div>
</div>

<br><br>
<div style="text-align: center;">
  <a href="/" class="nav-btn">← Return to Base</a>
</div>
