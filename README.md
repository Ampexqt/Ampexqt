<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>README · Jhon Harold Rueda</title>
  <!-- Font & minimal reset -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,600;14..32,700&display=swap" rel="stylesheet" />
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #0b0e14;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
      padding: 2rem 1rem;
    }

    .readme-card {
      max-width: 820px;
      width: 100%;
      background: #0f131a;
      border-radius: 2.5rem;
      padding: 2.5rem 2.2rem;
      box-shadow: 0 20px 40px -12px rgba(0, 0, 0, 0.8), 0 0 0 1px rgba(0, 217, 255, 0.08);
      transition: all 0.2s ease;
      border: 1px solid rgba(0, 217, 255, 0.06);
    }

    /* accent glow */
    .accent-glow {
      color: #00d9ff;
    }

    .accent-border {
      border-color: #00d9ff;
    }

    /* header */
    .header-gif {
      display: flex;
      justify-content: center;
      margin-bottom: 1rem;
    }

    .header-gif img {
      width: 100%;
      max-height: 120px;
      object-fit: cover;
      border-radius: 20px;
      border: 1px solid rgba(0, 217, 255, 0.08);
    }

    .divider {
      width: 100%;
      height: 2px;
      background: linear-gradient(90deg, transparent, #00d9ff40, #00d9ff80, #00d9ff40, transparent);
      margin: 1.5rem 0;
      border: 0;
    }

    .name-title {
      text-align: center;
      margin-top: 0.25rem;
    }

    .name-title h1 {
      font-size: 3.2rem;
      font-weight: 700;
      letter-spacing: -0.02em;
      background: linear-gradient(135deg, #f0f4ff 0%, #b0d0ff 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      display: inline-block;
      margin-bottom: 0.1rem;
      text-shadow: 0 0 30px rgba(0, 217, 255, 0.15);
    }

    .subhead {
      color: #9aa5b5;
      font-weight: 400;
      font-size: 1rem;
      letter-spacing: 0.3px;
      background: rgba(0, 217, 255, 0.04);
      display: inline-block;
      padding: 0.35rem 1.4rem;
      border-radius: 40px;
      border: 1px solid rgba(0, 217, 255, 0.08);
      backdrop-filter: blur(2px);
    }

    .tagline {
      text-align: center;
      max-width: 600px;
      margin: 1.2rem auto 0.5rem;
      color: #c8d0dc;
      font-weight: 400;
      font-size: 1.05rem;
      line-height: 1.6;
      background: rgba(0, 217, 255, 0.02);
      padding: 0.8rem 1.5rem;
      border-radius: 60px;
      border: 1px solid rgba(0, 217, 255, 0.04);
    }

    .tagline i {
      font-style: italic;
      color: #89b9ff;
    }

    /* stack sections */
    .section-label {
      display: flex;
      align-items: center;
      gap: 0.75rem;
      margin: 2rem 0 1.2rem 0;
    }

    .section-label span {
      font-weight: 600;
      font-size: 1.1rem;
      letter-spacing: 0.5px;
      color: #eef3fc;
      background: #1a212b;
      padding: 0.2rem 1.2rem;
      border-radius: 40px;
      border: 1px solid #2a3340;
    }

    .section-label .line {
      flex: 1;
      height: 1px;
      background: linear-gradient(90deg, #2a3340, transparent);
    }

    .stack-grid {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 1rem 1.5rem;
      background: #0d1117;
      padding: 1.2rem 1.2rem;
      border-radius: 40px;
      border: 1px solid #1f2833;
    }

    .stack-grid img {
      height: 44px;
      width: auto;
      filter: drop-shadow(0 0 4px rgba(0, 217, 255, 0.08));
      transition: 0.2s;
    }

    .stack-grid img:hover {
      transform: translateY(-2px);
      filter: drop-shadow(0 0 10px #00d9ff30);
    }

    /* right now table */
    .now-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 0.6rem 1.2rem;
      background: #0d1117;
      padding: 1.2rem 1.8rem;
      border-radius: 30px;
      border: 1px solid #1f2833;
      margin: 0.5rem 0 0.2rem;
    }

    .now-item {
      display: flex;
      align-items: center;
      gap: 0.6rem;
      color: #d0d9e6;
      font-weight: 400;
      font-size: 0.95rem;
      padding: 0.25rem 0;
    }

    .now-item .dot {
      font-size: 1.2rem;
      line-height: 1;
      color: #00d9ff;
      filter: drop-shadow(0 0 6px #00d9ff40);
    }

    /* stats */
    .stats-wrap {
      display: flex;
      justify-content: center;
      background: #0d1117;
      padding: 0.8rem 0.8rem;
      border-radius: 40px;
      border: 1px solid #1f2833;
    }

    .stats-wrap img {
      max-width: 100%;
      height: auto;
      border-radius: 16px;
    }

    /* connect buttons */
    .connect-grid {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 0.6rem 0.8rem;
      margin: 0.5rem 0 0.2rem;
    }

    .connect-btn {
      background: #0d1117;
      border: 1px solid #232d3b;
      border-radius: 60px;
      padding: 0.45rem 1.4rem;
      color: #b0c4dd;
      font-weight: 500;
      font-size: 0.85rem;
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      text-decoration: none;
      transition: 0.2s;
      letter-spacing: 0.2px;
    }

    .connect-btn:hover {
      border-color: #00d9ff80;
      background: #00d9ff08;
      color: #ffffff;
      transform: translateY(-1px);
      box-shadow: 0 0 16px #00d9ff10;
    }

    .connect-btn i {
      font-style: normal;
      font-weight: 400;
      opacity: 0.6;
    }

    /* footer quote */
    .quote {
      text-align: center;
      margin: 1.8rem 0 0.2rem;
      color: #a0b2cc;
      font-size: 0.95rem;
      letter-spacing: 0.3px;
      background: rgba(0, 217, 255, 0.02);
      padding: 0.6rem 1.2rem;
      border-radius: 60px;
      border: 1px solid rgba(0, 217, 255, 0.04);
    }

    .quote i {
      color: #7aa9ff;
    }

    .footnote {
      text-align: center;
      color: #4b5a6f;
      font-size: 0.7rem;
      letter-spacing: 1px;
      margin-top: 1.2rem;
      opacity: 0.5;
    }

    /* responsive */
    @media (max-width: 600px) {
      .readme-card {
        padding: 1.8rem 1.2rem;
        border-radius: 2rem;
      }
      .name-title h1 {
        font-size: 2.4rem;
      }
      .now-grid {
        grid-template-columns: 1fr;
        gap: 0.3rem;
        padding: 1rem 1.2rem;
      }
      .stack-grid {
        gap: 0.6rem 0.8rem;
        padding: 0.8rem 0.8rem;
      }
      .stack-grid img {
        height: 36px;
      }
      .tagline {
        font-size: 0.95rem;
        padding: 0.6rem 1rem;
      }
    }

    /* custom ascii decoration */
    .ascii-ornament {
      text-align: center;
      color: #1f2a36;
      font-size: 0.6rem;
      letter-spacing: 4px;
      margin: 0.2rem 0 0.6rem;
      font-weight: 300;
      opacity: 0.5;
      user-select: none;
      font-family: 'Inter', monospace;
    }
  </style>
</head>
<body>
<div class="readme-card">

  <!-- header GIF (replacing with a modern, clean visual) -->
  <div class="header-gif">
    <img src="./gif/Jeff-coding-quality.gif" alt="coding quality header" onerror="this.style.display='none'" />
  </div>

  <!-- divider -->
  <div class="divider"></div>

  <!-- name + title -->
  <div class="name-title">
    <h1>JHON HAROLD RUEDA</h1>
    <div class="subhead">
      <span style="opacity:0.7;">✦</span> FULL STACK WEBSITE DEVELOPER · ZAMBOANGA CITY, PH 🇵🇭 <span style="opacity:0.7;">✦</span>
    </div>
  </div>

  <!-- tagline -->
  <div class="tagline">
    <i>“</i> React interfaces on top, Node &amp; PHP APIs underneath, backed by SQL and Firebase.<br />
    <span style="color:#b0c8f0;">Currently open to my next project.</span>
  </div>

  <!-- divider -->
  <div class="divider"></div>

  <!-- Stack -->
  <div class="section-label">
    <span>⚡ stack</span>
    <div class="line"></div>
  </div>

  <div class="stack-grid">
    <img src="https://skillicons.dev/icons?i=react,ts,js,html,css,tailwind&theme=dark" alt="frontend" />
    <img src="https://skillicons.dev/icons?i=nodejs,express,php,python,mysql,postgres,firebase,supabase&theme=dark" alt="backend" />
    <img src="https://skillicons.dev/icons?i=git,github,figma,vscode,vercel,jenkins,githubactions,npm&theme=dark" alt="tools" />
  </div>

  <!-- Right now -->
  <div class="section-label" style="margin-top:2.2rem;">
    <span>🟢 right now</span>
    <div class="line"></div>
  </div>

  <div class="now-grid">
    <div class="now-item"><span class="dot">🟢</span> Open to new projects &amp; collabs</div>
    <div class="now-item"><span class="dot">🎨</span> Refining dashboard UI/UX in React</div>
    <div class="now-item"><span class="dot">⚙️</span> Sharpening backend — APIs that scale</div>
    <div class="now-item"><span class="dot">🌐</span> Building my own business website</div>
  </div>

  <!-- Stats -->
  <div class="section-label" style="margin-top:2.2rem;">
    <span>📊 stats</span>
    <div class="line"></div>
  </div>

  <div class="stats-wrap">
    <img 
      height="165" 
      src="https://github-readme-stats-sigma-five.vercel.app/api?username=Ampexqt&show_icons=true&hide_border=true&hide_title=true&theme=tokyonight&bg_color=0d1117&title_color=00d9ff&icon_color=00d9ff&text_color=c9d1d9" 
      alt="github stats" 
    />
  </div>

  <!-- Connect -->
  <div class="section-label" style="margin-top:2.2rem;">
    <span>🔗 connect</span>
    <div class="line"></div>
  </div>

  <div class="connect-grid">
    <a href="https://www.facebook.com/haroldzkie23" class="connect-btn">📘 Facebook</a>
    <a href="https://www.instagram.com/ampexxqt" class="connect-btn">📸 Instagram</a>
    <a href="https://www.tiktok.com/@ampexqt" class="connect-btn">🎵 TikTok</a>
    <a href="https://haroldqt.vercel.app/" class="connect-btn">⚡ Portfolio</a>
    <a href="mailto:haroldzkie99@gmail.com" class="connect-btn">✉️ Email</a>
  </div>

  <!-- quote -->
  <div class="quote">
    <i>“</i> If it works, improve it. If it's clean, scale it. <i>”</i>
  </div>

  <!-- ascii ornament -->
  <div class="ascii-ornament">
    ═══ ⋆⋅☆⋅⋆ ═══
  </div>

  <!-- subtle footer -->
  <div class="footnote">
    ✦ built with precision · zamboanga city ✦
  </div>
</div>
</body>
</html>
