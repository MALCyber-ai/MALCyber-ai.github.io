<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Welcome to My Cybersecurity Journey</title>
  <meta name="description" content="A cybersecurity student breaking down complex security concepts into plain, everyday language.">
  <style>
    :root {
      --bg: #0b1220;
      --surface: #131c2e;
      --surface-2: #1a2540;
      --border: #25324d;
      --text: #e6ebf5;
      --muted: #9aa7c0;
      --accent: #3ddc97;
      --accent-2: #5aa9ff;
      --radius: 14px;
    }
    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      margin: 0;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Inter, Roboto, sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height: 1.65;
    }
    a { color: var(--accent-2); text-decoration: none; }
    a:hover { text-decoration: underline; }
    .wrap { max-width: 860px; margin: 0 auto; padding: 0 1.25rem; }

    /* Nav */
    header.nav {
      position: sticky; top: 0; z-index: 10;
      background: rgba(11, 18, 32, 0.85);
      backdrop-filter: blur(10px);
      border-bottom: 1px solid var(--border);
    }
    header.nav .wrap { display: flex; align-items: center; justify-content: space-between; height: 60px; }
    .brand { font-weight: 700; letter-spacing: .02em; color: var(--text); }
    .brand span { color: var(--accent); }
    nav a { margin-left: 1.25rem; color: var(--muted); font-size: .95rem; }
    nav a:hover { color: var(--text); text-decoration: none; }

    /* Hero */
    .hero { padding: 5rem 0 3rem; }
    .eyebrow {
      display: inline-block; padding: .3rem .8rem; border: 1px solid var(--border);
      border-radius: 999px; color: var(--accent); font-size: .85rem; margin-bottom: 1.25rem;
      background: var(--surface);
    }
    h1 { font-size: clamp(2.1rem, 5vw, 3.2rem); line-height: 1.15; margin: 0 0 1.25rem; }
    h1 em { font-style: normal; color: var(--accent); }
    .lead { font-size: 1.15rem; color: var(--muted); max-width: 640px; margin: 0 0 1rem; }
    .cta { display: flex; flex-wrap: wrap; gap: .75rem; margin-top: 2rem; }
    .btn {
      display: inline-flex; align-items: center; gap: .5rem;
      padding: .7rem 1.2rem; border-radius: 10px; font-weight: 600; font-size: .95rem;
      border: 1px solid var(--border); background: var(--surface); color: var(--text);
      cursor: pointer; font-family: inherit; transition: transform .15s, border-color .15s, background .15s;
    }
    .btn:hover { transform: translateY(-2px); border-color: var(--accent); text-decoration: none; }
    .btn.primary { background: var(--accent); color: #07241a; border-color: var(--accent); }
    .btn.primary:hover { background: #5fe8ae; }

    /* Section toolbar */
    .toolbar { display: flex; justify-content: space-between; align-items: center; margin: 2.5rem 0 1rem; }
    .toolbar h2 { margin: 0; font-size: 1.4rem; }
    .toolbar .btn { padding: .45rem .9rem; font-size: .85rem; }

    /* Accordion */
    details {
      background: var(--surface);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      margin-bottom: .85rem;
      overflow: hidden;
      transition: border-color .2s;
    }
    details[open] { border-color: var(--accent); }
    summary {
      list-style: none; cursor: pointer;
      display: flex; align-items: center; gap: .9rem;
      padding: 1.1rem 1.25rem; font-weight: 600; font-size: 1.05rem;
    }
    summary::-webkit-details-marker { display: none; }
    summary:hover { background: var(--surface-2); }
    summary:focus-visible, .btn:focus-visible, a:focus-visible { outline: 2px solid var(--accent-2); outline-offset: 2px; }
    .icon {
      width: 38px; height: 38px; border-radius: 10px; display: grid; place-items: center;
      background: var(--surface-2); font-size: 1.15rem; flex-shrink: 0;
    }
    .summary-text small { display: block; font-weight: 400; color: var(--muted); font-size: .85rem; }
    .chevron { margin-left: auto; transition: transform .25s; color: var(--muted); }
    details[open] .chevron { transform: rotate(180deg); color: var(--accent); }
    .panel { padding: .25rem 1.25rem 1.4rem; border-top: 1px solid var(--border); }
    .panel p { color: var(--muted); }

    /* Cards inside panels */
    .cards { display: grid; gap: .85rem; grid-template-columns: repeat(auto-fill, minmax(240px, 1fr)); margin-top: 1rem; }
    .card {
      background: var(--surface-2); border: 1px solid var(--border);
      border-radius: 12px; padding: 1rem 1.1rem;
    }
    .card h3 { margin: 0 0 .35rem; font-size: 1rem; }
    .card p { margin: 0 0 .75rem; font-size: .9rem; color: var(--muted); }
    .tags { display: flex; flex-wrap: wrap; gap: .4rem; margin-bottom: .6rem; }
    .tag {
      font-size: .75rem; padding: .15rem .55rem; border-radius: 999px;
      background: rgba(61, 220, 151, .12); color: var(--accent);
    }
    .card a { font-size: .9rem; font-weight: 600; }

    ul.skills { list-style: none; padding: 0; margin: 1rem 0 0; display: flex; flex-wrap: wrap; gap: .5rem; }
    ul.skills li {
      padding: .35rem .8rem; border: 1px solid var(--border); border-radius: 999px;
      background: var(--surface-2); font-size: .9rem;
    }

    footer { margin-top: 4rem; padding: 2rem 0; border-top: 1px solid var(--border); color: var(--muted); font-size: .9rem; text-align: center; }

    @media (max-width: 560px) {
      nav a:not(:last-child) { display: none; }
      .hero { padding-top: 3rem; }
    }
    @media (prefers-reduced-motion: reduce) {
      * { transition: none !important; scroll-behavior: auto !important; }
    }
  </style>
</head>
<body>

<header class="nav">
  <div class="wrap">
    <a class="brand" href="#top">cyber<span>.</span>journey</a>
    <nav aria-label="Primary">
      <a href="#explore">Explore</a>
      <a href="https://github.com/YOUR-USERNAME">GitHub</a>
      <a href="https://www.youtube.com/@YOUR-CHANNEL">YouTube</a>
    </nav>
  </div>
</header>

<main id="top" class="wrap">

  <!-- Introduction -->
  <section class="hero">
    <span class="eyebrow">🛡️ Cybersecurity student &amp; educator</span>
    <h1>Welcome to my <em>cybersecurity</em> journey</h1>
    <p class="lead">
      I'm a cybersecurity student on a mission to make the digital world less mysterious.
      Whether you're a total beginner or just curious how hackers work, I break complex
      concepts down into simple, everyday language.
    </p>
    <p class="lead">
      My goal is to give you the knowledge to stay safe online, without needing a computer science degree.
      New videos, code updates and articles every week.
    </p>
    <div class="cta">
      <a class="btn primary" href="#explore">Start exploring ↓</a>
      <a class="btn" href="https://www.youtube.com/@YOUR-CHANNEL">▶ Watch on YouTube</a>
      <a class="btn" href="https://github.com/YOUR-USERNAME">⌘ View GitHub</a>
    </div>
  </section>

  <!-- Expandable sections -->
  <section id="explore" aria-labelledby="explore-title">
    <div class="toolbar">
      <h2 id="explore-title">Explore</h2>
      <button class="btn" id="toggle-all" type="button" aria-pressed="false">Expand all</button>
    </div>

    <details>
      <summary>
        <span class="icon" aria-hidden="true">🧪</span>
        <span class="summary-text">Hands-on Projects<small>Labs, builds and experiments, all documented on GitHub</small></span>
        <span class="chevron" aria-hidden="true">▾</span>
      </summary>
      <div class="panel">
        <div class="cards">
          <article class="card">
            <h3>Home Lab Setup</h3>
            <p>Building an isolated virtual lab for safe security practice.</p>
            <div class="tags"><span class="tag">VirtualBox</span><span class="tag">Kali</span></div>
            <a href="https://github.com/YOUR-USERNAME/project-one">View on GitHub →</a>
          </article>
          <article class="card">
            <h3>Network Scanning with Nmap</h3>
            <p>Mapping hosts and open ports, and what the results actually mean.</p>
            <div class="tags"><span class="tag">Nmap</span><span class="tag">Networking</span></div>
            <a href="https://github.com/YOUR-USERNAME/project-two">View on GitHub →</a>
          </article>
          <article class="card">
            <h3>Your Next Project</h3>
            <p>Replace this card with a short description of your own build.</p>
            <div class="tags"><span class="tag">Python</span></div>
            <a href="https://github.com/YOUR-USERNAME">View on GitHub →</a>
          </article>
        </div>
      </div>
    </details>

    <details>
      <summary>
        <span class="icon" aria-hidden="true">📝</span>
        <span class="summary-text">Blog &amp; Guides<small>Deep-dive articles written for beginners</small></span>
        <span class="chevron" aria-hidden="true">▾</span>
      </summary>
      <div class="panel">
        <div class="cards">
          <article class="card">
            <h3>Article title goes here</h3>
            <p>One-sentence summary of what the reader will learn.</p>
            <a href="/blog/your-first-post">Read article →</a>
          </article>
          <article class="card">
            <h3>Another article title</h3>
            <p>One-sentence summary of what the reader will learn.</p>
            <a href="/blog/your-second-post">Read article →</a>
          </article>
        </div>
        <p><a href="/blog">Browse all articles →</a></p>
      </div>
    </details>

    <details>
      <summary>
        <span class="icon" aria-hidden="true">🎥</span>
        <span class="summary-text">Videos<small>Concepts explained visually on YouTube</small></span>
        <span class="chevron" aria-hidden="true">▾</span>
      </summary>
      <div class="panel">
        <p>New videos every week, covering the basics of how things work and how attackers think.</p>
        <a class="btn" href="https://www.youtube.com/@YOUR-CHANNEL">▶ Visit the channel</a>
      </div>
    </details>

    <details>
      <summary>
        <span class="icon" aria-hidden="true">🧰</span>
        <span class="summary-text">Skills &amp; Tools<small>What I'm learning and working with</small></span>
        <span class="chevron" aria-hidden="true">▾</span>
      </summary>
      <div class="panel">
        <ul class="skills">
          <li>Networking</li>
          <li>Linux</li>
          <li>Python</li>
          <li>Wireshark</li>
          <li>Nmap</li>
          <li>Burp Suite</li>
          <li>Git</li>
        </ul>
      </div>
    </details>

    <details>
      <summary>
        <span class="icon" aria-hidden="true">🎓</span>
        <span class="summary-text">Learning Path &amp; Certifications<small>Where I'm at and where I'm headed</small></span>
        <span class="chevron" aria-hidden="true">▾</span>
      </summary>
      <div class="panel">
        <p>Add your degree, certifications (for example CompTIA Security+) and platforms like TryHackMe or Hack The Box here.</p>
      </div>
    </details>

    <details>
      <summary>
        <span class="icon" aria-hidden="true">✉️</span>
        <span class="summary-text">Get in Touch<small>Questions, ideas or collaboration</small></span>
        <span class="chevron" aria-hidden="true">▾</span>
      </summary>
      <div class="panel">
        <p>I'd love to hear from you.</p>
        <a class="btn" href="mailto:you@example.com">Email me</a>
        <a class="btn" href="https://www.linkedin.com/in/YOUR-PROFILE">LinkedIn</a>
      </div>
    </details>
  </section>
</main>

<footer>
  <div class="wrap">© <span id="year"></span> Your Name · Built with curiosity</div>
</footer>

<script>
  const items = document.querySelectorAll("#explore details");
  const toggle = document.getElementById("toggle-all");

  document.getElementById("year").textContent = new Date().getFullYear();

  // Optional: keep only one section open at a time unless "Expand all" is active
  let expandedAll = false;
  items.forEach(d => d.addEventListener("toggle", () => {
    if (d.open && !expandedAll) items.forEach(o => { if (o !== d) o.open = false; });
  }));

  toggle.addEventListener("click", () => {
    expandedAll = !expandedAll;
    items.forEach(d => d.open = expandedAll);
    toggle.textContent = expandedAll ? "Collapse all" : "Expand all";
    toggle.setAttribute("aria-pressed", expandedAll);
  });
</script>
</body>
</html>
