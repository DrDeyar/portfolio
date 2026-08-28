---
layout: post
title: About Me
permalink: /about/
comments: true
---

<style>
.about-page {
  --panel:#181818;
  --border:rgba(255,255,255,.10);
  --text:#f7f9fc;
  --muted:#afb7c4;
  --cyan:#70e6ff;
  --lime:#b8ff6a;
  max-width:1000px;
  margin:0 auto;
  padding:18px 15px 44px;
  color:var(--text);
}
.about-page * { box-sizing:border-box; }
.profile-hero {
  padding:12px 0 26px;
}
.profile-kicker {
  margin:0 0 12px;
  color:var(--cyan);
  font-size:.77rem;
  font-weight:850;
  letter-spacing:.14em;
  text-transform:uppercase;
}
.profile-hero h1 {
  max-width:780px;
  margin:0;
  font-size:clamp(2rem,4vw,2.75rem);
  line-height:1.12;
  letter-spacing:-.025em;
}
.profile-hero p:not(.profile-kicker) {
  max-width:720px;
  margin:20px 0 0;
  color:var(--muted);
  line-height:1.7;
}
.profile-actions,
.about-jump {
  display:flex;
  flex-wrap:wrap;
  gap:10px;
}
.profile-actions { margin-top:24px; }
.profile-link,
.jump-link {
  display:inline-flex;
  align-items:center;
  justify-content:center;
  min-height:40px;
  padding:7px 14px;
  border:1px solid var(--border);
  border-radius:999px;
  color:var(--text);
  background:rgba(255,255,255,.04);
  text-decoration:none !important;
  font-weight:800;
  transition:transform .2s ease,border-color .2s ease,background .2s ease;
}
.profile-link.primary {
  border-color:transparent;
  color:#081018;
  background:var(--lime);
}
.profile-link:hover,
.jump-link:hover {
  transform:translateY(-2px);
  border-color:var(--cyan);
  background:rgba(112,230,255,.10);
}
.about-jump {
  position:sticky;
  z-index:5;
  top:10px;
  margin:0 0 34px;
  padding:10px;
  border:1px solid var(--border);
  border-radius:18px;
  background:rgba(24,24,24,.92);
  backdrop-filter:blur(16px);
}
.jump-link { min-height:34px; font-size:.82rem; }
.about-section {
  margin-top:45px;
  scroll-margin-top:90px;
}
.about-section > h2 {
  margin:0 0 10px;
  font-size:1.85rem;
}
.about-section > p {
  max-width:800px;
  margin:0 0 20px;
  color:var(--muted);
  line-height:1.7;
}
.about-intro {
  padding:30px 38px;
  border:1px solid var(--border);
  border-radius:22px;
  background:var(--panel);
  text-align:center;
}
.about-intro h2 {
  margin:0 0 16px;
  font-size:1.8rem;
}
.about-intro p {
  max-width:760px;
  margin:10px auto;
  color:var(--muted);
  line-height:1.72;
}
.interest-grid {
  display:grid;
  grid-template-columns:repeat(2,minmax(0,1fr));
  gap:20px;
}
.interest-card {
  overflow:hidden;
  border:1px solid var(--border);
  border-radius:14px;
  background:var(--panel);
  transition:transform .25s ease,box-shadow .25s ease;
}
.interest-card:last-child {
  grid-column:1 / -1;
  width:calc(50% - 10px);
  justify-self:center;
}
.interest-card:hover {
  transform:translateY(-4px);
  box-shadow:0 12px 30px rgba(0,0,0,.30);
}
.interest-card img {
  width:100%;
  height:125px;
  object-fit:cover;
  display:block;
}
.interest-content { padding:17px 18px 19px; }
.interest-content h3 {
  margin:0 0 9px;
  padding-bottom:8px;
  border-bottom:1px solid rgba(255,255,255,.15);
  font-size:1.15rem;
}
.interest-content p {
  margin:0;
  color:var(--muted);
  line-height:1.6;
  font-size:.92rem;
}
.focus-grid {
  display:grid;
  grid-template-columns:1.1fr .9fr;
  gap:20px;
}
.focus-card,
.timeline-card {
  padding:28px;
  border:1px solid var(--border);
  border-radius:22px;
  background:var(--panel);
}
.focus-card h2,
.timeline-card h2 {
  margin:0 0 12px;
  font-size:1.65rem;
}
.focus-card > p,
.timeline-card li {
  color:var(--muted);
  line-height:1.68;
}
.build-steps {
  display:grid;
  gap:10px;
  margin-top:20px;
}
.build-step {
  display:grid;
  grid-template-columns:36px 1fr;
  gap:12px;
  padding:13px;
  border:1px solid var(--border);
  border-radius:15px;
  background:rgba(255,255,255,.025);
}
.build-step span {
  display:grid;
  place-items:center;
  width:36px;
  height:36px;
  border-radius:50%;
  color:#081018;
  background:var(--lime);
  font-weight:900;
}
.build-step strong { display:block; margin-bottom:3px; }
.build-step small { color:var(--muted); line-height:1.4; }
.timeline-list {
  position:relative;
  margin:20px 0 0;
  padding:0;
  list-style:none;
}
.timeline-list::before {
  content:"";
  position:absolute;
  top:8px;
  bottom:8px;
  left:7px;
  width:2px;
  background:var(--cyan);
}
.timeline-list li {
  position:relative;
  padding:0 0 20px 32px;
}
.timeline-list li:last-child { padding-bottom:0; }
.timeline-list li::before {
  content:"";
  position:absolute;
  top:7px;
  left:1px;
  width:14px;
  height:14px;
  border:3px solid var(--panel);
  border-radius:50%;
  background:var(--cyan);
  box-shadow:0 0 0 1px var(--border);
}
.timeline-list strong { color:var(--text); }
.workflow-grid,
.goal-grid {
  display:grid;
  gap:16px;
}
.workflow-grid { grid-template-columns:repeat(4,minmax(0,1fr)); }
.goal-grid { grid-template-columns:repeat(3,minmax(0,1fr)); }
.workflow-card,
.goal-card {
  padding:20px;
  border:1px solid var(--border);
  border-radius:18px;
  background:var(--panel);
}
.workflow-number,
.goal-status {
  color:var(--cyan);
  font-size:.74rem;
  font-weight:850;
  letter-spacing:.1em;
  text-transform:uppercase;
}
.workflow-card h3,
.goal-card h3 {
  margin:8px 0;
  font-size:1.05rem;
}
.workflow-card p,
.goal-card p {
  margin:0;
  color:var(--muted);
  line-height:1.6;
  font-size:.89rem;
}
.flag-grid {
  display:grid;
  grid-template-columns:repeat(2,minmax(0,1fr));
  gap:18px;
}
.flag-card {
  padding:18px;
  border:1px solid var(--border);
  border-radius:14px;
  background:var(--panel);
  text-align:center;
  transition:transform .25s ease,box-shadow .25s ease;
}
.flag-card:hover {
  transform:translateY(-4px);
  box-shadow:0 12px 30px rgba(0,0,0,.30);
}
.flag-card img {
  width:100%;
  height:110px;
  object-fit:contain;
  display:block;
  margin-bottom:13px;
  border-radius:6px;
  background:#f4f4f4;
}
.flag-card h3 { margin:0 0 7px; font-size:1.2rem; }
.flag-card p {
  max-width:410px;
  margin:0 auto;
  color:var(--muted);
  line-height:1.55;
  font-size:.9rem;
}
.album-grid {
  display:grid;
  grid-template-columns:repeat(4,minmax(0,1fr));
  gap:14px;
}
.album-card {
  margin:0;
  overflow:hidden;
  border:1px solid var(--border);
  border-radius:14px;
  background:var(--panel);
}
.album-card img {
  width:100%;
  height:140px;
  object-fit:cover;
  display:block;
}
.album-card.yours img { object-position:center 48%; }
.album-card.world img { object-position:center bottom; }
.album-card.dog-wide img { object-fit:contain; background:#111; }
.album-card.dog-neck img { object-position:center 52%; }
.album-card figcaption {
  min-height:46px;
  padding:10px 9px 12px;
  font-size:.8rem;
  font-weight:750;
  line-height:1.3;
  text-align:center;
}
.back-link {
  display:flex;
  justify-content:center;
  margin-top:48px;
}
@media (max-width:800px) {
  .focus-grid { grid-template-columns:1fr; }
  .workflow-grid { grid-template-columns:repeat(2,minmax(0,1fr)); }
  .album-grid { grid-template-columns:repeat(2,minmax(0,1fr)); max-width:560px; margin-inline:auto; }
}
@media (max-width:650px) {
  .about-intro { padding:24px 20px; }
  .interest-grid,
  .flag-grid,
  .goal-grid { grid-template-columns:1fr; }
  .interest-card:last-child { grid-column:auto; width:100%; }
  .about-jump { position:relative; top:auto; }
}
@media (max-width:430px) {
  .workflow-grid,
  .album-grid { grid-template-columns:1fr; }
  .album-grid { max-width:260px; }
}
@media (prefers-reduced-motion:reduce) {
  .about-page * { transition:none !important; }
}
</style>

<div class="about-page">
  <header class="profile-hero">
    <p class="profile-kicker">Student developer · AP CSP · California</p>
    <h1>Building skills through code, creativity, and teamwork.</h1>
    <p>I’m Deyar Raissadat. This page introduces my interests, background, current project, and progress in computer science.</p>
    <div class="profile-actions">
      <a class="profile-link primary" href="#current-focus">See what I’m building</a>
      <a class="profile-link" href="https://github.com/DrDeyar/portfolio">View source</a>
    </div>
  </header>

  <nav class="about-jump" aria-label="About page sections">
    <a class="jump-link" href="#story">Story</a>
    <a class="jump-link" href="#interests">Interests</a>
    <a class="jump-link" href="#current-focus">Current focus</a>
    <a class="jump-link" href="#workflow">Workflow</a>
    <a class="jump-link" href="#goals">Goals</a>
    <a class="jump-link" href="#places">Places</a>
    <a class="jump-link" href="#album">Photo album</a>
  </nav>

  <section class="about-intro" id="story">
    <h2>👋 About Me</h2>
    <p>I’m a student learning computer science through hands-on projects, GitHub, and teamwork.</p>
    <p>Outside of coding, I enjoy design, photography, writing, and video games.</p>
  </section>

  <section class="about-section" id="interests">
    <h2>Explore My Interests</h2>
    <p>These are the creative and technical areas I enjoy most.</p>
    <div class="interest-grid">
      <article class="interest-card"><img src="https://images.unsplash.com/photo-1498050108023-c5249f4df085?auto=format&fit=crop&w=900&q=82" alt="Computer displaying code" loading="lazy"><div class="interest-content"><h3>💻 Coding</h3><p>Learning how software and websites work and using those skills to build projects.</p></div></article>
      <article class="interest-card"><img src="https://images.unsplash.com/photo-1561070791-2526d30994b5?auto=format&fit=crop&w=900&q=82" alt="Creative design materials" loading="lazy"><div class="interest-content"><h3>🎨 Design</h3><p>Making ideas clear, useful, and visually interesting.</p></div></article>
      <article class="interest-card"><img src="https://images.unsplash.com/photo-1452780212940-6f5c0d14d848?auto=format&fit=crop&w=900&q=82" alt="Camera used for photography" loading="lazy"><div class="interest-content"><h3>📷 Photography</h3><p>Using composition and light to capture moments and tell stories.</p></div></article>
      <article class="interest-card"><img src="https://images.unsplash.com/photo-1455390582262-044cdead277a?auto=format&fit=crop&w=900&q=82" alt="Notebook and pen" loading="lazy"><div class="interest-content"><h3>✍️ Writing</h3><p>Turning ideas into organized explanations and stories.</p></div></article>
      <article class="interest-card"><img src="https://images.unsplash.com/photo-1542751371-adc38448a05e?auto=format&fit=crop&w=900&q=82" alt="Gaming setup" loading="lazy"><div class="interest-content"><h3>🎮 Video Games</h3><p>Enjoying interactive challenges, competition, and creative worlds.</p></div></article>
    </div>
  </section>

  <div class="focus-grid about-section" id="current-focus">
    <section class="focus-card">
      <p class="profile-kicker">Current build direction</p>
      <h2>Tennis equipment recommender</h2>
      <p>My team is planning a tool that uses experience level, playing style, comfort needs, and budget to suggest a racquet, string setup, and grip.</p>
      <div class="build-steps">
        <div class="build-step"><span>1</span><div><strong>Ask</strong><small>Collect the player’s needs and preferences.</small></div></div>
        <div class="build-step"><span>2</span><div><strong>Compare</strong><small>Match the answers with suitable equipment.</small></div></div>
        <div class="build-step"><span>3</span><div><strong>Recommend</strong><small>Explain the racquet, strings, and grip choices.</small></div></div>
      </div>
    </section>
    <section class="timeline-card">
      <p class="profile-kicker">Learning timeline</p>
      <h2>From setup to team software</h2>
      <ul class="timeline-list">
        <li><strong>Tools</strong><br>Prepared the programs needed for development.</li>
        <li><strong>GitHub Pages</strong><br>Learned how repository changes become a website.</li>
        <li><strong>Ground 0</strong><br>Built a repeatable workflow and documented evidence.</li>
        <li><strong>Next</strong><br>Apply those skills to the team project.</li>
      </ul>
    </section>
  </div>

  <section class="about-section" id="workflow">
    <h2>How I Build</h2>
    <p>A simple process helps me keep changes understandable and testable.</p>
    <div class="workflow-grid">
      <article class="workflow-card"><span class="workflow-number">01 · Plan</span><h3>Define the goal</h3><p>Decide what the page or feature needs to accomplish.</p></article>
      <article class="workflow-card"><span class="workflow-number">02 · Build</span><h3>Create in steps</h3><p>Use focused changes instead of changing everything at once.</p></article>
      <article class="workflow-card"><span class="workflow-number">03 · Debug</span><h3>Find the cause</h3><p>Compare what should happen with what actually happens.</p></article>
      <article class="workflow-card"><span class="workflow-number">04 · Verify</span><h3>Check the result</h3><p>Review the live page and make sure the change works.</p></article>
    </div>
  </section>

  <section class="about-section" id="goals">
    <h2>What I’m Working Toward</h2>
    <p>Three areas I want to keep improving during the course.</p>
    <div class="goal-grid">
      <article class="goal-card"><span class="goal-status">Coding</span><h3>Build stronger features</h3><p>Improve my JavaScript and become more confident creating complete projects.</p></article>
      <article class="goal-card"><span class="goal-status">Teamwork</span><h3>Contribute clearly</h3><p>Stay organized, communicate progress, and work well in a shared project.</p></article>
      <article class="goal-card"><span class="goal-status">Explanation</span><h3>Show my reasoning</h3><p>Explain technical choices and what I learned from mistakes.</p></article>
    </div>
  </section>

  <section class="about-section" id="places">
    <h2>Places That Shaped Me</h2>
    <p>I lived in Iran for seven years before moving to California.</p>
    <div class="flag-grid">
      <article class="flag-card"><img src="https://upload.wikimedia.org/wikipedia/commons/4/49/State_flag_of_Iran_1964-1980_%283-2%29.svg" alt="Historical Lion and Sun flag of Iran"><h3>Iran</h3><p>I lived in Iran for seven years. Those years made it an important part of my background.</p></article>
      <article class="flag-card"><img src="https://upload.wikimedia.org/wikipedia/commons/0/01/Flag_of_California.svg" alt="Flag of California"><h3>California</h3><p>After seven years in Iran, I moved to California, which is where I live now.</p></article>
    </div>
  </section>

  <section class="about-section" id="album">
    <h2>Photo Album</h2>
    <p>Four personal photos with short captions.</p>
    <div class="album-grid">
      <figure class="album-card yours"><img src="https://drdeyar.github.io/portfolio/assets/images/photo-album/yours-truly.jpg?v=6" alt="Creative portrait of Deyar" loading="lazy"><figcaption>Yours Truly</figcaption></figure>
      <figure class="album-card world"><img src="https://drdeyar.github.io/portfolio/assets/images/photo-album/world-cup.jpg?v=6" alt="Deyar at the World Cup" loading="lazy"><figcaption>At The World Cup</figcaption></figure>
      <figure class="album-card dog-wide"><img src="https://drdeyar.github.io/portfolio/assets/images/photo-album/felfel-portrait.jpg?v=6" alt="Felfel resting on a bed" loading="lazy"><figcaption>My Dog Felfel</figcaption></figure>
      <figure class="album-card dog-neck"><img src="https://drdeyar.github.io/portfolio/assets/images/photo-album/felfel-weird-neck.jpg?v=6" alt="Felfel in an unusual position" loading="lazy"><figcaption>I Don't Know How She's Doing That</figcaption></figure>
    </div>
  </section>

  <div class="back-link">
    <a class="profile-link primary" href="{{ site.baseurl }}/">Return to the home page</a>
  </div>
</div>
