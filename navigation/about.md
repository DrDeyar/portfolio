---
layout: post
title: About Deyar
permalink: /about/
comments: true
---

<style>
.deyar-about {
  --deyar-bg:#0b1018;
  --deyar-panel:#121a26;
  --deyar-panel-2:#172233;
  --deyar-border:rgba(255,255,255,.11);
  --deyar-text:#f6f8fc;
  --deyar-muted:#aab6c8;
  --deyar-blue:#61dafb;
  --deyar-purple:#a78bfa;
  --deyar-warm:#f8b45c;
  max-width:1080px;
  margin:0 auto;
  padding:8px 14px 44px;
  color:var(--deyar-text);
}
.deyar-about * { box-sizing:border-box; }
.deyar-about a { color:inherit; }
.deyar-hero {
  position:relative;
  display:grid;
  grid-template-columns:minmax(0,1.25fr) minmax(250px,.75fr);
  gap:34px;
  align-items:center;
  min-height:500px;
  padding:42px;
  overflow:hidden;
  border:1px solid var(--deyar-border);
  border-radius:28px;
  background:
    radial-gradient(circle at 12% 10%,rgba(97,218,251,.18),transparent 34%),
    radial-gradient(circle at 88% 88%,rgba(167,139,250,.18),transparent 35%),
    linear-gradient(145deg,#111a28,#0d131d);
}
.deyar-hero::before {
  content:"";
  position:absolute;
  width:260px;
  height:260px;
  right:-100px;
  top:-100px;
  border:1px solid rgba(97,218,251,.22);
  border-radius:50%;
}
.deyar-kicker {
  margin:0 0 14px;
  color:var(--deyar-blue);
  font-size:.76rem;
  font-weight:850;
  letter-spacing:.16em;
  text-transform:uppercase;
}
.deyar-hero h1 {
  max-width:650px;
  margin:0;
  font-size:clamp(2.55rem,6vw,4.8rem);
  line-height:.98;
  letter-spacing:-.05em;
}
.deyar-hero h1 span {
  color:transparent;
  background:linear-gradient(90deg,var(--deyar-blue),var(--deyar-purple));
  -webkit-background-clip:text;
  background-clip:text;
}
.deyar-hero-copy {
  max-width:650px;
  margin:22px 0 0;
  color:var(--deyar-muted);
  font-size:1.03rem;
  line-height:1.75;
}
.deyar-actions { display:flex; flex-wrap:wrap; gap:10px; margin-top:26px; }
.deyar-button,
.deyar-nav a {
  display:inline-flex;
  align-items:center;
  justify-content:center;
  min-height:42px;
  padding:8px 16px;
  border:1px solid var(--deyar-border);
  border-radius:999px;
  background:rgba(255,255,255,.045);
  text-decoration:none !important;
  font-weight:800;
  transition:transform .2s ease,border-color .2s ease,background .2s ease;
}
.deyar-button.primary {
  border-color:transparent;
  color:#071018;
  background:linear-gradient(90deg,var(--deyar-blue),#8de8ff);
}
.deyar-button:hover,
.deyar-nav a:hover {
  transform:translateY(-2px);
  border-color:var(--deyar-blue);
  background:rgba(97,218,251,.11);
}
.deyar-hero-photo {
  position:relative;
  z-index:1;
  max-width:300px;
  margin:0 auto;
  padding:8px;
  border:1px solid rgba(255,255,255,.16);
  border-radius:24px;
  background:rgba(255,255,255,.05);
  transform:rotate(2deg);
  box-shadow:0 24px 60px rgba(0,0,0,.38);
}
.deyar-hero-photo img {
  width:100%;
  aspect-ratio:4 / 5;
  object-fit:cover;
  object-position:center 45%;
  display:block;
  border-radius:17px;
}
.deyar-hero-photo span {
  display:block;
  padding:10px 6px 4px;
  color:var(--deyar-muted);
  font-size:.8rem;
  font-weight:750;
  text-align:center;
}
.deyar-nav {
  position:sticky;
  z-index:10;
  top:10px;
  display:flex;
  flex-wrap:wrap;
  gap:8px;
  margin:18px 0 42px;
  padding:10px;
  border:1px solid var(--deyar-border);
  border-radius:18px;
  background:rgba(11,16,24,.88);
  backdrop-filter:blur(16px);
}
.deyar-nav a { min-height:35px; padding:6px 13px; font-size:.78rem; }
.deyar-stats {
  display:grid;
  grid-template-columns:repeat(3,minmax(0,1fr));
  gap:14px;
  margin-bottom:48px;
}
.deyar-stat {
  padding:20px;
  border:1px solid var(--deyar-border);
  border-radius:18px;
  background:var(--deyar-panel);
}
.deyar-stat strong {
  display:block;
  color:var(--deyar-blue);
  font-size:1.75rem;
  line-height:1;
}
.deyar-stat span { display:block; margin-top:8px; color:var(--deyar-muted); font-size:.86rem; }
.deyar-section { margin-top:58px; scroll-margin-top:88px; }
.deyar-section-head { max-width:720px; margin:0 auto 24px; text-align:center; }
.deyar-section-head .deyar-kicker { margin-bottom:8px; }
.deyar-section-head h2 { margin:0; font-size:clamp(1.7rem,3.5vw,2.4rem); letter-spacing:-.025em; }
.deyar-section-head p { margin:12px 0 0; color:var(--deyar-muted); line-height:1.7; }
.deyar-interests {
  display:grid;
  grid-template-columns:repeat(6,minmax(0,1fr));
  gap:16px;
}
.deyar-interest {
  grid-column:span 2;
  overflow:hidden;
  border:1px solid var(--deyar-border);
  border-radius:20px;
  background:var(--deyar-panel);
  transition:transform .25s ease,box-shadow .25s ease,border-color .25s ease;
}
.deyar-interest:nth-child(4) { grid-column:2 / span 2; }
.deyar-interest:hover {
  transform:translateY(-5px);
  border-color:rgba(97,218,251,.45);
  box-shadow:0 18px 38px rgba(0,0,0,.28);
}
.deyar-interest img {
  width:100%;
  aspect-ratio:16 / 9;
  object-fit:cover;
  display:block;
}
.deyar-interest-copy { padding:17px 18px 20px; }
.deyar-interest h3 { margin:0 0 8px; font-size:1.12rem; }
.deyar-interest p { margin:0; color:var(--deyar-muted); line-height:1.6; font-size:.91rem; }
.deyar-story-grid {
  display:grid;
  grid-template-columns:repeat(2,minmax(0,1fr));
  gap:20px;
}
.deyar-story-card {
  overflow:hidden;
  border:1px solid var(--deyar-border);
  border-radius:22px;
  background:var(--deyar-panel);
  transition:transform .25s ease,border-color .25s ease;
}
.deyar-story-card:hover { transform:translateY(-4px); border-color:rgba(167,139,250,.45); }
.deyar-story-flag {
  display:grid;
  place-items:center;
  aspect-ratio:3 / 2;
  padding:0;
  background:#f3f5f8;
}
.deyar-story-flag img { width:100%; height:100%; object-fit:contain; display:block; }
.deyar-story-copy { padding:22px; }
.deyar-story-copy span {
  display:inline-block;
  margin-bottom:10px;
  padding:5px 9px;
  border:1px solid rgba(97,218,251,.28);
  border-radius:999px;
  color:var(--deyar-blue);
  background:rgba(97,218,251,.08);
  font-size:.7rem;
  font-weight:850;
  letter-spacing:.1em;
  text-transform:uppercase;
}
.deyar-story-copy h3 { margin:0 0 9px; font-size:1.35rem; }
.deyar-story-copy p { margin:0; color:var(--deyar-muted); line-height:1.7; }
.deyar-album {
  display:grid;
  grid-template-columns:repeat(4,minmax(0,1fr));
  gap:14px;
  max-width:920px;
  margin:0 auto;
}
.deyar-photo {
  position:relative;
  margin:0;
  overflow:hidden;
  border:1px solid var(--deyar-border);
  border-radius:16px;
  background:var(--deyar-panel);
  transition:transform .25s ease,box-shadow .25s ease;
}
.deyar-photo:hover { transform:translateY(-5px); box-shadow:0 18px 35px rgba(0,0,0,.3); }
.deyar-photo-media { position:relative; height:230px; overflow:hidden; background:#111925; }
.deyar-photo-media::after {
  content:"";
  position:absolute;
  inset:auto 0 0;
  height:18%;
  background:linear-gradient(transparent,var(--deyar-panel));
  pointer-events:none;
}
.deyar-photo img { width:100%; height:100%; object-fit:cover; display:block; }
.deyar-photo--portrait img { object-position:center 48%; }
.deyar-photo--world img { object-position:center bottom; }
.deyar-photo--landscape img { object-fit:contain; object-position:center; }
.deyar-photo--felfel img { object-position:center 52%; }
.deyar-photo figcaption {
  min-height:49px;
  padding:11px 10px 13px;
  color:var(--deyar-text);
  font-size:.83rem;
  font-weight:750;
  line-height:1.3;
  text-align:center;
}
.deyar-focus-grid {
  display:grid;
  grid-template-columns:1.05fr .95fr;
  gap:20px;
}
.deyar-focus-card {
  padding:clamp(22px,4vw,32px);
  border:1px solid var(--deyar-border);
  border-radius:22px;
  background:var(--deyar-panel);
}
.deyar-focus-card h3 { margin:0 0 12px; font-size:1.5rem; }
.deyar-focus-card > p { color:var(--deyar-muted); line-height:1.72; }
.deyar-steps { display:grid; gap:10px; margin-top:20px; }
.deyar-step {
  display:grid;
  grid-template-columns:38px 1fr;
  gap:12px;
  align-items:start;
  padding:13px;
  border:1px solid var(--deyar-border);
  border-radius:15px;
  background:rgba(255,255,255,.025);
}
.deyar-step b {
  display:grid;
  place-items:center;
  width:38px;
  height:38px;
  border-radius:50%;
  color:#081018;
  background:linear-gradient(145deg,var(--deyar-blue),var(--deyar-purple));
}
.deyar-step strong { display:block; margin:1px 0 3px; }
.deyar-step small { color:var(--deyar-muted); line-height:1.45; }
.deyar-timeline { margin:20px 0 0; padding:0; list-style:none; }
.deyar-timeline li {
  position:relative;
  margin-left:7px;
  padding:0 0 22px 28px;
  border-left:2px solid rgba(97,218,251,.35);
  color:var(--deyar-muted);
  line-height:1.6;
}
.deyar-timeline li:last-child { padding-bottom:0; }
.deyar-timeline li::before {
  content:"";
  position:absolute;
  top:5px;
  left:-7px;
  width:12px;
  height:12px;
  border:2px solid var(--deyar-panel);
  border-radius:50%;
  background:var(--deyar-purple);
  box-shadow:0 0 0 1px var(--deyar-border);
}
.deyar-timeline strong { color:var(--deyar-text); }
.deyar-tools { display:flex; flex-wrap:wrap; gap:8px; margin-top:18px; }
.deyar-tool {
  padding:6px 10px;
  border:1px solid var(--deyar-border);
  border-radius:999px;
  color:var(--deyar-muted);
  background:rgba(255,255,255,.03);
  font-size:.78rem;
  font-weight:700;
}
.deyar-goals { display:grid; grid-template-columns:repeat(3,minmax(0,1fr)); gap:16px; }
.deyar-goal {
  padding:22px;
  border:1px solid var(--deyar-border);
  border-radius:19px;
  background:linear-gradient(145deg,var(--deyar-panel),var(--deyar-panel-2));
}
.deyar-goal span { color:var(--deyar-purple); font-size:.72rem; font-weight:850; letter-spacing:.1em; text-transform:uppercase; }
.deyar-goal h3 { margin:9px 0 8px; font-size:1.12rem; }
.deyar-goal p { margin:0; color:var(--deyar-muted); line-height:1.62; font-size:.9rem; }
.deyar-footer-card {
  margin-top:58px;
  padding:28px;
  border:1px solid var(--deyar-border);
  border-radius:22px;
  background:linear-gradient(120deg,rgba(97,218,251,.11),rgba(167,139,250,.11));
  text-align:center;
}
.deyar-footer-card h2 { margin:0 0 8px; }
.deyar-footer-card p { max-width:620px; margin:0 auto 18px; color:var(--deyar-muted); line-height:1.65; }
@media (max-width:850px) {
  .deyar-hero { grid-template-columns:1fr; min-height:auto; padding:30px; }
  .deyar-hero-photo { max-width:250px; transform:none; }
  .deyar-interests { grid-template-columns:repeat(2,minmax(0,1fr)); }
  .deyar-interest,.deyar-interest:nth-child(4) { grid-column:auto; }
  .deyar-interest:last-child { grid-column:1 / -1; max-width:calc(50% - 8px); width:100%; justify-self:center; }
  .deyar-album { grid-template-columns:repeat(2,minmax(0,1fr)); max-width:560px; }
  .deyar-focus-grid { grid-template-columns:1fr; }
}
@media (max-width:620px) {
  .deyar-about { padding-inline:7px; }
  .deyar-hero { padding:24px 20px; border-radius:22px; }
  .deyar-hero h1 { font-size:2.55rem; }
  .deyar-nav { position:relative; top:auto; }
  .deyar-stats,.deyar-story-grid,.deyar-goals { grid-template-columns:1fr; }
  .deyar-interests { grid-template-columns:1fr; }
  .deyar-interest:last-child { grid-column:auto; max-width:none; }
  .deyar-photo-media { height:220px; }
}
@media (max-width:400px) {
  .deyar-album { grid-template-columns:1fr; max-width:270px; }
}
@media (prefers-reduced-motion:reduce) {
  .deyar-about * { scroll-behavior:auto !important; transition:none !important; }
}
</style>

<div class="deyar-about">
  <header class="deyar-hero" id="top">
    <div>
      <p class="deyar-kicker">Student · Creator · Problem Solver</p>
      <h1>Hey, I’m <span>Deyar.</span></h1>
      <p class="deyar-hero-copy">I’m a student learning computer science through hands-on projects, GitHub, and teamwork. I enjoy combining code with design, photography, writing, and creative ideas.</p>
      <div class="deyar-actions">
        <a class="deyar-button primary" href="#album">View my photo album</a>
        <a class="deyar-button" href="https://github.com/DrDeyar/portfolio">View my GitHub</a>
      </div>
    </div>
    <figure class="deyar-hero-photo">
      <img src="https://drdeyar.github.io/portfolio/assets/images/photo-album/yours-truly.jpg?v=5" alt="Creative portrait of Deyar">
      <span>A creative self-portrait</span>
    </figure>
  </header>

  <nav class="deyar-nav" aria-label="About page sections">
    <a href="#interests">Interests</a>
    <a href="#story">My story</a>
    <a href="#album">Photo album</a>
    <a href="#journey">CSP journey</a>
    <a href="#project">Team project</a>
    <a href="#goals">Goals</a>
  </nav>

  <div class="deyar-stats" aria-label="Quick facts">
    <div class="deyar-stat"><strong>7 years</strong><span>Lived in Iran</span></div>
    <div class="deyar-stat"><strong>5</strong><span>Creative interests</span></div>
    <div class="deyar-stat"><strong>1</strong><span>Team project in progress</span></div>
  </div>

  <section class="deyar-section" id="interests">
    <div class="deyar-section-head">
      <p class="deyar-kicker">What I enjoy</p>
      <h2>My Interests</h2>
      <p>Creativity and technology show up in different parts of my life.</p>
    </div>
    <div class="deyar-interests">
      <article class="deyar-interest">
        <img src="https://images.unsplash.com/photo-1498050108023-c5249f4df085?auto=format&fit=crop&w=900&q=82" alt="Computer displaying code" loading="lazy">
        <div class="deyar-interest-copy"><h3>💻 Coding</h3><p>Learning how software and websites work, then using that knowledge to build useful ideas.</p></div>
      </article>
      <article class="deyar-interest">
        <img src="https://images.unsplash.com/photo-1561070791-2526d30994b5?auto=format&fit=crop&w=900&q=82" alt="Creative design materials" loading="lazy">
        <div class="deyar-interest-copy"><h3>🎨 Design</h3><p>Making information clear, useful, and visually interesting.</p></div>
      </article>
      <article class="deyar-interest">
        <img src="https://images.unsplash.com/photo-1452780212940-6f5c0d14d848?auto=format&fit=crop&w=900&q=82" alt="Camera used for photography" loading="lazy">
        <div class="deyar-interest-copy"><h3>📷 Photography</h3><p>Using composition and light to capture a moment or tell a story.</p></div>
      </article>
      <article class="deyar-interest">
        <img src="https://images.unsplash.com/photo-1455390582262-044cdead277a?auto=format&fit=crop&w=900&q=82" alt="Notebook and pen" loading="lazy">
        <div class="deyar-interest-copy"><h3>✍️ Writing</h3><p>Turning ideas into organized explanations, reflections, and stories.</p></div>
      </article>
      <article class="deyar-interest">
        <img src="https://images.unsplash.com/photo-1542751371-adc38448a05e?auto=format&fit=crop&w=900&q=82" alt="Gaming setup" loading="lazy">
        <div class="deyar-interest-copy"><h3>🎮 Video Games</h3><p>Enjoying interactive challenges, competition, and creative worlds.</p></div>
      </article>
    </div>
  </section>

  <section class="deyar-section" id="story">
    <div class="deyar-section-head">
      <p class="deyar-kicker">Two places, one story</p>
      <h2>Places That Shaped Me</h2>
      <p>Iran and California are both important parts of my background.</p>
    </div>
    <div class="deyar-story-grid">
      <article class="deyar-story-card">
        <div class="deyar-story-flag"><img src="https://upload.wikimedia.org/wikipedia/commons/4/49/State_flag_of_Iran_1964-1980_%283-2%29.svg" alt="Historical Lion and Sun flag of Iran"></div>
        <div class="deyar-story-copy"><span>Seven years</span><h3>Life in Iran</h3><p>I lived in Iran for seven years before moving to California. Those years made Iran an important part of my background and personal story.</p></div>
      </article>
      <article class="deyar-story-card">
        <div class="deyar-story-flag"><img src="https://upload.wikimedia.org/wikipedia/commons/0/01/Flag_of_California.svg" alt="Flag of California"></div>
        <div class="deyar-story-copy"><span>My home now</span><h3>Life in California</h3><p>After living in Iran for seven years, I moved to California. California is where I live now, making it the other major place in my story.</p></div>
      </article>
    </div>
  </section>

  <section class="deyar-section" id="album">
    <div class="deyar-section-head">
      <p class="deyar-kicker">Snapshots</p>
      <h2>Photo Album</h2>
      <p>A few moments featuring me and my dog, Felfel.</p>
    </div>
    <div class="deyar-album">
      <figure class="deyar-photo deyar-photo--portrait"><div class="deyar-photo-media"><img src="https://drdeyar.github.io/portfolio/assets/images/photo-album/yours-truly.jpg?v=5" alt="Creative portrait of Deyar" loading="lazy"></div><figcaption>Yours truly</figcaption></figure>
      <figure class="deyar-photo deyar-photo--world"><div class="deyar-photo-media"><img src="https://drdeyar.github.io/portfolio/assets/images/photo-album/world-cup.jpg?v=5" alt="Deyar at the World Cup" loading="lazy"></div><figcaption>At the World Cup</figcaption></figure>
      <figure class="deyar-photo deyar-photo--landscape"><div class="deyar-photo-media"><img src="https://drdeyar.github.io/portfolio/assets/images/photo-album/felfel-portrait.jpg?v=5" alt="Felfel resting on a bed" loading="lazy"></div><figcaption>My Dog Felfel</figcaption></figure>
      <figure class="deyar-photo deyar-photo--felfel"><div class="deyar-photo-media"><img src="https://drdeyar.github.io/portfolio/assets/images/photo-album/felfel-weird-neck.jpg?v=5" alt="Felfel in an unusual resting position" loading="lazy"></div><figcaption>I Don't Know How She's Doing That</figcaption></figure>
    </div>
  </section>

  <section class="deyar-section" id="journey">
    <div class="deyar-section-head">
      <p class="deyar-kicker">Learning by building</p>
      <h2>My CSP Journey</h2>
      <p>This portfolio records my work, mistakes, fixes, reflections, and progress.</p>
    </div>
    <div class="deyar-focus-grid">
      <article class="deyar-focus-card">
        <h3>Building a dependable workflow</h3>
        <p>I am developing my skills with VS Code, Git, GitHub, Markdown, HTML, CSS, JavaScript, and GitHub Pages.</p>
        <div class="deyar-steps">
          <div class="deyar-step"><b>1</b><div><strong>Set up</strong><small>Prepare the development tools and local environment.</small></div></div>
          <div class="deyar-step"><b>2</b><div><strong>Build</strong><small>Create pages and improve them through focused changes.</small></div></div>
          <div class="deyar-step"><b>3</b><div><strong>Publish</strong><small>Use GitHub and Pages to share and verify the result.</small></div></div>
        </div>
        <div class="deyar-tools">
          <span class="deyar-tool">VS Code</span><span class="deyar-tool">Git</span><span class="deyar-tool">GitHub</span><span class="deyar-tool">HTML</span><span class="deyar-tool">CSS</span><span class="deyar-tool">JavaScript</span>
        </div>
      </article>
      <article class="deyar-focus-card">
        <h3>My learning timeline</h3>
        <ul class="deyar-timeline">
          <li><strong>Tools</strong><br>Set up the programs needed for development.</li>
          <li><strong>GitHub Pages</strong><br>Learn how repository changes become a published website.</li>
          <li><strong>Ground 0</strong><br>Build a repeatable workflow and document the evidence.</li>
          <li><strong>Next</strong><br>Apply those skills to a shared team product.</li>
        </ul>
        <div class="deyar-actions">
          <a class="deyar-button" href="https://pages.opencodingsociety.com/sprint1/challenge/csp/">Ground 0 challenge</a>
          <a class="deyar-button" href="https://github.com/DrDeyar/portfolio/issues/1">View my evidence</a>
        </div>
      </article>
    </div>
  </section>

  <section class="deyar-section" id="project">
    <div class="deyar-section-head">
      <p class="deyar-kicker">Current build direction</p>
      <h2>Tennis Equipment Recommender</h2>
      <p>My team’s idea turns player information into useful equipment suggestions.</p>
    </div>
    <article class="deyar-focus-card">
      <h3>How the idea works</h3>
      <p>A user would enter details such as experience level, playing style, comfort needs, and budget. The program would then suggest a suitable racquet, string setup, and grip.</p>
      <div class="deyar-steps">
        <div class="deyar-step"><b>1</b><div><strong>Learn about the player</strong><small>Collect experience, style, comfort, and budget information.</small></div></div>
        <div class="deyar-step"><b>2</b><div><strong>Compare choices</strong><small>Use clear recommendation rules to match the player with equipment.</small></div></div>
        <div class="deyar-step"><b>3</b><div><strong>Explain the result</strong><small>Show the suggested racquet, strings, and grip with understandable reasons.</small></div></div>
      </div>
    </article>
  </section>

  <section class="deyar-section" id="goals">
    <div class="deyar-section-head">
      <p class="deyar-kicker">What comes next</p>
      <h2>Growth Goals</h2>
      <p>The skills I want to keep improving as the course continues.</p>
    </div>
    <div class="deyar-goals">
      <article class="deyar-goal"><span>Development</span><h3>Strengthen my coding</h3><p>Keep improving JavaScript and become more confident building complete features.</p></article>
      <article class="deyar-goal"><span>Teamwork</span><h3>Work better with others</h3><p>Improve organization, communication, and how I contribute to a shared project.</p></article>
      <article class="deyar-goal"><span>Communication</span><h3>Explain my decisions</h3><p>Become more confident describing technical choices and what I learned from mistakes.</p></article>
    </div>
  </section>

  <div class="deyar-footer-card">
    <h2>Thanks for visiting.</h2>
    <p>This page will continue changing as I add projects, improve my skills, and build more work throughout the course.</p>
    <a class="deyar-button primary" href="{{ site.baseurl }}/">Return to the portfolio home page</a>
  </div>
</div>
