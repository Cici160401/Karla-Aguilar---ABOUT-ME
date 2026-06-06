<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Karla's Digital Garden</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=VT323&family=Space+Mono:wght@400;700&display=swap');

    :root {
      --pink: #ff7ac8;
      --hot-pink: #ff3ca7;
      --purple: #a855f7;
      --blue: #7dd3fc;
      --mint: #86efac;
      --cream: #fff7ed;
      --dark: #13051f;
      --panel: rgba(35, 15, 58, 0.88);
      --border: #ffb3e6;
    }

    * { box-sizing: border-box; }

    body {
      margin: 0;
      min-height: 100vh;
      color: var(--cream);
      font-family: 'Space Mono', monospace;
      background:
        radial-gradient(circle at 20% 20%, rgba(255, 122, 200, .35), transparent 25%),
        radial-gradient(circle at 80% 10%, rgba(125, 211, 252, .3), transparent 25%),
        radial-gradient(circle at 50% 90%, rgba(168, 85, 247, .35), transparent 30%),
        #13051f;
      overflow-x: hidden;
    }

    body::before {
      content: "";
      position: fixed;
      inset: 0;
      pointer-events: none;
      background-image:
        linear-gradient(rgba(255,255,255,.05) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,.05) 1px, transparent 1px);
      background-size: 32px 32px;
      opacity: .35;
    }

    .page {
      width: min(1040px, 92vw);
      margin: 40px auto;
      position: relative;
      z-index: 1;
    }

    .hero {
      text-align: center;
      padding: 36px 24px;
      border: 3px double var(--border);
      background: linear-gradient(135deg, rgba(255,122,200,.18), rgba(125,211,252,.12)), var(--panel);
      border-radius: 28px;
      box-shadow: 0 0 35px rgba(255, 122, 200, .35), inset 0 0 35px rgba(255,255,255,.05);
    }

    h1 {
      margin: 0;
      font-family: 'VT323', monospace;
      font-size: clamp(3rem, 9vw, 6rem);
      letter-spacing: 2px;
      color: #fff;
      text-shadow: 4px 4px 0 var(--hot-pink), 8px 8px 0 rgba(125,211,252,.7);
    }

    .subtitle {
      font-size: 1rem;
      color: #ffe4f4;
      margin-top: 12px;
    }

    .marquee {
      margin-top: 24px;
      overflow: hidden;
      border: 2px dashed var(--pink);
      background: rgba(0,0,0,.35);
      border-radius: 999px;
      white-space: nowrap;
    }

    .marquee span {
      display: inline-block;
      padding: 12px 0;
      animation: scroll 18s linear infinite;
    }

    @keyframes scroll {
      from { transform: translateX(100%); }
      to { transform: translateX(-100%); }
    }

    .ascii {
      margin: 28px auto 0;
      text-align: left;
      max-width: 520px;
      padding: 16px;
      background: rgba(0,0,0,.42);
      border: 1px solid rgba(255,255,255,.25);
      border-radius: 18px;
      color: var(--mint);
      font-family: 'VT323', monospace;
      font-size: 1.35rem;
      box-shadow: inset 0 0 20px rgba(134,239,172,.15);
      white-space: pre-wrap;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(12, 1fr);
      gap: 20px;
      margin-top: 24px;
    }

    .card {
      grid-column: span 6;
      padding: 22px;
      background: var(--panel);
      border: 2px solid rgba(255,179,230,.8);
      border-radius: 24px;
      box-shadow: 0 0 22px rgba(168,85,247,.25);
    }

    .wide { grid-column: span 12; }

    .card h2 {
      margin: 0 0 14px;
      font-family: 'VT323', monospace;
      font-size: 2.2rem;
      color: #fff;
      text-shadow: 2px 2px 0 var(--purple);
    }

    .badge-row {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }

    .badge {
      padding: 9px 12px;
      color: #1f1230;
      font-weight: 700;
      background: linear-gradient(90deg, #ffd6ef, #d6f4ff, #e4ffd6);
      border: 2px solid #fff;
      border-radius: 999px;
      box-shadow: 4px 4px 0 rgba(0,0,0,.35);
    }

    .project {
      padding: 14px;
      border: 1px dashed rgba(255,255,255,.4);
      border-radius: 16px;
      margin-bottom: 12px;
      background: rgba(255,255,255,.06);
    }

    .project strong { color: var(--blue); }

    .status-box {
      font-family: 'VT323', monospace;
      font-size: 1.45rem;
      color: #ffe4f4;
      line-height: 1.15;
      background: rgba(0,0,0,.4);
      border-radius: 18px;
      padding: 18px;
      border: 1px solid rgba(255,255,255,.25);
      white-space: pre-wrap;
    }

    .links a {
      display: inline-block;
      margin: 8px 8px 0 0;
      padding: 10px 14px;
      color: #fff;
      text-decoration: none;
      background: linear-gradient(135deg, var(--hot-pink), var(--purple));
      border: 2px solid #fff;
      border-radius: 12px;
      box-shadow: 5px 5px 0 rgba(0,0,0,.35);
      transition: transform .2s ease;
    }

    .links a:hover { transform: translate(-2px, -2px); }

    footer {
      text-align: center;
      margin: 28px 0 0;
      color: #ffd6ef;
      font-family: 'VT323', monospace;
      font-size: 1.5rem;
    }

    @media (max-width: 760px) {
      .card { grid-column: span 12; }
      .ascii, .status-box { font-size: 1.1rem; }
    }
  </style>
</head>
<body>
  <main class="page">
    <section class="hero">
      <h1>KARLA'S DIGITAL GARDEN</h1>
      <p class="subtitle">Software Engineer · AI Explorer · Data & Backend Builder</p>
      <div class="marquee"><span>Welcome traveler · growing ideas, dashboards, APIs and neural networks · currently debugging reality.exe ·</span></div>
      <div class="ascii">╔════════════════════════════════╗
║      LOADING KARLA.EXE...      ║
║                                ║
║  ████████████████████ 100%     ║
║                                ║
║  STATUS: ONLINE                ║
║  LOCATION: ECUADOR             ║
║  MODE: BUILDING THINGS         ║
╚════════════════════════════════╝</div>
    </section>

    <section class="grid">
      <article class="card wide">
        <h2>About this garden</h2>
        <p>Hello traveler. I'm Karla, a software engineer from Ecuador who enjoys building useful software, learning machine learning, reading research papers and creating projects with a little bit of magic.</p>
        <p>My favorite intersection is where software engineering meets data, AI, agriculture and real-world problems.</p>
      </article>

      <article class="card">
        <h2>Current quest log</h2>
        <div class="status-box">MAIN QUEST:
  Build AI solutions for agriculture

SIDE QUESTS:
  - Improve C# and ASP.NET
  - Study ML and Deep Learning
  - Build clean APIs
  - Create research-based projects</div>
      </article>

      <article class="card">
        <h2>Digital shrine</h2>
        <ul>
          <li>Machine Learning</li>
          <li>Computer Vision</li>
          <li>Backend Architecture</li>
          <li>Agriculture Tech</li>
          <li>Protein Classification</li>
          <li>Data Analytics</li>
        </ul>
      </article>

      <article class="card wide">
        <h2>Tech collection</h2>
        <div class="badge-row">
          <span class="badge">Python</span>
          <span class="badge">C#</span>
          <span class="badge">ASP.NET</span>
          <span class="badge">FastAPI</span>
          <span class="badge">React</span>
          <span class="badge">Vue</span>
          <span class="badge">MySQL</span>
          <span class="badge">Docker</span>
          <span class="badge">TensorFlow</span>
          <span class="badge">Pandas</span>
        </div>
      </article>

      <article class="card wide">
        <h2>Featured projects</h2>
        <div class="project"><strong>Spider Venom Classification</strong><br/>Deep learning project for classifying phospholipases using structural protein images.</div>
        <div class="project"><strong>PlantsGrow AI</strong><br/>AgTech platform idea for crop monitoring and disease detection with AI.</div>
        <div class="project"><strong>Banana Export Forecasting</strong><br/>Time-series forecasting and dashboards for export analytics.</div>
        <div class="project"><strong>Portfolio API</strong><br/>FastAPI + MySQL project manager with authentication, categories and comments.</div>
      </article>

      <article class="card wide links">
        <h2>Message board</h2>
        <p>Let's talk about software, machine learning, agriculture, research or weird little internet projects.</p>
        <a href="https://github.com/Cici160401">GitHub</a>
        <a href="https://linkedin.com/in/karladelcisneaguilaralonso">LinkedIn</a>
        <a href="mailto:raliuga2001@gmail.com">Email</a>
      </article>
    </section>

    <footer>
      ╔════════════════════════════════════╗<br/>
      Thanks for visiting my garden<br/>
      Come back anytime<br/>
      ╚════════════════════════════════════╝
    </footer>
  </main>
</body>
</html>
