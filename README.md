<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Curtain Times — Timeless Theater Insights</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Barlow:wght@300;500&display=swap" rel="stylesheet">
  <style>
    /* Reset & Base */
    *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body { font-family: 'Barlow', sans-serif; background: #000080; color: #f5f5f5; overflow-x: hidden; }
    a { text-decoration: none; color: inherit; }

    /* Palette */
    :root { --accent: #ff0000; --noise-opacity: 0.08; }

    /* Digital Noise & Scanlines */
    .digital-noise { pointer-events: none; position: fixed; top:0; left:0; width:100%; height:100%; background:url('assets/noise.png') repeat; opacity:var(--noise-opacity); mix-blend-mode:overlay; animation:noiseAnim 0.5s steps(2) infinite; z-index:9999; }
    .scanlines { pointer-events: none; position: fixed; top:0; left:0; width:100%; height:100%; background:repeating-linear-gradient(to bottom, transparent 0, transparent 1px, rgba(0,0,0,0.03) 1px, rgba(0,0,0,0.03) 2px); z-index:9998; }
    @keyframes noiseAnim { 0% { background-position:0 0; } 100% { background-position:200px 200px; } }

    /* Header */
    header { position: fixed; top:0; left:0; width:100%; padding:1rem 2rem; display:flex; justify-content:space-between; align-items:center; background: rgba(0,0,128,0.7); backdrop-filter:blur(10px); z-index:100; }
    .logo img { height:2rem; }
    nav a { margin-left: 2rem; padding: 0.5rem 1rem; font-weight:500; color:#f5f5f5; border: 2px solid var(--accent); border-radius:4px; transition: background 0.3s, box-shadow 0.3s, color 0.3s; display:inline-block; }
    nav a:hover { background: var(--accent); color: #000; box-shadow: 0 0 8px var(--accent), 0 0 16px var(--accent); }

    /* Page Title */
    .page-title { margin-top: 6rem; text-align: center; }
    .page-title h1 { font-family:'Playfair Display', serif; font-size:3rem; color:var(--accent); text-shadow:0 0 8px var(--accent), 0 0 16px var(--accent); animation: glow 2s ease-in-out infinite alternate; }

    /* Hero */
    .hero { position: relative; width: 100vw; min-height: calc(100vh - 6rem); display: flex; align-items: flex-start; justify-content: center; background-color: #000080; padding-top: 2rem; }

    .hero-content { text-align: center; max-width: 700px; display: flex; flex-direction: column; align-items: center; gap: 0.5rem; }
    .hero-content img { max-width:80%; height:auto; display:block; }
    .btn-circle { width:4rem; height:4rem; border:2px solid var(--accent); border-radius:50%; display:flex; align-items:center; justify-content:center; color:var(--accent); }

    /* Footer */
    footer { background:#000080; color:#666; text-align:center; padding:3rem 2rem; font-size:0.875rem; }

    /* Animations */
    @keyframes glow { from { text-shadow:0 0 8px var(--accent), 0 0 16px var(--accent);} to { text-shadow:0 0 16px var(--accent), 0 0 32px var(--accent);} }
  </style>
</head>
<body>
  <canvas id="trail-canvas"></canvas>
  <div class="digital-noise"></div>
  <div class="scanlines"></div>

  <header>
    <div class="logo"><img src="assets/red-crown.png" alt="Curtain Times Logo" /></div>
    <nav>
      <a href="#" class="btn">Home</a>
      <a href="#features" class="btn">Features</a>
      <a href="#about" class="btn">About</a>
      <a href="#contact" class="btn">Contact</a>
    </nav>
  </header>

  <div class="page-title">
    <h1>The Curtain Times</h1>
  </div>

  <div class="hero">
    <div class="hero-content">
      <img src="assets/curtain-times-cover.png" alt="Cover Image" />
      <a href="#articles" class="btn-circle">Iss. #1</a>
    </div>
  </div>

  <!-- Additional sections go here -->

  <footer>
    &copy; 2025 Curtain Times. All Rights Reserved.
  </footer>
</body>
</html>
