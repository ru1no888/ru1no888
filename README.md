<!doctype html>
<html lang="th">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Thanakorn Portfolio | Fusion 2+1</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Kanit:wght@300;400;600;700;800&display=swap" rel="stylesheet" />
  <style>
    :root {
      --bg-1: #07121f;
      --bg-2: #0b1d33;
      --panel: rgba(7, 18, 31, 0.74);
      --line: rgba(255, 255, 255, 0.15);
      --text: #eaf2ff;
      --muted: #a0b5cf;
      --brand-1: #16a34a;
      --brand-2: #06b6d4;
      --brand-3: #f59e0b;
      --shadow: 0 24px 52px rgba(0, 0, 0, 0.35);
      --radius: 18px;
    }

    * {
      box-sizing: border-box;
    }

    html,
    body {
      margin: 0;
      padding: 0;
    }

    body {
      font-family: "Kanit", sans-serif;
      color: var(--text);
      background:
        radial-gradient(1200px 650px at 85% -15%, rgba(6, 182, 212, 0.26), transparent 55%),
        radial-gradient(900px 600px at -10% 10%, rgba(245, 158, 11, 0.18), transparent 60%),
        linear-gradient(150deg, var(--bg-1) 0%, var(--bg-2) 55%, #0f172a 100%);
      min-height: 100vh;
      overflow-x: hidden;
    }

    .grain {
      position: fixed;
      inset: 0;
      pointer-events: none;
      z-index: 0;
      opacity: 0.3;
      background:
        repeating-linear-gradient(
          115deg,
          rgba(255, 255, 255, 0.02) 0px,
          rgba(255, 255, 255, 0.02) 1px,
          transparent 1px,
          transparent 14px
        );
    }

    .orb {
      position: fixed;
      width: 34vmax;
      aspect-ratio: 1;
      border-radius: 50%;
      filter: blur(45px);
      z-index: 0;
      opacity: 0.22;
      animation: floaty 14s ease-in-out infinite alternate;
    }

    .orb.a {
      left: -12vmax;
      top: -8vmax;
      background: var(--brand-1);
    }

    .orb.b {
      right: -14vmax;
      bottom: -12vmax;
      background: var(--brand-2);
      animation-delay: 1.2s;
    }

    @keyframes floaty {
      from {
        transform: translate(0, 0) scale(1);
      }
      to {
        transform: translate(30px, 24px) scale(1.08);
      }
    }

    .wrap {
      width: min(1160px, 92vw);
      margin: 0 auto;
      padding: 24px 0 78px;
      position: relative;
      z-index: 1;
    }

    .nav {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 12px;
      position: sticky;
      top: 10px;
      z-index: 20;
      padding: 12px 14px;
      border: 1px solid var(--line);
      border-radius: 999px;
      background: rgba(7, 18, 31, 0.64);
      backdrop-filter: blur(10px);
    }

    .brand {
      font-weight: 800;
      letter-spacing: 0.4px;
      font-size: 1.05rem;
      white-space: nowrap;
    }

    .brand i {
      font-style: normal;
      color: var(--brand-2);
    }

    .menu {
      display: flex;
      gap: 14px;
      flex-wrap: wrap;
    }

    .menu a {
      color: var(--muted);
      text-decoration: none;
      font-weight: 600;
      transition: 0.2s ease;
    }

    .menu a:hover {
      color: var(--text);
      transform: translateY(-1px);
    }

    .panel {
      border: 1px solid var(--line);
      border-radius: var(--radius);
      background: var(--panel);
      backdrop-filter: blur(8px);
      box-shadow: var(--shadow);
    }

    .hero {
      margin-top: 26px;
      display: grid;
      grid-template-columns: 1.25fr 0.75fr;
      gap: 16px;
    }

    .hero-main {
      padding: 28px;
    }

    .pill {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      border: 1px solid rgba(52, 211, 153, 0.45);
      color: #bef9dc;
      background: rgba(22, 163, 74, 0.17);
      border-radius: 999px;
      padding: 6px 12px;
      font-size: 0.9rem;
    }

    .hero h1 {
      margin: 14px 0 10px;
      font-size: clamp(1.9rem, 5vw, 3.2rem);
      line-height: 1.08;
      letter-spacing: 0.25px;
    }

    .hero p {
      margin: 0;
      color: var(--muted);
      line-height: 1.7;
      font-size: 1.04rem;
    }

    .chips {
      margin-top: 16px;
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
    }

    .chip {
      font-size: 0.86rem;
      padding: 6px 10px;
      border-radius: 999px;
      border: 1px solid rgba(6, 182, 212, 0.35);
      background: rgba(6, 182, 212, 0.1);
      color: #b8ecf6;
      animation: softPulse 3s ease-in-out infinite;
    }

    .chip:nth-child(2n) {
      animation-delay: 0.4s;
    }

    .chip:nth-child(3n) {
      animation-delay: 0.9s;
    }

    @keyframes softPulse {
      0%,
      100% {
        transform: translateY(0);
        opacity: 0.95;
      }
      50% {
        transform: translateY(-2px);
        opacity: 1;
      }
    }

    .status {
      margin-top: 10px;
      color: #c7d2fe;
      font-size: 0.9rem;
      min-height: 1.2em;
    }

    .hero-side {
      padding: 18px;
      display: grid;
      gap: 10px;
    }

    .profile-head {
      display: flex;
      align-items: center;
      gap: 10px;
      padding-bottom: 8px;
      border-bottom: 1px dashed var(--line);
    }

    .avatar {
      width: 52px;
      height: 52px;
      border-radius: 50%;
      border: 2px solid rgba(255, 255, 255, 0.24);
      object-fit: cover;
    }

    .uname {
      margin: 0;
      font-weight: 700;
      font-size: 1.02rem;
      line-height: 1.2;
    }

    .small {
      color: var(--muted);
      margin: 0;
      font-size: 0.88rem;
    }

    .stat-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 10px;
    }

    .stat {
      border: 1px solid var(--line);
      border-radius: 12px;
      padding: 12px;
      background: rgba(255, 255, 255, 0.03);
    }

    .num {
      font-size: 1.45rem;
      font-weight: 800;
      line-height: 1.1;
    }

    .lbl {
      color: var(--muted);
      font-size: 0.82rem;
    }

    .section-title {
      margin: 32px 0 12px;
      font-size: 1.25rem;
      font-weight: 800;
      letter-spacing: 0.2px;
    }

    .cards {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 12px;
    }

    .card {
      border: 1px solid var(--line);
      border-radius: 14px;
      padding: 14px;
      background: rgba(2, 8, 23, 0.5);
      transition: transform 0.22s ease, border-color 0.22s ease;
    }

    .card:hover {
      transform: translateY(-4px);
      border-color: rgba(6, 182, 212, 0.5);
    }

    .card h3 {
      margin: 0 0 6px;
      font-size: 1rem;
    }

    .card p {
      margin: 0;
      color: var(--muted);
      line-height: 1.6;
      font-size: 0.94rem;
    }

    .lang {
      margin-top: 10px;
      display: inline-block;
      font-size: 0.78rem;
      color: #a7d8ff;
      background: rgba(59, 130, 246, 0.12);
      border: 1px solid rgba(96, 165, 250, 0.35);
      padding: 4px 8px;
      border-radius: 999px;
    }

    .projects {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 12px;
    }

    .timeline {
      display: grid;
      gap: 10px;
      margin-top: 8px;
    }

    .step {
      display: flex;
      gap: 10px;
      border: 1px solid var(--line);
      border-radius: 14px;
      padding: 12px 14px;
      background: rgba(255, 255, 255, 0.025);
    }

    .dot {
      width: 11px;
      height: 11px;
      border-radius: 50%;
      margin-top: 7px;
      flex: 0 0 auto;
      background: linear-gradient(180deg, var(--brand-3), #ea580c);
      box-shadow: 0 0 0 4px rgba(245, 158, 11, 0.18);
    }

    .step b {
      display: block;
      margin-bottom: 2px;
    }

    .step span {
      color: var(--muted);
    }

    .footer {
      margin-top: 24px;
      color: var(--muted);
      text-align: center;
      font-size: 0.9rem;
    }

    .footer a {
      color: #b9e8ff;
    }

    .reveal {
      opacity: 0;
      transform: translateY(16px) scale(0.985);
      transition: all 0.65s cubic-bezier(0.2, 0.68, 0.2, 1);
    }

    .reveal.show {
      opacity: 1;
      transform: translateY(0) scale(1);
    }

    @media (max-width: 980px) {
      .hero {
        grid-template-columns: 1fr;
      }

      .cards {
        grid-template-columns: 1fr 1fr;
      }
    }

    @media (max-width: 680px) {
      .menu {
        display: none;
      }

      .projects {
        grid-template-columns: 1fr;
      }

      .cards {
        grid-template-columns: 1fr;
      }

      .hero-main {
        padding: 20px;
      }

      .hero-side {
        padding: 14px;
      }
    }
  </style>
</head>
<body>
  <div class="grain"></div>
  <div class="orb a"></div>
  <div class="orb b"></div>

  <main class="wrap">
    <nav class="nav panel">
      <div class="brand">Profile <i>Fusion 2+1</i></div>
      <div class="menu">
        <a href="#repos">Repositories</a>
        <a href="#featured">Featured</a>
        <a href="#roadmap">Roadmap</a>
      </div>
    </nav>

    <section class="hero">
      <article class="hero-main panel reveal">
        <div class="pill">Live Data from GitHub</div>
        <h1 id="title">Loading profile...</h1>
        <p id="bio">Please wait, loading latest profile information.</p>
        <div class="chips">
          <span class="chip">IoT</span>
          <span class="chip">Embedded</span>
          <span class="chip">FastAPI</span>
          <span class="chip">Django</span>
          <span class="chip">Spring Boot</span>
          <span class="chip">Automation</span>
        </div>
        <p class="status" id="status"></p>
      </article>

      <aside class="hero-side panel reveal">
        <div class="profile-head">
          <img id="avatar" class="avatar" alt="avatar" src="https://avatars.githubusercontent.com/u/200022091?v=4" />
          <div>
            <p id="nameMini" class="uname">ru1no888</p>
            <p id="loginMini" class="small">@ru1no888</p>
          </div>
        </div>

        <div class="stat-grid">
          <div class="stat">
            <div class="num" id="followers">0</div>
            <div class="lbl">Followers</div>
          </div>
          <div class="stat">
            <div class="num" id="following">0</div>
            <div class="lbl">Following</div>
          </div>
          <div class="stat">
            <div class="num" id="publicRepos">0</div>
            <div class="lbl">Public Repos</div>
          </div>
          <div class="stat">
            <div class="num" id="locationMini">Khon Kaen</div>
            <div class="lbl">Location</div>
          </div>
        </div>
      </aside>
    </section>

    <h2 class="section-title" id="repos">Popular Repositories</h2>
    <section class="cards" id="repoGrid">
      <article class="card reveal">
        <h3>Loading repositories...</h3>
        <p>Fetching your latest repositories from GitHub.</p>
      </article>
    </section>

    <h2 class="section-title" id="featured">Featured Projects</h2>
    <section class="projects">
      <article class="card reveal">
        <h3>Smart Health Monitoring</h3>
        <p>Wearable IoT thesis for real-time health data acquisition, transmission and analysis.</p>
        <span class="lang">ESP32 • MQTT • FastAPI • Digital Twin</span>
      </article>
      <article class="card reveal">
        <h3>IoT Security Matrix</h3>
        <p>Multi-sensor ESP32 security system with synchronized event handling and APIs.</p>
        <span class="lang">ESP32 • C/C++ • Arduino • REST API</span>
      </article>
      <article class="card reveal">
        <h3>Smart Medicine Storage</h3>
        <p>Environment monitoring, API bridge and simulation workflow via Wokwi.</p>
        <span class="lang">ESP32 • Python • REST API • Wokwi</span>
      </article>
      <article class="card reveal">
        <h3>Dino Forum Web App</h3>
        <p>Full-stack community forum with authentication, CRUD and responsive UI.</p>
        <span class="lang">Django • Spring Boot • SQL • Web</span>
      </article>
    </section>

    <h2 class="section-title" id="roadmap">Roadmap Style 2+1</h2>
    <section class="timeline">
      <div class="step reveal">
        <div class="dot"></div>
        <div>
          <b>Phase 1: Profile Identity</b>
          <span>Professional layout with clear hero and important profile metrics.</span>
        </div>
      </div>
      <div class="step reveal">
        <div class="dot"></div>
        <div>
          <b>Phase 2: Motion + Readability</b>
          <span>Balanced animations and clean cards that keep content easy to scan.</span>
        </div>
      </div>
      <div class="step reveal">
        <div class="dot"></div>
        <div>
          <b>Phase 3: Live GitHub Sync</b>
          <span>Real profile and repository data from API with safe fallback values.</span>
        </div>
      </div>
    </section>

    <p class="footer">
      GitHub:
      <a href="https://github.com/ru1no888" target="_blank" rel="noreferrer">ru1no888</a>
      • Updated live from GitHub API
    </p>
  </main>

  <script>
    const USERNAME = "ru1no888";
    const statusEl = document.getElementById("status");

    function animateCount(el, target, ms = 900) {
      const n = Number(target) || 0;
      const start = performance.now();

      function tick(now) {
        const p = Math.min((now - start) / ms, 1);
        const eased = 1 - Math.pow(1 - p, 3);
        el.textContent = Math.round(n * eased).toLocaleString("en-US");
        if (p < 1) requestAnimationFrame(tick);
      }

      requestAnimationFrame(tick);
    }

    function setProfile(data) {
      const displayName = data.name || USERNAME;
      document.getElementById("title").textContent = displayName + " | Portfolio Fusion";
      document.getElementById("bio").textContent =
        data.bio || "Computer Engineering student focused on IoT, full-stack development and AI automation.";
      document.getElementById("nameMini").textContent = displayName;
      document.getElementById("loginMini").textContent = "@" + (data.login || USERNAME);
      document.getElementById("avatar").src = data.avatar_url || document.getElementById("avatar").src;
      document.getElementById("locationMini").textContent = data.location || "Thailand";

      animateCount(document.getElementById("followers"), data.followers || 0);
      animateCount(document.getElementById("following"), data.following || 0);
      animateCount(document.getElementById("publicRepos"), data.public_repos || 0);
    }

    function renderRepos(repos) {
      const grid = document.getElementById("repoGrid");
      if (!Array.isArray(repos) || repos.length === 0) {
        grid.innerHTML =
          '<article class="card reveal show"><h3>No repository data found</h3><p>Try reloading or check internet connection.</p></article>';
        return;
      }

      const top = repos
        .filter((r) => !r.fork)
        .sort(
          (a, b) =>
            (b.stargazers_count - a.stargazers_count) ||
            new Date(b.updated_at) - new Date(a.updated_at)
        )
        .slice(0, 6);

      grid.innerHTML = top
        .map((r) => {
          const desc = r.description || "No description";
          const lang = r.language || "Mixed";
          const stars = r.stargazers_count || 0;
          return (
            '<article class="card reveal show">' +
            '<h3><a href="' + r.html_url + '" target="_blank" rel="noreferrer" style="color:inherit;text-decoration:none">' + r.name + "</a></h3>" +
            "<p>" + desc + "</p>" +
            '<span class="lang">' + lang + " • ★ " + stars + "</span>" +
            "</article>"
          );
        })
        .join("");
    }

    async function loadGitHubData() {
      try {
        statusEl.textContent = "Loading live data from GitHub...";

        const [userRes, repoRes] = await Promise.all([
          fetch("https://api.github.com/users/" + USERNAME),
          fetch("https://api.github.com/users/" + USERNAME + "/repos?per_page=100&sort=updated"),
        ]);

        if (!userRes.ok || !repoRes.ok) {
          throw new Error("GitHub API error");
        }

        const userData = await userRes.json();
        const repoData = await repoRes.json();

        setProfile(userData);
        renderRepos(repoData);

        const updateDate = new Date(userData.updated_at || Date.now());
        statusEl.textContent = "Last sync: " + updateDate.toLocaleString("en-US");
      } catch (error) {
        statusEl.textContent = "Live sync failed. Showing fallback data.";
        setProfile({
          name: "Thanakorn Supawanchai",
          login: "ru1no888",
          bio: "Computer Engineering student focused on IoT, full-stack and AI automation.",
          followers: 1,
          following: 1,
          public_repos: 12,
          location: "Khon Kaen, Thailand",
          avatar_url: "https://avatars.githubusercontent.com/u/200022091?v=4",
        });
        renderRepos([
          {
            name: "IOT-smart-Warehouse-Mini-Project",
            description: "IoT warehouse mini project",
            language: "PHP",
            stargazers_count: 1,
            fork: false,
            updated_at: "2026-03-01",
            html_url: "https://github.com/ru1no888/IOT-smart-Warehouse-Mini-Project"
          },
          {
            name: "mini-forum",
            description: "Community forum project",
            language: "JavaScript",
            stargazers_count: 0,
            fork: false,
            updated_at: "2026-03-10",
            html_url: "https://github.com/ru1no888/mini-forum"
          },
          {
            name: "miniprodatabase",
            description: "Mini database practice",
            language: "HTML",
            stargazers_count: 0,
            fork: false,
            updated_at: "2026-03-10",
            html_url: "https://github.com/ru1no888/miniprodatabase"
          },
        ]);
      }
    }

    const io = new IntersectionObserver(
      (entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting) {
            entry.target.classList.add("show");
            io.unobserve(entry.target);
          }
        });
      },
      { threshold: 0.16 }
    );

    document.querySelectorAll(".reveal").forEach((el) => io.observe(el));
    loadGitHubData();
  </script>
</body>
</html>
