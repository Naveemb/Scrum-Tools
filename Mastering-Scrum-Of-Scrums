<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Scrum of Scrums – Senior SM Interview Guide</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet"/>
<style>
  :root {
    --navy:   #0F1F3D;
    --blue:   #1A4FBE;
    --cyan:   #00C2FF;
    --green:  #00D68F;
    --amber:  #FFB020;
    --red:    #FF4D6D;
    --purple: #7B5EA7;
    --bg:     #F4F7FF;
    --card:   #FFFFFF;
    --text:   #1A1A2E;
    --muted:  #6B7A99;
    --border: #E0E8F5;
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body {
    font-family: 'Inter', sans-serif; background: var(--bg); color: var(--text);
    -webkit-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
  }

  /* ── NAV ── */
  nav {
    background: var(--navy);
    padding: 0 32px;
    display: flex;
    align-items: center;
    gap: 4px;
    position: sticky;
    top: 0;
    z-index: 100;
    box-shadow: 0 2px 16px rgba(0,0,0,.25);
    flex-wrap: wrap;
  }
  nav .logo {
    font-family: 'Syne', sans-serif;
    font-weight: 800;
    font-size: 15px;
    color: var(--cyan);
    padding: 14px 0;
    margin-right: 16px;
    white-space: nowrap;
  }
  nav button {
    background: none; border: none; cursor: pointer;
    font-family: 'Inter', sans-serif; font-size: 12px; font-weight: 500;
    color: #8899BB; padding: 14px 10px; transition: color .2s;
    white-space: nowrap;
  }
  nav button:hover { color: #fff; }
  nav button.active { color: var(--cyan); border-bottom: 2px solid var(--cyan); }

  /* ── HERO ── */
  .hero {
    background: linear-gradient(135deg, var(--navy) 0%, #1A2E5C 100%);
    padding: 52px 40px 44px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }
  .hero::before {
    content:'';
    position: absolute; inset: 0;
    background: radial-gradient(ellipse at 70% 50%, rgba(0,194,255,.08) 0%, transparent 70%);
  }
  .hero .badge {
    display: inline-block;
    background: rgba(0,214,143,.15);
    border: 1px solid rgba(0,214,143,.35);
    color: var(--green);
    font-size: 11px; font-weight: 600; letter-spacing: .08em;
    padding: 4px 12px; border-radius: 20px; margin-bottom: 16px;
  }
  .hero h1 {
    font-family: 'Syne', sans-serif; font-weight: 800;
    font-size: clamp(26px, 4vw, 42px); color: #fff;
    line-height: 1.15; margin-bottom: 12px;
  }
  .hero h1 span { color: var(--cyan); }
  .hero p { color: #8899BB; font-size: 15px; max-width: 580px; margin: 0 auto; }

  /* ── LAYOUT ── */
  .page { display: none; padding: 36px 32px 60px; max-width: 1000px; margin: 0 auto; }
  .page.active { display: block; }

  /* ── SECTION TITLE ── */
  .section-label {
    font-size: 10px; font-weight: 700; letter-spacing: .12em;
    color: var(--blue); text-transform: uppercase; margin-bottom: 6px;
  }
  .section-title {
    font-family: 'Syne', sans-serif; font-weight: 700;
    font-size: 22px; color: var(--navy); margin-bottom: 24px;
    padding-bottom: 12px; border-bottom: 2px solid var(--border);
  }

  /* ── CARDS ── */
  .card {
    background: var(--card); border-radius: 12px;
    border: 1px solid var(--border);
    padding: 22px 24px; margin-bottom: 16px;
    box-shadow: 0 1px 4px rgba(0,0,0,.04);
  }
  .card h3 {
    font-family: 'Syne', sans-serif; font-weight: 700;
    font-size: 15px; color: var(--navy); margin-bottom: 10px;
    display: flex; align-items: center; gap: 8px;
  }
  .card h3 .icon { font-size: 18px; }
  .card p, .card li {
    font-size: 13.5px; line-height: 1.75; color: #3A4A6B;
  }
  .card ul, .card ol { padding-left: 18px; }
  .card li { margin-bottom: 4px; }

  /* ── ACCENT STRIP ── */
  .strip {
    border-left: 4px solid var(--cyan);
    padding: 14px 18px;
    background: rgba(0,194,255,.05);
    border-radius: 0 8px 8px 0;
    margin-bottom: 14px;
  }
  .strip.amber { border-color: var(--amber); background: rgba(255,176,32,.06); }
  .strip.green  { border-color: var(--green); background: rgba(0,214,143,.06); }
  .strip.red    { border-color: var(--red);   background: rgba(255,77,109,.06); }
  .strip.purple { border-color: var(--purple);background: rgba(123,94,167,.06);}
  .strip p, .strip li { font-size: 13.5px; line-height: 1.7; color: #3A4A6B; }
  .strip strong { color: var(--navy); }
  .strip ul { padding-left: 16px; }

  /* ── GRID ── */
  .grid-2 { display: grid; grid-template-columns: 1fr 1fr; gap: 14px; margin-bottom: 16px; }
  @media(max-width:640px){ .grid-2 { grid-template-columns: 1fr; } }

  /* ── TAGS ── */
  .tag {
    display: inline-block; font-size: 11px; font-weight: 600;
    padding: 2px 9px; border-radius: 20px; margin: 2px;
  }
  .tag-blue   { background:#E8F0FE; color: var(--blue); }
  .tag-green  { background:#E6FAF3; color: #0A7A50; }
  .tag-amber  { background:#FFF4DC; color: #8A5A00; }
  .tag-red    { background:#FFE8ED; color: #A0002A; }
  .tag-purple { background:#F0EAF8; color: #5A3A8A; }

  /* ── Q&A ── */
  .qa { margin-bottom: 12px; }
  .qa-q {
    background: var(--navy); color: #fff;
    padding: 12px 16px; border-radius: 8px 8px 0 0;
    font-size: 13.5px; font-weight: 600; cursor: pointer;
    display: flex; justify-content: space-between; align-items: center;
    user-select: none;
  }
  .qa-q .arrow { transition: transform .25s; font-size: 12px; }
  .qa-q.open .arrow { transform: rotate(180deg); }
  .qa-a {
    display: none;
    background: #fff; border: 1px solid var(--navy);
    border-top: none; border-radius: 0 0 8px 8px;
    padding: 14px 16px;
  }
  .qa-a.open { display: block; }
  .qa-a p, .qa-a li { font-size: 13px; line-height: 1.75; color: #3A4A6B; }
  .qa-a ul { padding-left: 16px; }
  .qa-a .tip {
    margin-top: 10px; padding: 8px 12px;
    background: rgba(0,214,143,.08); border-radius: 6px;
    font-size: 12px; color: #0A7A50; font-weight: 500;
  }

  /* ── TABLE ── */
  table { width: 100%; border-collapse: collapse; margin-bottom: 16px; font-size: 13px; }
  th {
    background: var(--navy); color: #fff;
    padding: 10px 14px; text-align: left;
    font-family: 'Syne', sans-serif; font-weight: 600; font-size: 12px;
  }
  td { padding: 9px 14px; border-bottom: 1px solid var(--border); color: #3A4A6B; }
  tr:nth-child(even) td { background: #F9FBFF; }
  tr:hover td { background: #EEF3FF; }

  /* ── CHECKLIST ── */
  .checklist li {
    list-style: none; padding: 7px 0;
    border-bottom: 1px solid var(--border);
    font-size: 13.5px; color: #3A4A6B;
    display: flex; align-items: flex-start; gap: 8px;
  }
  .checklist li::before { content: '☐'; font-size: 15px; color: var(--blue); flex-shrink: 0; }
  .checklist li:last-child { border: none; }

  /* ── FLOW ── */
  .flow { display: flex; gap: 0; margin-bottom: 16px; flex-wrap: wrap; }
  .flow-step {
    flex: 1; min-width: 130px;
    background: var(--card); border: 1px solid var(--border);
    padding: 14px 12px; text-align: center;
    position: relative;
  }
  .flow-step:not(:last-child)::after {
    content: '→'; position: absolute; right: -12px; top: 50%;
    transform: translateY(-50%); color: var(--blue); font-size: 18px; z-index: 1;
  }
  .flow-step .num {
    width: 26px; height: 26px; border-radius: 50%;
    background: var(--blue); color: #fff;
    font-size: 11px; font-weight: 700;
    display: flex; align-items: center; justify-content: center;
    margin: 0 auto 8px;
  }
  .flow-step p { font-size: 12px; font-weight: 600; color: var(--navy); }
  .flow-step span { font-size: 11px; color: var(--muted); }

  /* ── PROGRESS BAR ── */
  .progress-wrap { background: var(--bg); border-radius: 4px; height: 6px; margin: 6px 0 14px; }
  .progress-bar { height: 6px; border-radius: 4px; background: linear-gradient(90deg, var(--blue), var(--cyan)); }

  /* ── PILL NAV ── */
  .pill-nav { display: flex; gap: 8px; margin-bottom: 20px; flex-wrap: wrap; }
  .pill-nav button {
    padding: 6px 14px; border-radius: 20px; border: 1.5px solid var(--border);
    background: var(--card); font-size: 12px; font-weight: 600;
    color: var(--muted); cursor: pointer; transition: all .2s;
  }
  .pill-nav button.active, .pill-nav button:hover {
    background: var(--navy); color: #fff; border-color: var(--navy);
  }
</style>
</head>
<body>

<div class="hero">
  <div class="badge">SENIOR SCRUM MASTER INTERVIEW PREP</div>
  <h1>Mastering <span>Scrum of Scrums</span></h1>
  <p>Everything you need to know — concepts, mechanics, anti-patterns, and interview Q&amp;A — in one place.</p>
</div>

<nav>
  <div class="logo">SoS Guide</div>
  <button class="active" onclick="showPage('what')">What is SoS</button>
  <button onclick="showPage('how')">How It Works</button>
  <button onclick="showPage('roles')">Roles</button>
  <button onclick="showPage('meetings')">Meetings</button>
  <button onclick="showPage('scaling')">vs Other Frameworks</button>
  <button onclick="showPage('antipatterns')">Anti-patterns</button>
  <button onclick="showPage('interview')">Interview Q&amp;A</button>
  <button onclick="showPage('cheatsheet')">Cheat Sheet</button>
</nav>

<!-- ══════════════════════════════════════════════════════════ -->
<!--  PAGE 1 — WHAT IS SoS                                     -->
<!-- ══════════════════════════════════════════════════════════ -->
<div id="page-what" class="page active">
  <div class="section-label">Module 1</div>
  <div class="section-title">What is Scrum of Scrums?</div>

  <div class="strip">
    <p><strong>Definition:</strong> Scrum of Scrums (SoS) is a scaled Agile coordination technique where one representative from each Scrum team meets regularly to synchronise cross-team work, surface inter-team dependencies, and resolve blockers that no single team can fix alone.</p>
  </div>

  <div class="card">
    <h3><span class="icon">🧠</span> The Core Idea — In One Sentence</h3>
    <p>If a Daily Scrum helps one team stay aligned, the Scrum of Scrums does the same thing for a <em>team of teams</em> — same structure, one level up.</p>
  </div>

  <div class="grid-2">
    <div class="card">
      <h3><span class="icon">📅</span> Origin</h3>
      <p>Introduced in <strong>1996</strong> by Jeff Sutherland and Ken Schwaber — the creators of Scrum itself. It was the original answer to the question: <em>"What do you do when you have more than one Scrum team on the same product?"</em></p>
    </div>
    <div class="card">
      <h3><span class="icon">📐</span> When to Use It</h3>
      <ul>
        <li>2+ Scrum teams working on the same product</li>
        <li>Teams share dependencies or integration points</li>
        <li>Blockers cross team boundaries</li>
        <li>Coordination is failing (handoffs, missed dependencies)</li>
      </ul>
    </div>
  </div>

  <div class="card">
    <h3><span class="icon">⚠️</span> Pre-condition — Critical to Know</h3>
    <div class="strip red">
      <p><strong>SoS only works if each individual team is already running Scrum well.</strong> You cannot scale dysfunction. If teams aren't doing proper standups, retrospectives, and sprints, fix that first before introducing SoS.</p>
    </div>
    <p>As Jeff Sutherland said: <em>"Don't attempt to Scrum in the large until you're doing it successfully in the small."</em></p>
  </div>

  <div class="card">
    <h3><span class="icon">💡</span> What Problem It Solves</h3>
    <table>
      <tr><th>Problem</th><th>How SoS Addresses It</th></tr>
      <tr><td>Team A blocks Team B's sprint</td><td>Dependency surfaced in SoS meeting, resolved immediately</td></tr>
      <tr><td>Duplicate work across teams</td><td>Transparency across teams prevents overlap</td></tr>
      <tr><td>Integration surprises at release</td><td>Regular sync catches integration issues early</td></tr>
      <tr><td>Escalation goes to management</td><td>Teams resolve cross-team issues themselves</td></tr>
      <tr><td>Nobody knows what other teams are doing</td><td>Regular ambassadors bring cross-team visibility</td></tr>
    </table>
  </div>
</div>

<!-- ══════════════════════════════════════════════════════════ -->
<!--  PAGE 2 — HOW IT WORKS                                    -->
<!-- ══════════════════════════════════════════════════════════ -->
<div id="page-how" class="page">
  <div class="section-label">Module 2</div>
  <div class="section-title">How Scrum of Scrums Works</div>

  <div class="card">
    <h3><span class="icon">🏗️</span> Structure</h3>
    <p>Each Scrum team appoints an <strong>Ambassador</strong> (usually the Scrum Master or a senior team member). These ambassadors form the SoS team and meet at a regular cadence.</p>
    <br/>
    <div class="flow">
      <div class="flow-step"><div class="num">1</div><p>Team A</p><span>Ambassador →</span></div>
      <div class="flow-step"><div class="num">2</div><p>Team B</p><span>Ambassador →</span></div>
      <div class="flow-step"><div class="num">3</div><p>Team C</p><span>Ambassador →</span></div>
      <div class="flow-step"><div class="num">4</div><p>SoS Meeting</p><span>Sync + Resolve</span></div>
    </div>
  </div>

  <div class="card">
    <h3><span class="icon">❓</span> The Four SoS Questions</h3>
    <p style="margin-bottom:12px">Every ambassador answers these four questions — an expansion of the 3 Daily Scrum questions:</p>
    <div class="strip green">
      <ul>
        <li><strong>1.</strong> What has your team done since we last met that could affect other teams?</li>
        <li><strong>2.</strong> What will your team do before we meet again that could affect other teams?</li>
        <li><strong>3.</strong> Is your team blocked on anything? Is your team blocking other teams?</li>
        <li><strong>4.</strong> Are you about to introduce anything that other teams should be aware of?</li>
      </ul>
    </div>
    <div class="strip amber">
      <p><strong>Key distinction from a daily standup:</strong> The SoS focuses only on <em>cross-team</em> matters. Team-internal progress is not discussed here. That's what the individual team standup is for.</p>
    </div>
  </div>

  <div class="card">
    <h3><span class="icon">📆</span> Cadence</h3>
    <table>
      <tr><th>Situation</th><th>Recommended Frequency</th></tr>
      <tr><td>Teams tightly coupled / active integration work</td><td>Daily</td></tr>
      <tr><td>Normal sprint work, moderate dependencies</td><td>3× per week</td></tr>
      <tr><td>Loosely coupled teams, fewer shared concerns</td><td>2× per week or weekly</td></tr>
    </table>
    <p style="font-size:13px; color:var(--muted)">The right cadence is determined empirically — start more frequently and reduce as coordination improves. Adjust in retrospectives.</p>
  </div>

  <div class="card">
    <h3><span class="icon">📏</span> Duration</h3>
    <p>Timeboxed to <strong>15–30 minutes maximum</strong>. Anything requiring a longer discussion is taken offline into a separate session. The SoS is a sync, not a working session.</p>
  </div>

  <div class="card">
    <h3><span class="icon">📊</span> The SoS Board</h3>
    <p>Best practice is to maintain a visual SoS board that tracks cross-team dependencies, their status, and who owns resolution. Columns typically include:</p>
    <br/>
    <div class="grid-2">
      <div class="strip">
        <ul>
          <li><strong>Dependency</strong> — what is the dependency?</li>
          <li><strong>Team A</strong> — who needs it?</li>
          <li><strong>Team B</strong> — who provides it?</li>
        </ul>
      </div>
      <div class="strip green">
        <ul>
          <li><strong>Due by</strong> — sprint / date needed</li>
          <li><strong>Status</strong> — on track / at risk / blocked</li>
          <li><strong>Owner</strong> — who is resolving?</li>
        </ul>
      </div>
    </div>
  </div>
</div>

<!-- ══════════════════════════════════════════════════════════ -->
<!--  PAGE 3 — ROLES                                           -->
<!-- ══════════════════════════════════════════════════════════ -->
<div id="page-roles" class="page">
  <div class="section-label">Module 3</div>
  <div class="section-title">Roles in Scrum of Scrums</div>

  <div class="card">
    <h3><span class="icon">🧑‍💼</span> The Ambassador (SoS Representative)</h3>
    <div class="strip">
      <p><strong>Who:</strong> Usually the Scrum Master, but can be a senior developer or tech lead — whoever is best positioned to discuss cross-team technical and process dependencies.</p>
    </div>
    <p style="margin-bottom:10px"><strong>Responsibilities:</strong></p>
    <ul>
      <li>Represent their team's status, plans, and blockers accurately</li>
      <li>Surface dependencies before they become blockers</li>
      <li>Bring back decisions and outcomes to their team</li>
      <li>Own the resolution of cross-team issues on behalf of their team</li>
      <li>Participate in the SoS board maintenance</li>
    </ul>
    <br/>
    <div class="strip amber">
      <p><strong>Interview insight:</strong> Ambassadors are not permanent. A team may send a developer to the SoS when a specific technical dependency needs to be resolved, even if the Scrum Master normally attends. Flexibility matters more than rigid role assignment.</p>
    </div>
  </div>

  <div class="card">
    <h3><span class="icon">🧭</span> The SoS Scrum Master (Meta-Scrum Master)</h3>
    <p style="margin-bottom:10px">In larger SoS setups, someone facilitates the SoS meeting itself. This is often called the <strong>Scrum of Scrums Master</strong> or <strong>Chief Scrum Master</strong>.</p>
    <table>
      <tr><th>Regular Scrum Master</th><th>SoS Scrum Master</th></tr>
      <tr><td>Serves one team</td><td>Serves the SoS team (team of teams)</td></tr>
      <tr><td>Removes blockers within the team</td><td>Removes blockers between teams</td></tr>
      <tr><td>Coaches one team on Scrum</td><td>Coaches multiple SMs and teams</td></tr>
      <tr><td>Facilitates team ceremonies</td><td>Facilitates SoS ceremony</td></tr>
      <tr><td>Escalates to management</td><td>Bridges teams and leadership</td></tr>
    </table>
  </div>

  <div class="card">
    <h3><span class="icon">🛒</span> MetaScrum / Executive Action Team</h3>
    <p>In <strong>Scrum@Scale</strong>, the SoS has a Product Owner counterpart called the <strong>MetaScrum</strong> — where Product Owners from all teams align on priorities, shared backlog items, and release strategy. As a senior SM, you should know both sides of the coin.</p>
    <div class="strip purple">
      <p><strong>SoS = How (coordination, delivery, blockers)</strong><br/>
      <strong>MetaScrum = What (priorities, scope, product direction)</strong></p>
    </div>
  </div>
</div>

<!-- ══════════════════════════════════════════════════════════ -->
<!--  PAGE 4 — MEETINGS                                        -->
<!-- ══════════════════════════════════════════════════════════ -->
<div id="page-meetings" class="page">
  <div class="section-label">Module 4</div>
  <div class="section-title">SoS Ceremonies & Meetings</div>

  <div class="card">
    <h3><span class="icon">📋</span> SoS Daily Sync</h3>
    <p><strong>Timebox:</strong> 15–30 min &nbsp;|&nbsp; <strong>Who:</strong> One ambassador per team &nbsp;|&nbsp; <strong>Frequency:</strong> Daily to 2× week</p>
    <br/>
    <div class="strip green">
      <p><strong>Agenda:</strong> Round-robin of the 4 SoS questions. Blockers and dependencies go on the SoS board. Nothing is solved in the meeting — issues are taken offline.</p>
    </div>
  </div>

  <div class="card">
    <h3><span class="icon">📐</span> Scaled Sprint Planning</h3>
    <p>Happens at the start of each sprint. Teams plan <em>together</em> before breaking into individual team planning so that:</p>
    <ul style="margin-top:8px">
      <li>Shared backlog items are identified and assigned</li>
      <li>Cross-team dependencies are made visible upfront</li>
      <li>Integration points are agreed on</li>
      <li>Teams align on what "done" looks like for the sprint</li>
    </ul>
    <br/>
    <div class="strip amber">
      <p><strong>Common failure:</strong> Teams plan in silos, then surface dependencies mid-sprint. Scaled sprint planning prevents this.</p>
    </div>
  </div>

  <div class="card">
    <h3><span class="icon">🔍</span> Scaled Sprint Review</h3>
    <p>At end of sprint. Teams demonstrate their combined increment together. Key goals:</p>
    <ul style="margin-top:8px">
      <li>Show integrated, working product — not individual team outputs</li>
      <li>Stakeholders see the whole, not fragments</li>
      <li>Identify integration gaps that need addressing in next sprint</li>
    </ul>
  </div>

  <div class="card">
    <h3><span class="icon">🔄</span> Scaled Retrospective</h3>
    <p>Two-level retro structure:</p>
    <div class="grid-2">
      <div class="strip">
        <p><strong>Level 1 — Team Retro</strong><br/>Each team runs their own retrospective first. Identifies what they want to raise at the SoS level.</p>
      </div>
      <div class="strip green">
        <p><strong>Level 2 — SoS Retro</strong><br/>Ambassadors bring cross-team issues. Focus on process improvements that span teams, not team-internal issues.</p>
      </div>
    </div>
  </div>

  <div class="card">
    <h3><span class="icon">🗺️</span> Dependency Mapping Session</h3>
    <p>Not a standard Scrum ceremony, but a <strong>best practice</strong> at the start of each sprint or PI. Teams visually map all inter-team dependencies using a board or tool (Miro, physical wall). Key output: a dependency risk register.</p>
    <div class="strip purple" style="margin-top:12px">
      <p><strong>Senior SM angle:</strong> Proactively running dependency mapping sessions before blockers emerge is a sign of a mature SoS practice — interviewers love this answer.</p>
    </div>
  </div>
</div>

<!-- ══════════════════════════════════════════════════════════ -->
<!--  PAGE 5 — VS OTHER FRAMEWORKS                             -->
<!-- ══════════════════════════════════════════════════════════ -->
<div id="page-scaling" class="page">
  <div class="section-label">Module 5</div>
  <div class="section-title">SoS vs Other Scaling Frameworks</div>

  <div class="strip amber">
    <p><strong>Why this matters in interviews:</strong> A senior SM is expected to know where SoS fits in the broader scaling landscape and when to recommend alternatives. This is a very common interview question.</p>
  </div>

  <div class="card">
    <h3><span class="icon">📊</span> Framework Comparison</h3>
    <table>
      <tr><th>Framework</th><th>Scale</th><th>Prescriptiveness</th><th>SoS Role</th><th>Best For</th></tr>
      <tr><td><strong>SoS (standalone)</strong></td><td>2–10 teams</td><td>Low — very flexible</td><td>Core mechanism</td><td>Starting point, small-medium scale</td></tr>
      <tr><td><strong>Scrum@Scale</strong></td><td>Any</td><td>Medium</td><td>Core delivery component</td><td>Organisations wanting Jeff Sutherland's full model</td></tr>
      <tr><td><strong>SAFe</strong></td><td>50–1000s</td><td>High — very prescriptive</td><td>Within ART (Agile Release Train)</td><td>Large enterprises, regulated industries</td></tr>
      <tr><td><strong>LeSS</strong></td><td>2–8 teams (LeSS) / huge</td><td>Low-medium</td><td>Not used — simpler model</td><td>Teams wanting minimal overhead</td></tr>
      <tr><td><strong>Nexus</strong></td><td>3–9 teams</td><td>Medium</td><td>Nexus Integration Team plays this role</td><td>Technical integration focus</td></tr>
    </table>
  </div>

  <div class="grid-2">
    <div class="card">
      <h3><span class="icon">✅</span> Choose SoS When</h3>
      <ul>
        <li>2–5 teams, same product</li>
        <li>You want lightweight coordination</li>
        <li>Teams are already good at Scrum</li>
        <li>No need for heavy process framework</li>
        <li>You want to grow organically</li>
      </ul>
    </div>
    <div class="card">
      <h3><span class="icon">❌</span> SoS May Not Be Enough When</h3>
      <ul>
        <li>10+ teams — SoS of SoS needed</li>
        <li>Complex release trains / ARTs</li>
        <li>Portfolio-level alignment needed</li>
        <li>Deep technical integration challenges</li>
        <li>Organisation needs governance structure</li>
      </ul>
    </div>
  </div>

  <div class="card">
    <h3><span class="icon">🔁</span> SoS of SoS (Recursive Scaling)</h3>
    <p>When you have many teams (e.g. 15 teams = 3 groups of 5), you run SoS at two levels:</p>
    <div class="strip purple" style="margin-top:12px">
      <ul>
        <li><strong>Level 1:</strong> 3 SoS groups (5 teams each) — each runs its own SoS meeting</li>
        <li><strong>Level 2:</strong> 1 SoS of SoS — one ambassador from each SoS group meets to align at the programme level</li>
      </ul>
    </div>
    <p style="margin-top:10px; font-size:13px">This is also called <strong>Scrum@Scale</strong> in Jeff Sutherland's framework and can theoretically scale infinitely.</p>
  </div>
</div>

<!-- ══════════════════════════════════════════════════════════ -->
<!--  PAGE 6 — ANTI-PATTERNS                                   -->
<!-- ══════════════════════════════════════════════════════════ -->
<div id="page-antipatterns" class="page">
  <div class="section-label">Module 6</div>
  <div class="section-title">Anti-patterns & How to Fix Them</div>
  <p style="font-size:13.5px; color:var(--muted); margin-bottom:20px">A senior SM is expected to recognise and articulate these. Interviewers will test this directly.</p>

  <div class="card">
    <h3><span class="icon">🚨</span> Anti-pattern 1: The Status Report Meeting</h3>
    <div class="strip red">
      <p><strong>What happens:</strong> Ambassadors read out their team's progress like a status update. No cross-team issues are discussed. The SoS becomes a reporting meeting for management.</p>
    </div>
    <div class="strip green">
      <p><strong>Fix:</strong> Strictly enforce the 4 SoS questions, focusing only on cross-team impacts. Remind ambassadors: "If it only affects your team, save it for your own standup."</p>
    </div>
  </div>

  <div class="card">
    <h3><span class="icon">🚨</span> Anti-pattern 2: The Wrong People in the Room</h3>
    <div class="strip red">
      <p><strong>What happens:</strong> The same person always attends regardless of what needs to be discussed. A technical integration problem is discussed without any developer present.</p>
    </div>
    <div class="strip green">
      <p><strong>Fix:</strong> The ambassador role should be fluid. If a sprint has complex BE/FE integration, send the tech lead. The right person depends on the current dependencies at play.</p>
    </div>
  </div>

  <div class="card">
    <h3><span class="icon">🚨</span> Anti-pattern 3: Problems Solved In the Meeting</h3>
    <div class="strip red">
      <p><strong>What happens:</strong> The SoS meeting runs 60+ minutes because teams try to solve blockers in real time with everyone present.</p>
    </div>
    <div class="strip green">
      <p><strong>Fix:</strong> Timebox strictly to 15–30 min. Blockers are noted on the SoS board, assigned an owner, and resolved in a separate smaller meeting with only the relevant people. Classic "after-party" model.</p>
    </div>
  </div>

  <div class="card">
    <h3><span class="icon">🚨</span> Anti-pattern 4: SoS Becomes a Management Tool</h3>
    <div class="strip red">
      <p><strong>What happens:</strong> Management starts attending and using the SoS to get project status. Ambassadors start filtering what they say. Psychological safety drops.</p>
    </div>
    <div class="strip green">
      <p><strong>Fix:</strong> The SoS is a team-to-team coordination mechanism, not a reporting channel. Management gets information through dashboards and Sprint Reviews, not the SoS. Coach leadership on the distinction.</p>
    </div>
  </div>

  <div class="card">
    <h3><span class="icon">🚨</span> Anti-pattern 5: Scaling Before Teams Are Ready</h3>
    <div class="strip red">
      <p><strong>What happens:</strong> Teams are struggling with basic Scrum but SoS is introduced anyway. The scaled ceremony amplifies existing dysfunction.</p>
    </div>
    <div class="strip green">
      <p><strong>Fix:</strong> Assess each team's Scrum maturity first. Fix team-level issues before scaling. "Pull the Andon Cord" — stop the line, fix the problem, then scale.</p>
    </div>
  </div>

  <div class="card">
    <h3><span class="icon">🚨</span> Anti-pattern 6: No Dependency Board</h3>
    <div class="strip red">
      <p><strong>What happens:</strong> Dependencies are discussed verbally and forgotten. The same blocker resurfaces every meeting.</p>
    </div>
    <div class="strip green">
      <p><strong>Fix:</strong> Maintain a visible, shared SoS dependency board (physical or digital — Miro, Jira). Every identified dependency has an owner, a due date, and a status. Review it at the start of every SoS meeting.</p>
    </div>
  </div>
</div>

<!-- ══════════════════════════════════════════════════════════ -->
<!--  PAGE 7 — INTERVIEW Q&A                                   -->
<!-- ══════════════════════════════════════════════════════════ -->
<div id="page-interview" class="page">
  <div class="section-label">Module 7</div>
  <div class="section-title">Senior SM Interview Q&amp;A</div>

  <div class="pill-nav">
    <button class="active" onclick="filterQA('all', this)">All Questions</button>
    <button onclick="filterQA('concept', this)">Concept</button>
    <button onclick="filterQA('scenario', this)">Scenario-based</button>
    <button onclick="filterQA('behavioural', this)">Behavioural</button>
    <button onclick="filterQA('advanced', this)">Advanced</button>
  </div>

  <div id="qa-container">

    <div class="qa" data-cat="concept">
      <div class="qa-q" onclick="toggleQA(this)">What is Scrum of Scrums and when would you use it? <span class="arrow">▼</span></div>
      <div class="qa-a">
        <p>Scrum of Scrums is a scaled coordination technique where one representative per Scrum team meets regularly to synchronise cross-team dependencies, surface blockers, and align on shared goals — without disrupting individual team autonomy.</p>
        <br/><p>I'd recommend SoS when two or more teams are working on the same product and begin experiencing inter-team dependencies, integration challenges, or duplicate work. The trigger isn't team size — it's the presence of cross-team coordination needs.</p>
        <div class="tip">💡 Tip: Always mention the pre-condition — "I would first confirm each team is running Scrum effectively before introducing SoS, since you can't scale dysfunction."</div>
      </div>
    </div>

    <div class="qa" data-cat="concept">
      <div class="qa-q" onclick="toggleQA(this)">How does SoS differ from a regular Daily Scrum? <span class="arrow">▼</span></div>
      <div class="qa-a">
        <ul>
          <li>Daily Scrum = one team, internal sync, 15 min, 3 questions</li>
          <li>SoS = team of teams, cross-team sync, 15–30 min, 4 questions</li>
          <li>Daily Scrum answers "what are we building today" — SoS answers "what are we building together and what is in each other's way"</li>
          <li>SoS is not a status meeting for management — it's a peer-to-peer coordination tool</li>
        </ul>
        <div class="tip">💡 The 4th SoS question ("are you about to introduce anything others should know about?") is the key differentiator — it's forward-looking and cross-team focused.</div>
      </div>
    </div>

    <div class="qa" data-cat="concept">
      <div class="qa-q" onclick="toggleQA(this)">Who should be the ambassador at a SoS meeting? <span class="arrow">▼</span></div>
      <div class="qa-a">
        <p>The ambassador should be whoever is best positioned to represent the team's cross-team concerns for that sprint. It's often the Scrum Master, but it should be fluid — if there's a complex technical integration in play, a senior developer or tech lead might be more valuable in the room.</p>
        <br/><p>The key is that the ambassador must have enough context to speak to dependencies, blockers, and commitments — and enough authority to make coordination decisions on behalf of the team.</p>
        <div class="tip">💡 Avoid the anti-pattern of always sending the same person regardless of context.</div>
      </div>
    </div>

    <div class="qa" data-cat="scenario">
      <div class="qa-q" onclick="toggleQA(this)">Team B is blocked on Team A's API. Team A says it will be ready "next sprint." How do you handle this? <span class="arrow">▼</span></div>
      <div class="qa-a">
        <p>Using the STAR method:</p>
        <ul>
          <li><strong>Situation:</strong> Hard dependency creating a sprint-level blocker for Team B</li>
          <li><strong>Task:</strong> Resolve without escalating to management, maintaining team autonomy</li>
          <li><strong>Action:</strong> First, facilitate a conversation between both teams in the SoS to get a precise commitment — "next sprint" is vague. Get a specific date and a specific API contract. Then explore whether Team B can work on non-dependent features in the interim. Log this dependency on the SoS board with an owner and a due date. Check in daily until resolved.</li>
          <li><strong>Result:</strong> Teams aligned on a specific date, Team B replanned their sprint around the dependency, blocker resolved in the next SoS cycle with no escalation needed.</li>
        </ul>
        <div class="tip">💡 Mention the SoS dependency board and the importance of getting a specific commitment, not a vague one.</div>
      </div>
    </div>

    <div class="qa" data-cat="scenario">
      <div class="qa-q" onclick="toggleQA(this)">How do you run Sprint Planning at scale with multiple teams? <span class="arrow">▼</span></div>
      <div class="qa-a">
        <p>I use a two-wave planning approach:</p>
        <ul>
          <li><strong>Wave 1 — Scaled Planning (all teams together, 1–2 hrs):</strong> Ambassadors from each team review the upcoming sprint backlog together. Dependencies are identified and mapped. Teams agree on integration points, shared components, and sequencing. A dependency board is updated.</li>
          <li><strong>Wave 2 — Team Planning (each team separately):</strong> Each team plans their own sprint with full awareness of cross-team commitments from Wave 1.</li>
        </ul>
        <br/><p>The key output of Wave 1 is a clear picture of who is building what, what relies on what, and in what order — before any team commits to their sprint backlog.</p>
        <div class="tip">💡 Mention the risk of the opposite — teams planning in silos and discovering dependencies mid-sprint.</div>
      </div>
    </div>

    <div class="qa" data-cat="scenario">
      <div class="qa-q" onclick="toggleQA(this)">The SoS meeting is becoming a status report for management. What do you do? <span class="arrow">▼</span></div>
      <div class="qa-a">
        <p>This is a classic SoS anti-pattern. My approach:</p>
        <ul>
          <li>Have a direct conversation with management about the purpose of SoS — it's a peer coordination tool, not a reporting mechanism</li>
          <li>Provide management with the information they need through a separate channel: a dashboard, a weekly written update, or access to the SoS board</li>
          <li>Facilitate a team retrospective to surface how the meeting's dynamic has changed and let the team articulate what they want back</li>
          <li>Reinforce the 4 SoS questions — if an ambassador starts giving status, gently redirect: "Is there a cross-team impact to flag here?"</li>
        </ul>
        <div class="tip">💡 Show you can coach leadership without being adversarial. Frame it as: "Here's a better way to get what you need."</div>
      </div>
    </div>

    <div class="qa" data-cat="behavioural">
      <div class="qa-q" onclick="toggleQA(this)">Tell me about a time you ran SoS and it wasn't working. What did you change? <span class="arrow">▼</span></div>
      <div class="qa-a">
        <p>Structure your answer with STAR. Key themes to include regardless of your specific story:</p>
        <ul>
          <li>The SoS was functioning as a status meeting (common problem)</li>
          <li>You facilitated a retrospective specifically about the SoS format</li>
          <li>You re-trained ambassadors on the 4 questions and cross-team focus</li>
          <li>You introduced or updated the SoS dependency board</li>
          <li>You changed the cadence based on empirical observation</li>
          <li>Outcome: blockers resolved faster, teams more autonomous</li>
        </ul>
        <div class="tip">💡 Interviewers aren't looking for a perfect story — they want to see reflection, adaptation, and measurable improvement. Mention the before/after.</div>
      </div>
    </div>

    <div class="qa" data-cat="behavioural">
      <div class="qa-q" onclick="toggleQA(this)">How do you handle a situation where one team is consistently blocking others? <span class="arrow">▼</span></div>
      <div class="qa-a">
        <p>I'd approach this at multiple levels:</p>
        <ul>
          <li><strong>First:</strong> Make the pattern visible — use the SoS board to show the data. Sometimes teams don't realise how often they're the bottleneck until they see it.</li>
          <li><strong>Second:</strong> Investigate root cause — is it capacity? Unclear interfaces? Too many dependencies on a specialised skill in that team?</li>
          <li><strong>Third:</strong> Work with that team's SM and PO on structural fixes — can work be redistributed? Can the dependency be removed through better team design (e.g. moving to feature teams vs. component teams)?</li>
          <li><strong>Fourth:</strong> If it's a persistent capacity issue, escalate to leadership with data — not as a complaint but as an organisational impediment that needs resourcing.</li>
        </ul>
      </div>
    </div>

    <div class="qa" data-cat="advanced">
      <div class="qa-q" onclick="toggleQA(this)">How does SoS fit within Scrum@Scale? <span class="arrow">▼</span></div>
      <div class="qa-a">
        <p>In Scrum@Scale (Jeff Sutherland's framework), SoS is one of two complementary scaling mechanisms:</p>
        <ul>
          <li><strong>SoS</strong> = the Scrum Master cycle — coordinates the "how" of delivery (process, dependencies, blockers)</li>
          <li><strong>MetaScrum</strong> = the Product Owner cycle — coordinates the "what" (priorities, backlog, vision)</li>
        </ul>
        <br/><p>Scrum@Scale also introduces the concept of an <strong>Executive Action Team (EAT)</strong> — a small group that resolves organisational impediments that the SoS cannot fix itself (e.g. hiring, tooling, policy changes).</p>
        <p style="margin-top:8px">The SoS can scale recursively — a SoS of SoSs — which allows the framework to theoretically scale to any number of teams.</p>
      </div>
    </div>

    <div class="qa" data-cat="advanced">
      <div class="qa-q" onclick="toggleQA(this)">When would you recommend SAFe over SoS? <span class="arrow">▼</span></div>
      <div class="qa-a">
        <p>SoS is lightweight and team-driven — ideal for 2–8 teams already doing Scrum well, where you want minimal overhead and want teams to self-organise coordination.</p>
        <br/><p>I'd recommend SAFe when:</p>
        <ul>
          <li>The organisation has 50+ people across many teams</li>
          <li>There are complex portfolio/programme-level dependencies</li>
          <li>The organisation needs governance, compliance, and audit structures</li>
          <li>Release trains need to be synchronised on a quarterly cadence (PI Planning)</li>
          <li>Leadership needs a structured transformation roadmap</li>
        </ul>
        <br/><p>The trade-off: SAFe gives you structure but adds significant process overhead. SoS gives you flexibility but requires team maturity and self-organisation.</p>
        <div class="tip">💡 Show you can make pragmatic recommendations, not just advocate for one framework.</div>
      </div>
    </div>

    <div class="qa" data-cat="advanced">
      <div class="qa-q" onclick="toggleQA(this)">How do you measure whether your SoS is effective? <span class="arrow">▼</span></div>
      <div class="qa-a">
        <p>I track both leading and lagging indicators:</p>
        <ul>
          <li><strong>Dependency resolution time</strong> — how many days from blocker surfaced to resolved? Trending down = SoS working.</li>
          <li><strong>Sprint spillover caused by cross-team blockers</strong> — should decrease over time</li>
          <li><strong>Number of integration surprises at Sprint Review</strong> — should approach zero</li>
          <li><strong>SoS meeting duration</strong> — consistently under 30 min is a good sign</li>
          <li><strong>Team satisfaction</strong> — do teams feel coordination is better? Simple pulse survey.</li>
          <li><strong>Escalations to management</strong> — should decrease as SoS resolves more at the team level</li>
        </ul>
        <div class="tip">💡 Mention that you'd review these metrics in the scaled retrospective and use them to adjust the SoS cadence and format empirically.</div>
      </div>
    </div>

  </div>
</div>

<!-- ══════════════════════════════════════════════════════════ -->
<!--  PAGE 8 — CHEAT SHEET                                     -->
<!-- ══════════════════════════════════════════════════════════ -->
<div id="page-cheatsheet" class="page">
  <div class="section-label">Module 8</div>
  <div class="section-title">Quick Reference Cheat Sheet</div>

  <div class="grid-2">
    <div class="card">
      <h3><span class="icon">❓</span> The 4 SoS Questions</h3>
      <ol style="padding-left:16px; margin-top:8px">
        <li style="margin-bottom:6px; font-size:13.5px">What has your team done that <strong>affects other teams?</strong></li>
        <li style="margin-bottom:6px; font-size:13.5px">What will your team do that <strong>may affect other teams?</strong></li>
        <li style="margin-bottom:6px; font-size:13.5px">Is your team <strong>blocked or blocking</strong> others?</li>
        <li style="margin-bottom:6px; font-size:13.5px">Are you introducing anything others <strong>should know about?</strong></li>
      </ol>
    </div>
    <div class="card">
      <h3><span class="icon">⚙️</span> SoS at a Glance</h3>
      <table style="margin:0">
        <tr><td><strong>Timebox</strong></td><td>15–30 minutes</td></tr>
        <tr><td><strong>Frequency</strong></td><td>Daily → 2× week → weekly</td></tr>
        <tr><td><strong>Who attends</strong></td><td>1 ambassador per team</td></tr>
        <tr><td><strong>Focus</strong></td><td>Cross-team only</td></tr>
        <tr><td><strong>Output</strong></td><td>Updated dependency board</td></tr>
      </table>
    </div>
  </div>

  <div class="card">
    <h3><span class="icon">🚨</span> Top 6 Anti-patterns (Know These Cold)</h3>
    <div style="display:flex; flex-wrap:wrap; gap:8px; margin-top:10px">
      <span class="tag tag-red">Status report meeting</span>
      <span class="tag tag-red">Wrong person attending</span>
      <span class="tag tag-red">Solving problems in the meeting</span>
      <span class="tag tag-red">Management using it for reporting</span>
      <span class="tag tag-red">Scaling before teams are ready</span>
      <span class="tag tag-red">No dependency board</span>
    </div>
  </div>

  <div class="card">
    <h3><span class="icon">🆚</span> Framework One-liners</h3>
    <table style="margin:0">
      <tr><td><strong>SoS</strong></td><td>Lightweight, team-driven, 2–8 teams, minimal overhead</td></tr>
      <tr><td><strong>Scrum@Scale</strong></td><td>SoS + MetaScrum + recursive scaling to any size</td></tr>
      <tr><td><strong>SAFe</strong></td><td>Enterprise-grade, PI Planning, Agile Release Trains, governance</td></tr>
      <tr><td><strong>LeSS</strong></td><td>Single PO + backlog, minimal ceremony added, team purity</td></tr>
      <tr><td><strong>Nexus</strong></td><td>Technical integration focus, Nexus Integration Team</td></tr>
    </table>
  </div>

  <div class="card">
    <h3><span class="icon">📋</span> Senior SM Interview Readiness Checklist</h3>
    <ul class="checklist">
      <li>Can explain SoS in one sentence without jargon</li>
      <li>Know the 4 SoS questions by heart</li>
      <li>Can distinguish Forecast vs Ambassador vs SoS SM roles</li>
      <li>Can name 6 anti-patterns and their fixes</li>
      <li>Have a real STAR story about running or fixing SoS</li>
      <li>Can compare SoS vs SAFe vs LeSS vs Nexus vs Scrum@Scale</li>
      <li>Know what MetaScrum is and how it complements SoS</li>
      <li>Can explain how to measure SoS effectiveness</li>
      <li>Know the scaled ceremonies: planning, review, retro</li>
      <li>Can explain SoS of SoS (recursive scaling)</li>
    </ul>
  </div>

  <div class="strip purple">
    <p><strong>Key message to land in every interview:</strong> "SoS is not a ceremony you run — it's a culture of cross-team transparency you build. The meeting is just the visible tip of that iceberg."</p>
  </div>
</div>

<script>
// ── PROTECTION ────────────────────────────────────────────────
// Disable right-click
document.addEventListener('contextmenu', e => e.preventDefault());

// Disable text selection
document.addEventListener('selectstart', e => e.preventDefault());

// Disable drag
document.addEventListener('dragstart', e => e.preventDefault());

// Disable keyboard shortcuts: Ctrl+C, Ctrl+A, Ctrl+S, Ctrl+U, Ctrl+P, F12
document.addEventListener('keydown', e => {
  const blocked = (
    (e.ctrlKey && ['c','a','s','u','p'].includes(e.key.toLowerCase())) ||
    (e.ctrlKey && e.shiftKey && ['i','j','c'].includes(e.key.toLowerCase())) ||
    e.key === 'F12'
  );
  if (blocked) e.preventDefault();
});

// Disable print
window.onbeforeprint = () => { document.body.style.display = 'none'; };
window.onafterprint  = () => { document.body.style.display = ''; };

function showPage(id) {
  document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
  document.querySelectorAll('nav button').forEach(b => b.classList.remove('active'));
  document.getElementById('page-' + id).classList.add('active');
  event.target.classList.add('active');
  window.scrollTo({top: 0, behavior: 'smooth'});
}
function toggleQA(el) {
  el.classList.toggle('open');
  const ans = el.nextElementSibling;
  ans.classList.toggle('open');
}
function filterQA(cat, btn) {
  document.querySelectorAll('.pill-nav button').forEach(b => b.classList.remove('active'));
  btn.classList.add('active');
  document.querySelectorAll('.qa').forEach(q => {
    q.style.display = (cat === 'all' || q.dataset.cat === cat) ? 'block' : 'none';
  });
}
</script>
</body>
</html>
