<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<!--💡UPDATE: page title and description (shown in Google results and when you share the link) -->
<title>Mohamed Abdikadir | Data Analyst Portfolio</title>
<meta name="description" content="Mohamed Abdikadir is a data analyst and the founder of SMART Institute of Technology & Innovation (SITI). Dashboards, data analysis and AI training, based in Nairobi, Kenya.">
<meta property="og:title" content="Mohamed Abdikadir | Data Analyst Portfolio">
<meta property="og:description" content="Dashboards, data analysis and AI training.">
<meta name="theme-color" content="#0A2533">
<!--💡UPDATE: replace this emoji favicon with your own file (e.g. favicon.ico in the root folder) -->
<link rel="icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='.9em' font-size='90'>📊</text></svg>">

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,500;12..96,700;12..96,800&family=Figtree:wght@400;500;600&display=swap" rel="stylesheet">

<style>
  :root {
    --bg: #0A2533;
    --panel: #103548;
    --panel-2: #0D2D3F;
    --line: rgba(234, 242, 244, 0.14);
    --text: #EAF2F4;
    --muted: #9DB6BF;
    --accent: #5FD3B8;
    --accent-ink: #062A22;
    --sun: #F4B13E;
    --radius: 14px;
    --display: "Bricolage Grotesque", "Segoe UI", system-ui, sans-serif;
    --body: "Figtree", "Segoe UI", system-ui, sans-serif;
    color-scheme: dark;
  }
  :root[data-theme="light"] {
    --bg: #F2F7F8;
    --panel: #FFFFFF;
    --panel-2: #E8F0F2;
    --line: rgba(10, 37, 51, 0.16);
    --text: #0A2533;
    --muted: #46616C;
    --accent: #0C7D68;
    --accent-ink: #FFFFFF;
    --sun: #B86F00;
    color-scheme: light;
  }

  * { box-sizing: border-box; }
  html { scroll-behavior: smooth; scroll-padding-top: 76px; }
  body {
    margin: 0;
    background: var(--bg);
    color: var(--text);
    font: 400 1.0625rem/1.65 var(--body);
    -webkit-font-smoothing: antialiased;
  }
  img { max-width: 100%; display: block; }
  a { color: inherit; }
  :focus-visible { outline: 3px solid var(--sun); outline-offset: 3px; border-radius: 6px; }

  .wrap { width: min(1120px, 100% - 2.5rem); margin-inline: auto; }
  section { padding: 5.5rem 0; }
  h1, h2, h3 { font-family: var(--display); line-height: 1.1; margin: 0; letter-spacing: -0.02em; }
  h2 { font-size: clamp(1.9rem, 4vw, 2.6rem); font-weight: 800; margin-bottom: 2rem; }
  h3 { font-size: 1.35rem; font-weight: 700; }
  p { margin: 0 0 1rem; }
  .muted { color: var(--muted); }

  /* Navigation */
  .nav {
    position: sticky; top: 0; z-index: 10;
    background: color-mix(in srgb, var(--bg) 88%, transparent);
    backdrop-filter: blur(10px);
    border-bottom: 1px solid var(--line);
  }
  .nav .wrap { display: flex; align-items: center; justify-content: space-between; height: 64px; }
  .brand { font: 800 1.25rem var(--display); text-decoration: none; letter-spacing: -0.02em; }
  .nav ul { display: flex; gap: 1.6rem; list-style: none; margin: 0; padding: 0; align-items: center; }
  .nav a.link { text-decoration: none; color: var(--muted); font-weight: 500; transition: color .2s; }
  .nav a.link:hover { color: var(--text); }
  .theme-btn {
    background: transparent; color: var(--text); border: 1px solid var(--line);
    border-radius: 999px; padding: .35rem .85rem; font: 500 .9rem var(--body); cursor: pointer;
  }
  .theme-btn:hover { border-color: var(--accent); }

  /* Buttons */
  .btn {
    display: inline-flex; align-items: center; gap: .5rem;
    padding: .8rem 1.35rem; border-radius: 999px; font-weight: 600; text-decoration: none;
    border: 1.5px solid var(--line); transition: transform .15s, border-color .2s, background .2s;
  }
  .btn:hover { transform: translateY(-2px); border-color: var(--accent); }
  .btn.primary { background: var(--accent); color: var(--accent-ink); border-color: var(--accent); }
  .btn.primary:hover { filter: brightness(1.08); }

  /* Hero */
  .hero { padding: 4.5rem 0 5rem; }
  .hero .wrap { display: grid; grid-template-columns: 1.05fr 1fr; gap: 3.5rem; align-items: center; }
  .hero h1 { font-size: clamp(2.5rem, 6vw, 4.4rem); font-weight: 800; margin-bottom: 1.25rem; }
  .hero .lead { font-size: 1.2rem; color: var(--muted); max-width: 34rem; }
  .hero .actions { display: flex; flex-wrap: wrap; gap: .8rem; margin-top: 1.8rem; }
  .hero .place { margin-top: 1.6rem; font-size: .98rem; color: var(--muted); }

  /* Hero chart: the one memorable element */
  .chart-card {
    background: var(--panel); border: 1px solid var(--line); border-radius: 22px;
    padding: 1.5rem 1.5rem 1.2rem;
    box-shadow: 0 30px 60px -30px rgba(0, 0, 0, .55);
  }
  .chart-head { display: flex; justify-content: space-between; align-items: center; gap: 1rem; flex-wrap: wrap; margin-bottom: 1.2rem; }
  .chart-head strong { font: 700 1.05rem var(--display); }
  .seg { display: inline-flex; border: 1px solid var(--line); border-radius: 999px; padding: 3px; background: var(--panel-2); }
  .seg button {
    border: 0; background: transparent; color: var(--muted); padding: .3rem .85rem;
    border-radius: 999px; font: 600 .88rem var(--body); cursor: pointer;
  }
  .seg button[aria-pressed="true"] { background: var(--accent); color: var(--accent-ink); }
  .bars { display: grid; grid-template-columns: repeat(6, 1fr); gap: .7rem; height: 220px; align-items: end; border-bottom: 1px solid var(--line); padding-bottom: 0; }
  .col { height: 100%; display: flex; flex-direction: column; justify-content: flex-end; align-items: center; gap: .35rem; }
  .col .val { font: 600 .85rem var(--body); }
  .col .bar {
    width: 100%; border-radius: 8px 8px 0 0; background: var(--accent);
    height: 0; transition: height .7s cubic-bezier(.2, .8, .2, 1), background .2s;
    transition-delay: calc(var(--i) * 70ms);
  }
  .col.top .bar { background: var(--sun); }
  .col.low .bar { background: color-mix(in srgb, var(--muted) 70%, var(--bg)); }
  .labels { display: grid; grid-template-columns: repeat(6, 1fr); gap: .7rem; margin-top: .5rem; text-align: center; font-size: .82rem; color: var(--muted); }
  .chart-note { margin: 1rem 0 0; font-size: .92rem; min-height: 3em; }
  .chart-note small { color: var(--muted); display: block; margin-top: .25rem; }

  /* About */
  .about .wrap { display: grid; grid-template-columns: 300px 1fr; gap: 3.5rem; align-items: start; }
  .photo {
    position: relative; aspect-ratio: 4 / 5; border-radius: 22px; overflow: hidden;
    background: linear-gradient(160deg, var(--panel), var(--panel-2)); border: 1px solid var(--line);
    display: grid; place-items: center;
  }
  .photo span { font: 800 4.5rem var(--display); color: var(--accent); }
  .photo img { position: absolute; inset: 0; width: 100%; height: 100%; object-fit: cover; }
  .facts { margin: 1.6rem 0 0; display: grid; grid-template-columns: 9rem 1fr; gap: .7rem 1rem; padding-top: 1.4rem; border-top: 1px solid var(--line); }
  .facts dt { color: var(--muted); }
  .facts dd { margin: 0; font-weight: 500; }

  /* Projects */
  .projects-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 1.4rem; }
  .project {
    background: var(--panel); border: 1px solid var(--line); border-radius: var(--radius);
    padding: 1.8rem; display: flex; flex-direction: column; gap: 1rem;
    transition: border-color .2s, transform .2s;
  }
  .project:hover { border-color: var(--accent); transform: translateY(-3px); }
  .project.featured { grid-column: 1 / -1; display: grid; grid-template-columns: 1.1fr 1fr; gap: 2rem; padding: 2.2rem; }
  .project.featured h3 { font-size: 1.8rem; }
  .tags { display: flex; flex-wrap: wrap; gap: .45rem; padding: 0; margin: 0; list-style: none; }
  .tags li { border: 1px solid var(--line); border-radius: 999px; padding: .15rem .7rem; font-size: .85rem; color: var(--muted); }
  .project .more { margin-top: auto; font-weight: 600; color: var(--accent); text-decoration: none; }
  .project .more:hover { text-decoration: underline; text-underline-offset: 4px; }
  .findings { margin: 0; padding: 0; list-style: none; display: grid; gap: .7rem; align-content: center; background: var(--panel-2); border-radius: 12px; padding: 1.3rem; }
  .findings li { padding-left: 1.2rem; position: relative; }
  .findings li::before { content: ""; position: absolute; left: 0; top: .72em; width: .5rem; height: .5rem; border-radius: 2px; background: var(--sun); }

  /* Skills */
  .skills-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.4rem; }
  .skill-group { background: var(--panel); border: 1px solid var(--line); border-radius: var(--radius); padding: 1.6rem; }
  .skill-group h3 { margin-bottom: 1.1rem; font-size: 1.15rem; }
  .skill { display: flex; justify-content: space-between; align-items: center; gap: 1rem; padding: .5rem 0; border-top: 1px solid var(--line); }
  .skill:first-of-type { border-top: 0; }
  .meter { display: inline-flex; gap: 4px; }
  .meter i { width: 18px; height: 6px; border-radius: 3px; background: var(--line); }
  .meter i.on { background: var(--accent); }
  .level { color: var(--muted); font-size: .85rem; min-width: 5.2rem; text-align: right; }
  .skill-right { display: inline-flex; align-items: center; gap: .8rem; }

  /* Contact */
  .contact { padding-bottom: 4rem; }
  .contact-card {
    background: linear-gradient(135deg, var(--panel), var(--panel-2));
    border: 1px solid var(--line); border-radius: 26px; padding: clamp(2rem, 5vw, 3.8rem);
  }
  .contact-card h2 { margin-bottom: 1rem; max-width: 18ch; }
  .contact-card .actions { display: flex; flex-wrap: wrap; gap: .8rem; margin-top: 1.8rem; }

  footer { border-top: 1px solid var(--line); padding: 1.8rem 0 2.5rem; color: var(--muted); font-size: .95rem; }
  footer .wrap { display: flex; justify-content: space-between; flex-wrap: wrap; gap: .5rem; }

  /* Responsive */
  @media (max-width: 880px) {
    .hero .wrap, .about .wrap, .project.featured { grid-template-columns: 1fr; }
    .about .wrap { gap: 2rem; }
    .photo { max-width: 260px; }
    .projects-grid, .skills-grid { grid-template-columns: 1fr; }
    .nav ul li.hide-sm { display: none; }
    section { padding: 4rem 0; }
  }
  @media (max-width: 520px) {
    .facts { grid-template-columns: 1fr; gap: .1rem; }
    .facts dd { margin-bottom: .8rem; }
  }
  @media (prefers-reduced-motion: reduce) {
    html { scroll-behavior: auto; }
    * { transition: none !important; }
  }
</style>
</head>

<body>

<header class="nav">
  <div class="wrap">
    <!--💡UPDATE: your name -->
    <a class="brand" href="#top">Mohamed Abdikadir</a>
    <ul>
      <li class="hide-sm"><a class="link" href="#about">About</a></li>
      <li class="hide-sm"><a class="link" href="#projects">Projects</a></li>
      <li class="hide-sm"><a class="link" href="#skills">Skills</a></li>
      <li class="hide-sm"><a class="link" href="#contact">Contact</a></li>
      <li><button class="theme-btn" id="themeBtn" type="button" aria-label="Switch between light and dark theme">Light mode</button></li>
    </ul>
  </div>
</header>

<main id="top">

  <!-- HERO -->
  <section class="hero">
    <div class="wrap">
      <div>
        <!--💡UPDATE: your headline and intro -->
        <h1>I turn messy data into dashboards people actually use.</h1>
        <p class="lead">I'm Mohamed Abdikadir, a data analyst and the founder of SMART Institute of Technology &amp; Innovation (SITI). I build clear reports, automate repetitive work, and teach teams how to use data and AI.</p>
        <div class="actions">
          <a class="btn primary" href="#projects">View projects</a>
          <!--💡UPDATE: put your CV in the assets/ folder and match the file name -->
          <a class="btn" href="assets/Mohamed-Abdikadir-CV.pdf" download>Download CV</a>
        </div>
        <p class="place">Based in Nairobi, Kenya. Available for remote and on-site work.</p>
      </div>

      <div class="chart-card" aria-labelledby="chartTitle">
        <div class="chart-head">
          <strong id="chartTitle">Average score by school</strong>
          <div class="seg" role="group" aria-label="Filter by student group">
            <button type="button" data-mode="both" aria-pressed="true">All</button>
            <button type="button" data-mode="boys" aria-pressed="false">Boys</button>
            <button type="button" data-mode="girls" aria-pressed="false">Girls</button>
          </div>
        </div>
        <div class="bars" id="bars" role="img" aria-label="Bar chart of sample average scores for six schools"></div>
        <div class="labels" id="labels"></div>
        <p class="chart-note" id="chartNote" aria-live="polite"></p>
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section class="about" id="about">
    <div class="wrap">
      <figure class="photo" style="margin:0">
        <span aria-hidden="true">MA</span>
        <!--💡UPDATE: add your photo as assets/images/profile.jpg (portrait works best). Until then, your initials show. -->
        <img src="assets/images/profile.jpg" alt="Portrait of Mohamed Abdikadir" onerror="this.remove()">
      </figure>
      <div>
        <h2>About me</h2>
        <!--💡UPDATE: rewrite this in your own voice -->
        <p>I'm a data analyst who enjoys the moment a messy spreadsheet turns into a clear answer. My work centres on dashboards that get used, models that help teams plan, and automation that frees people for more interesting problems.</p>
        <p>As CEO and founder of SITI, I also design professional AI and Prompt Engineering courses, so I know how to explain technical ideas in plain language. I bring the same approach to every client report.</p>
        <dl class="facts">
          <dt>Role</dt><dd>Data analyst, CEO and founder at SITI</dd>
          <dt>Education</dt><dd>Computer science background; associated with Daha International University, Kismayo</dd>
          <dt>Business</dt><dd>Mo-Sheikh Farms, livestock and agriculture</dd>
          <dt>Location</dt><dd>Nairobi, Kenya</dd>
        </dl>
      </div>
    </div>
  </section>

  <!-- PROJECTS -->
  <section id="projects">
    <div class="wrap">
      <h2>Projects</h2>
      <div class="projects-grid">

        <!--💡UPDATE: project 1 (featured). Change the title, text, tags, findings and link -->
        <article class="project featured">
          <div style="display:flex;flex-direction:column;gap:1rem">
            <h3>Jubbaland Grade 8 Results Dashboard</h3>
            <p class="muted" style="margin:0">An Excel dashboard that turns Grade 8 exam results into one clear view for the State of Somalia's schools, so decision makers can see who is doing well and who needs support.</p>
            <ul class="tags"><li>Excel</li><li>Dashboard design</li><li>Education data</li></ul>
            <!--💡UPDATE: link to your repository, file or demo -->
            <a class="more" href="https://github.com/TODO-your-username/TODO-repository">View project</a>
          </div>
          <ul class="findings" aria-label="What the dashboard shows">
            <li>Compares 12 schools across 9 subjects</li>
            <li>Splits results for boys and girls</li>
            <li>Highlights the highest and lowest performing school</li>
            <li>Counts failing students per school and subject</li>
          </ul>
        </article>

        <!--💡UPDATE: project 2 -->
        <article class="project">
          <h3>AI and Prompt Engineering Course</h3>
          <p class="muted" style="margin:0">A structured, module-based professional course for SITI, with a consistent slide framework so every lesson is easy to teach and easy to follow.</p>
          <ul class="tags"><li>Curriculum design</li><li>Prompt Engineering</li><li>Training slides</li></ul>
          <a class="more" href="https://github.com/TODO-your-username/TODO-repository">View project</a>
        </article>

        <!--💡UPDATE: project 3 (replace the text in brackets with your SQL, Python or Power BI project) -->
        <article class="project">
          <h3>[Your next project title]</h3>
          <p class="muted" style="margin:0">[One or two sentences: the problem, the tools you used, and the result it produced.]</p>
          <ul class="tags"><li>SQL</li><li>Power BI</li><li>Python</li></ul>
          <a class="more" href="https://github.com/TODO-your-username/TODO-repository">View project</a>
        </article>

      </div>
    </div>
  </section>

  <!-- SKILLS -->
  <section id="skills">
    <div class="wrap">
      <h2>Skills</h2>
      <!--💡UPDATE: change skill names and levels. Each meter has 5 bars: class="on" fills one. -->
      <div class="skills-grid">

        <div class="skill-group">
          <h3>Data visualization</h3>
          <div class="skill"><span>Excel dashboards</span><span class="skill-right"><span class="meter" aria-hidden="true"><i class="on"></i><i class="on"></i><i class="on"></i><i class="on"></i><i class="on"></i></span><span class="level">Expert</span></span></div>
          <div class="skill"><span>Power BI</span><span class="skill-right"><span class="meter" aria-hidden="true"><i class="on"></i><i class="on"></i><i class="on"></i><i class="on"></i><i class="on"></i></span><span class="level">Expert</span></span></div>
          <div class="skill"><span>Data storytelling</span><span class="skill-right"><span class="meter" aria-hidden="true"><i class="on"></i><i class="on"></i><i class="on"></i><i class="on"></i><i class="on"></i></span><span class="level">Expert</span></span></div>
        </div>

        <div class="skill-group">
          <h3>Data analysis</h3>
          <div class="skill"><span>SQL</span><span class="skill-right"><span class="meter" aria-hidden="true"><i class="on"></i><i class="on"></i><i class="on"></i><i class="on"></i><i class="on"></i></span><span class="level">Expert</span></span></div>
          <div class="skill"><span>Python (Pandas)</span><span class="skill-right"><span class="meter" aria-hidden="true"><i class="on"></i><i class="on"></i><i class="on"></i><i class="on"></i><i></i></span><span class="level">Advanced</span></span></div>
          <div class="skill"><span>Statistical analysis</span><span class="skill-right"><span class="meter" aria-hidden="true"><i class="on"></i><i class="on"></i><i class="on"></i><i class="on"></i><i class="on"></i></span><span class="level">Expert</span></span></div>
        </div>

        <div class="skill-group">
          <h3>Modeling and training</h3>
          <div class="skill"><span>Power Query and DAX</span><span class="skill-right"><span class="meter" aria-hidden="true"><i class="on"></i><i class="on"></i><i class="on"></i><i class="on"></i><i class="on"></i></span><span class="level">Expert</span></span></div>
          <div class="skill"><span>KPI development</span><span class="skill-right"><span class="meter" aria-hidden="true"><i class="on"></i><i class="on"></i><i class="on"></i><i class="on"></i><i class="on"></i></span><span class="level">Expert</span></span></div>
          <div class="skill"><span>Prompt Engineering</span><span class="skill-right"><span class="meter" aria-hidden="true"><i class="on"></i><i class="on"></i><i class="on"></i><i class="on"></i><i class="on"></i></span><span class="level">Expert</span></span></div>
        </div>

      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section class="contact" id="contact">
    <div class="wrap">
      <div class="contact-card">
        <h2>Have data that needs a clear story?</h2>
        <p class="muted" style="max-width:36rem">Send me a message about your project, report or training need. I'll reply with how I can help.</p>
        <div class="actions">
          <!--💡UPDATE: your email and social links -->
          <a class="btn primary" href="mailto:Mohedabdikadir57@gmail.com">Email me</a>
          <a class="btn" href="https://linkedin.com/in/mohamed-abdikadir-282a3830a" target="_blank" rel="noopener">LinkedIn</a>
          <a class="btn" href="https://github.com/TODO-your-username" target="_blank" rel="noopener">GitHub</a>
        </div>
      </div>
    </div>
  </section>

</main>

<footer>
  <div class="wrap">
    <span>&copy; <span id="year"></span> Mohamed Abdikadir</span>
    <span>Nairobi, Kenya</span>
  </div>
</footer>

<script>
  /* Theme toggle (dark by default, remembers the choice) */
  (function () {
    var root = document.documentElement;
    var btn = document.getElementById('themeBtn');
    var saved = null;
    try { saved = localStorage.getItem('theme'); } catch (e) {}
    if (!saved && window.matchMedia && window.matchMedia('(prefers-color-scheme: light)').matches) saved = 'light';
    function apply(t) {
      if (t === 'light') root.setAttribute('data-theme', 'light'); else root.removeAttribute('data-theme');
      btn.textContent = t === 'light' ? 'Dark mode' : 'Light mode';
    }
    apply(saved);
    btn.addEventListener('click', function () {
      var next = root.getAttribute('data-theme') === 'light' ? 'dark' : 'light';
      apply(next);
      try { localStorage.setItem('theme', next); } catch (e) {}
    });
  })();

  /* Hero chart: illustrative sample data only */
  (function () {
    var schools = [
      { n: 'School A', b: 61, g: 66 },
      { n: 'School B', b: 72, g: 77 },
      { n: 'School C', b: 55, g: 52 },
      { n: 'School D', b: 80, g: 84 },
      { n: 'School E', b: 67, g: 70 },
      { n: 'School F', b: 48, g: 51 }
    ];
    var bars = document.getElementById('bars');
    var labels = document.getElementById('labels');
    var note = document.getElementById('chartNote');
    var buttons = document.querySelectorAll('.seg button');
    var cols = [];

    schools.forEach(function (s, i) {
      var col = document.createElement('div');
      col.className = 'col';
      col.style.setProperty('--i', i);
      col.innerHTML = '<span class="val"></span><div class="bar"></div>';
      bars.appendChild(col);
      cols.push(col);
      var l = document.createElement('span');
      l.textContent = s.n.replace('School ', 'Sch. ');
      labels.appendChild(l);
    });

    function score(s, mode) {
      if (mode === 'boys') return s.b;
      if (mode === 'girls') return s.g;
      return Math.round((s.b + s.g) / 2);
    }

    function render(mode) {
      var vals = schools.map(function (s) { return score(s, mode); });
      var max = Math.max.apply(null, vals), min = Math.min.apply(null, vals);
      cols.forEach(function (col, i) {
        col.classList.toggle('top', vals[i] === max);
        col.classList.toggle('low', vals[i] === min);
        col.querySelector('.val').textContent = vals[i];
        col.querySelector('.bar').style.height = vals[i] + '%';
      });
      var hi = schools[vals.indexOf(max)].n, lo = schools[vals.indexOf(min)].n;
      var who = mode === 'both' ? 'all students' : mode;
      note.innerHTML = 'Highest for ' + who + ': <strong>' + hi + '</strong> (' + max + '). Lowest: <strong>' + lo + '</strong> (' + min + ').' +
        '<small>Illustrative sample data, not real results.</small>';
    }

    buttons.forEach(function (b) {
      b.addEventListener('click', function () {
        buttons.forEach(function (x) { x.setAttribute('aria-pressed', 'false'); });
        b.setAttribute('aria-pressed', 'true');
        render(b.getAttribute('data-mode'));
      });
    });

    /* Single page-load moment: bars grow in */
    requestAnimationFrame(function () { requestAnimationFrame(function () { render('both'); }); });
  })();

  document.getElementById('year').textContent = new Date().getFullYear();
</script>
</body>
</html>
