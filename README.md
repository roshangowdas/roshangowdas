<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Roshan · GitHub Profile</title>
  <!-- Font Awesome 6 (free) -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #0d1117;
      font-family: 'Segoe UI', 'Helvetica Neue', system-ui, -apple-system, sans-serif;
      color: #e6edf3;
      padding: 2rem 1.5rem;
      display: flex;
      justify-content: center;
    }

    .profile-card {
      max-width: 1200px;
      width: 100%;
      background: #161b22;
      border-radius: 32px;
      padding: 2rem 2rem 2.5rem;
      box-shadow: 0 12px 40px rgba(0,0,0,0.6);
      border: 1px solid #30363d;
    }

    /* header wave image (replaces capsule) */
    .wave-header {
      width: 100%;
      border-radius: 24px;
      overflow: hidden;
      margin-bottom: 1.8rem;
      background: linear-gradient(145deg, #0d1117, #161b22);
      position: relative;
    }

    .wave-header img {
      display: block;
      width: 100%;
      height: auto;
      object-fit: cover;
    }

    /* social badges */
    .social-links {
      display: flex;
      justify-content: center;
      gap: 1.2rem;
      flex-wrap: wrap;
      margin: 0.5rem 0 2rem 0;
    }

    .social-links a {
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      background: #21262d;
      padding: 0.5rem 1.2rem;
      border-radius: 40px;
      color: #e6edf3;
      text-decoration: none;
      font-weight: 500;
      font-size: 0.95rem;
      border: 1px solid #30363d;
      transition: all 0.2s ease;
    }

    .social-links a:hover {
      background: #30363d;
      border-color: #58a6ff;
      transform: translateY(-2px);
    }

    .social-links a i {
      font-size: 1.1rem;
    }

    /* about me table */
    .about-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 2rem;
      background: #0d1117;
      border-radius: 24px;
      padding: 1.8rem 2rem;
      margin: 2rem 0 2.2rem 0;
      border: 1px solid #30363d;
    }

    .about-text {
      flex: 2;
      min-width: 260px;
    }

    .about-text h2 {
      font-size: 1.6rem;
      font-weight: 600;
      margin-bottom: 0.75rem;
      color: #f0f6fc;
    }

    .about-text p {
      line-height: 1.7;
      color: #c9d1d9;
      margin-bottom: 0.8rem;
    }

    .about-text .highlight {
      color: #58a6ff;
      font-weight: 500;
    }

    .about-text .code-tag {
      background: #21262d;
      padding: 0.15rem 0.6rem;
      border-radius: 12px;
      font-family: 'JetBrains Mono', 'Fira Code', monospace;
      font-size: 0.9rem;
      color: #f0883e;
      border: 1px solid #30363d;
    }

    .about-image {
      flex: 1;
      min-width: 150px;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .about-image img {
      width: 100%;
      max-width: 300px;
      border-radius: 20px;
      border: 1px solid #30363d;
      box-shadow: 0 8px 24px rgba(0,0,0,0.5);
      transition: transform 0.2s;
    }

    .about-image img:hover {
      transform: scale(1.01);
    }

    /* tech badges */
    .tech-cloud {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 0.6rem 0.9rem;
      margin: 1.8rem 0 2.2rem 0;
      padding: 0.6rem 1rem;
      background: #0d1117;
      border-radius: 40px;
      border: 1px solid #30363d;
    }

    .tech-cloud span {
      background: #21262d;
      padding: 0.3rem 1rem;
      border-radius: 30px;
      font-size: 0.85rem;
      font-weight: 500;
      color: #c9d1d9;
      border: 1px solid #30363d;
      transition: 0.15s;
    }

    .tech-cloud span i {
      margin-right: 6px;
      font-size: 0.9rem;
    }

    .tech-cloud span:hover {
      background: #30363d;
      border-color: #58a6ff;
      color: #f0f6fc;
    }

    /* stats grid */
    .stats-row {
      display: flex;
      flex-wrap: wrap;
      gap: 1.5rem;
      margin: 2rem 0 1.5rem 0;
    }

    .stats-row > div {
      flex: 1 1 280px;
      background: #0d1117;
      border-radius: 20px;
      padding: 0.5rem;
      border: 1px solid #30363d;
      transition: border 0.2s;
    }

    .stats-row > div:hover {
      border-color: #58a6ff50;
    }

    .stats-row img {
      width: 100%;
      height: auto;
      display: block;
      border-radius: 16px;
    }

    .lang-chart {
      max-width: 600px;
      margin: 1rem auto 0.8rem auto;
      background: #0d1117;
      border-radius: 24px;
      padding: 0.5rem;
      border: 1px solid #30363d;
    }

    .lang-chart img {
      width: 100%;
      height: auto;
      display: block;
      border-radius: 16px;
    }

    /* trophies + quote */
    .trophy-section, .quote-section, .contrib-section {
      background: #0d1117;
      border-radius: 24px;
      padding: 1.2rem 1rem;
      margin: 2rem 0 1.5rem 0;
      border: 1px solid #30363d;
      text-align: center;
    }

    .trophy-section img, .quote-section img, .contrib-section img {
      max-width: 100%;
      height: auto;
      border-radius: 16px;
    }

    .contrib-section {
      margin-top: 0.8rem;
    }

    .visitor {
      text-align: center;
      margin-top: 2rem;
      font-size: 0.9rem;
      color: #8b949e;
      border-top: 1px solid #30363d;
      padding-top: 1.8rem;
    }

    .visitor img {
      vertical-align: middle;
      margin-right: 6px;
    }

    /* responsiveness */
    @media (max-width: 700px) {
      .profile-card {
        padding: 1.2rem;
      }
      .about-grid {
        flex-direction: column;
        padding: 1.5rem;
      }
      .about-image img {
        max-width: 100%;
      }
      .social-links a {
        padding: 0.4rem 1rem;
        font-size: 0.8rem;
      }
    }

    /* extra polish for quote */
    .quote-section img {
      background: #161b22;
      padding: 0.4rem 0.8rem;
    }

    /* fix for graph contribution: replaced with actual contribution graph image from gh */
    .contribution-graph-wrapper {
      background: #0d1117;
      border-radius: 24px;
      padding: 0.75rem 0.75rem 0.2rem 0.75rem;
      margin: 1.8rem 0 0.5rem 0;
      border: 1px solid #30363d;
      text-align: center;
    }

    .contribution-graph-wrapper img {
      max-width: 100%;
      border-radius: 16px;
      background: #0d1117;
    }

    .section-title {
      font-size: 1.2rem;
      font-weight: 500;
      color: #f0f6fc;
      margin-bottom: 0.6rem;
      display: flex;
      align-items: center;
      gap: 0.5rem;
      justify-content: center;
    }

    .section-title i {
      color: #58a6ff;
    }
  </style>
</head>
<body>
<div class="profile-card">

  <!-- wave header (capsule render) -->
  <div class="wave-header">
    <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=0,2,20,30,40&height=220&section=header&text=Welcome%20to%20Roshan's%20GitHub&fontSize=50&fontColor=fff&animation=fadeIn&fontAlignY=38" alt="wave header" />
  </div>

  <!-- social icons -->
  <div class="social-links">
    <a href="https://linkedin.com/in/roshangowdas" target="_blank"><i class="fab fa-linkedin"></i> LinkedIn</a>
    <a href="https://github.com/roshangowdas" target="_blank"><i class="fab fa-github"></i> GitHub</a>
    <a href="mailto:roshangowdas@gmail.com"><i class="fas fa-envelope"></i> Email</a>
  </div>

  <!-- about me -->
  <div class="about-grid">
    <div class="about-text">
      <h2>👨‍💻 About Me</h2>
      <p>Hello there! I'm <strong>Roshan Gowda S</strong>, an Information Science and Engineering student at Nagarjuna College of Engineering and Technology, Bengaluru.</p>
      <p>Specializing in full-stack MERN development, I've published an open-source npm package (<span class="code-tag">@roshan__gowda/react-status-kit</span>) and built multi-user web platforms end-to-end, from database design to deployment, using AI developer tools (Google AI Studio, Gemini API) to accelerate delivery.</p>
      <p>📍 Bengaluru, Karnataka, India</p>
    </div>
    <div class="about-image">
      <img src="https://images.unsplash.com/photo-1555066931-4365d14bab8c?auto=format&fit=crop&w=500&q=80" alt="Developer setup" />
    </div>
  </div>

  <!-- technologies -->
  <div class="tech-cloud">
    <span><i class="fab fa-js"></i> JavaScript</span>
    <span><i class="fab fa-react"></i> React</span>
    <span><i class="fab fa-node"></i> Node.js</span>
    <span><i class="fas fa-code"></i> Express.js</span>
    <span><i class="fas fa-database"></i> MongoDB</span>
    <span><i class="fab fa-html5"></i> HTML5</span>
    <span><i class="fab fa-css3-alt"></i> CSS3</span>
    <span><i class="fab fa-tailwind"></i> Tailwind</span>
    <span><i class="fab fa-python"></i> Python</span>
    <span><i class="fas fa-copyright"></i> C++</span>
    <span><i class="fab fa-java"></i> Java</span>
    <span><i class="fab fa-git-alt"></i> Git</span>
    <span><i class="fab fa-github"></i> GitHub</span>
    <span><i class="fas fa-fire"></i> Firebase</span>
    <span><i class="fas fa-cloud"></i> REST API</span>
  </div>

  <!-- ====== CONTRIBUTION GRAPH (FIXED) ====== -->
  <div class="section-title">
    <i class="fas fa-chart-line"></i> Contribution Graph
  </div>
  <div class="contribution-graph-wrapper">
    <!-- using the official GitHub contribution chart image (embed) -->
    <img src="https://ghchart.rshah.org/roshangowdas" alt="Roshan's GitHub Contribution Chart" />
    <!-- fallback note: if the chart doesn't load, it's a dynamic svg from the service -->
    <p style="color:#8b949e; font-size:0.8rem; margin-top:6px;">⬆️ contribution calendar (powered by ghchart.rshah.org)</p>
  </div>

  <!-- stats: 2 columns -->
  <div class="stats-row">
    <div><img src="https://github-readme-stats.shion.dev/api?username=roshangowdas&theme=dark&hide_border=false&include_all_commits=true&count_private=true" alt="GitHub stats" /></div>
    <div><img src="https://streak-stats.demolab.com/?user=roshangowdas&theme=dark&hide_border=false" alt="Streak stats" /></div>
  </div>

  <!-- top languages -->
  <div class="lang-chart">
    <img src="https://github-readme-stats.shion.dev/api/top-langs/?username=roshangowdas&theme=dark&hide_border=false&include_all_commits=true&count_private=true&layout=compact" alt="Top languages" />
  </div>

  <!-- trophies -->
  <div class="trophy-section">
    <div class="section-title"><i class="fas fa-trophy"></i> GitHub Trophies</div>
    <img src="https://github-profile-trophy.vercel.app/?username=roshangowdas&theme=radical&no-frame=false&no-bg=true&margin-w=4" alt="Trophies" />
  </div>

  <!-- quote -->
  <div class="quote-section">
    <div class="section-title"><i class="fas fa-quote-left"></i> Random Dev Quote</div>
    <img src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=radical" alt="Dev quote" />
  </div>

  <!-- top contributed repo -->
  <div class="contrib-section">
    <div class="section-title"><i class="fas fa-code-branch"></i> Top Contributed Repo</div>
    <img src="https://github-contributor-stats.vercel.app/api?username=roshangowdas&limit=5&theme=dark&combine_all_yearly_contributions=true" alt="Top contributed" />
  </div>

  <!-- visitor count -->
  <div class="visitor">
    <img src="https://komarev.com/ghpvc/?username=roshangowdas&icon=0&color=0" alt="Visitor Count" />
    <span style="margin-left: 6px;">profile views</span>
  </div>

</div>
</body>
</html>
