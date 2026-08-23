---
layout: null
permalink: /cv/
---
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mark C. Hunnell — Curriculum Vitae</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Source+Serif+4:ital,opsz,wght@0,8..60,400;0,8..60,500;0,8..60,600;0,8..60,700;1,8..60,400;1,8..60,600&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --bg: #faf9f6;
    --paper: #ffffff;
    --ink: #1c1a17;
    --muted: #6b675f;
    --rule: #d8d3c8;
    --accent: #8a3b32;
    --accent-soft: #c98a80;
    --link: #2c4a63;
    --serif: 'Source Serif 4', Georgia, 'Times New Roman', serif;
    --sans: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    --maxw: 780px;
  }

  * { box-sizing: border-box; }

  html, body {
    margin: 0;
    padding: 0;
    background: var(--bg);
    color: var(--ink);
    font-family: var(--serif);
    font-size: 16px;
    line-height: 1.55;
    -webkit-font-smoothing: antialiased;
  }

  .page {
    max-width: var(--maxw);
    margin: 0 auto;
    background: var(--paper);
    padding: 3.2rem 3.4rem 4rem;
    box-shadow: 0 0 0 1px rgba(0,0,0,0.03), 0 20px 50px -25px rgba(0,0,0,0.25);
  }

  /* ---------- header ---------- */
  header.cv-header {
    text-align: center;
    margin-bottom: 2.1rem;
  }

  .cv-name {
    font-family: var(--serif);
    font-weight: 600;
    font-size: 2.5rem;
    letter-spacing: 0.01em;
    margin: 0 0 0.35rem;
    color: var(--ink);
  }

  .cv-title {
    font-family: var(--sans);
    font-size: 0.95rem;
    color: var(--muted);
    letter-spacing: 0.02em;
    line-height: 1.6;
  }

  .cv-contact {
    font-family: var(--sans);
    font-size: 0.85rem;
    color: var(--muted);
    margin-top: 0.6rem;
    letter-spacing: 0.01em;
  }

  .cv-contact a { color: var(--link); text-decoration: none; }
  .cv-contact a:hover { text-decoration: underline; }

  .cv-contact .sep {
    color: var(--accent-soft);
    margin: 0 0.55em;
  }

  /* ---------- graph-motif section divider ---------- */
  .node-rule {
    display: flex;
    align-items: center;
    width: 100%;
    height: 10px;
    margin: 0.15rem 0 1.15rem;
  }
  .node-rule svg { width: 100%; height: 10px; display: block; overflow: visible; }
  .node-rule line { stroke: var(--rule); stroke-width: 1.3; }
  .node-rule circle { fill: var(--accent); }
  .node-rule circle.hollow { fill: var(--paper); stroke: var(--accent); stroke-width: 1.4; }

  h2.section-title {
    font-family: var(--serif);
    font-weight: 600;
    font-size: 1.32rem;
    letter-spacing: 0.01em;
    margin: 0;
    padding-top: 0.2rem;
    color: var(--ink);
  }

  section.cv-section { margin-top: 2.1rem; }
  section.cv-section:first-of-type { margin-top: 0; }

  h3.subsection-title {
    font-family: var(--serif);
    font-style: italic;
    font-weight: 600;
    font-size: 1.02rem;
    color: var(--accent);
    margin: 1.1rem 0 0.55rem;
  }
  h3.subsection-title:first-of-type { margin-top: 0.2rem; }

  /* ---------- entry rows (position / degree + dates) ---------- */
  .entry-row {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    gap: 1rem;
    margin: 0.15rem 0;
  }
  .entry-title { font-weight: 600; }
  .entry-sub { font-weight: 600; }
  .entry-date {
    font-family: var(--sans);
    font-size: 0.83rem;
    color: var(--muted);
    white-space: nowrap;
  }
  .entry-org {
    font-style: italic;
    color: var(--muted);
    margin: -0.1rem 0 0.4rem;
  }

  /* ---------- generic lists ---------- */
  ul.cv-list {
    margin: 0.3rem 0 0.9rem;
    padding-left: 1.15rem;
  }
  ul.cv-list li { margin-bottom: 0.42rem; }
  ul.cv-list ul { margin: 0.25rem 0 0.25rem; padding-left: 1.1rem; }
  ul.cv-list ul li { margin-bottom: 0.15rem; font-size: 0.96rem; color: var(--muted); }

  ul.tight li { margin-bottom: 0.18rem; }

  /* dense multi-column course list */
  ul.courses {
    columns: 2;
    column-gap: 2.2rem;
    margin: 0.3rem 0 0.9rem;
    padding-left: 1.15rem;
  }
  ul.courses li { margin-bottom: 0.28rem; break-inside: avoid; font-size: 0.97rem; }

  /* ---------- publication list ---------- */
  ol.pub-list {
    list-style: none;
    counter-reset: pub;
    margin: 0.3rem 0 0.9rem;
    padding: 0;
  }
  ol.pub-list li {
    counter-increment: pub;
    position: relative;
    padding-left: 2.15rem;
    margin-bottom: 0.85rem;
    line-height: 1.5;
  }
  ol.pub-list li::before {
    content: "[" counter(pub) "]";
    position: absolute;
    left: 0;
    top: 0;
    font-family: var(--sans);
    font-size: 0.8rem;
    color: var(--accent);
    font-weight: 600;
  }
  .pub-list em { color: var(--muted); }
  .pub-list a.pub-link {
    font-family: var(--sans);
    font-size: 0.78rem;
    color: var(--link);
    text-decoration: none;
    border-bottom: 1px solid var(--accent-soft);
    padding-bottom: 1px;
    white-space: nowrap;
  }
  .pub-list a.pub-link:hover { color: var(--accent); border-color: var(--accent); }

  strong.field { font-weight: 600; }

  p.lead-note {
    font-family: var(--sans);
    font-size: 0.9rem;
    color: var(--muted);
    margin: 0.2rem 0 0.6rem;
  }

  footer.cv-footer {
    margin-top: 2.6rem;
    padding-top: 1rem;
    border-top: 1px solid var(--rule);
    text-align: center;
    font-family: var(--sans);
    font-size: 0.75rem;
    color: var(--muted);
  }

  /* ---------- print button ---------- */
  .print-btn {
    position: fixed;
    top: 22px;
    right: 22px;
    font-family: var(--sans);
    font-size: 0.82rem;
    font-weight: 500;
    background: var(--accent);
    color: #fff;
    border: none;
    padding: 0.6rem 1.05rem;
    border-radius: 3px;
    cursor: pointer;
    letter-spacing: 0.01em;
    box-shadow: 0 6px 16px -6px rgba(138,59,50,0.55);
    transition: transform 0.15s ease, box-shadow 0.15s ease;
  }
  .print-btn:hover { transform: translateY(-1px); box-shadow: 0 10px 20px -6px rgba(138,59,50,0.6); }

  @media (max-width: 700px) {
    .page { padding: 2.1rem 1.3rem 2.6rem; }
    .cv-name { font-size: 1.9rem; }
    ul.courses { columns: 1; }
    .print-btn { top: 12px; right: 12px; padding: 0.5rem 0.85rem; font-size: 0.75rem; }
    .cv-contact .sep { display: block; height: 0; margin: 0; }
    .cv-contact .sep::before { content: ""; }
  }

  @media print {
    .print-btn { display: none; }
    html, body { background: #fff; }
    .page { box-shadow: none; padding: 0; max-width: 100%; }
    a { color: inherit !important; text-decoration: none !important; }
    .pub-list a.pub-link { border-bottom: none; }
  }
</style>
</head>
<body>

<button class="print-btn" onclick="window.print()">Save as PDF</button>

<div class="page">

  <header class="cv-header">
    <h1 class="cv-name">Mark C. Hunnell</h1>
    <div class="cv-title">Professor, Department of Mathematics<br>Winston-Salem State University</div>
    <div class="cv-contact">
      <a href="mailto:hunnellm@wssu.edu">hunnellm@wssu.edu</a>
      <span class="sep">&#124;</span>
      <a href="https://hunnellm.github.io" target="_blank" rel="noopener">hunnellm.github.io</a>
      <span class="sep">&#124;</span>
      2621 Audubon Dr, Winston-Salem, NC 27106
    </div>
  </header>

  <!-- ============================================================ -->
  <section class="cv-section">
    <h2 class="section-title">Education</h2>
    <div class="node-rule" aria-hidden="true">
      <svg preserveAspectRatio="none" viewBox="0 0 100 10"><line x1="0" y1="5" x2="100" y2="5"/><circle cx="2" cy="5" r="2.6"/><circle cx="26" cy="5" r="2.6" class="hollow"/><circle cx="50" cy="5" r="2.6"/><circle cx="74" cy="5" r="2.6" class="hollow"/><circle cx="98" cy="5" r="2.6"/></svg>
    </div>

    <div class="entry-row">
      <span class="entry-sub">North Carolina State University, Raleigh, NC</span>
      <span class="entry-date">August 2005 – May 2015</span>
    </div>

    <ul class="cv-list">
      <li>
        <div class="entry-row"><span class="entry-title">Ph.D. in Mathematics</span><span class="entry-date">May 2015</span></div>
        <ul>
          <li>Dissertation: <em>Orbits of minimal parabolic k-subgroups on symmetric k-varieties</em></li>
          <li>Advisor: A.G. Helminck</li>
        </ul>
      </li>
      <li><div class="entry-row"><span class="entry-title">M.S. in Mathematics</span><span class="entry-date">December 2012</span></div></li>
      <li><div class="entry-row"><span class="entry-title">B.S. in Mathematics</span> <span style="font-weight:400;color:var(--muted)">(Honors Certification, Summa Cum Laude)</span><span class="entry-date">May 2010</span></div></li>
    </ul>
  </section>

  <!-- ============================================================ -->
  <section class="cv-section">
    <h2 class="section-title">Research Experience</h2>
    <div class="node-rule" aria-hidden="true">
      <svg preserveAspectRatio="none" viewBox="0 0 100 10"><line x1="0" y1="5" x2="100" y2="5"/><circle cx="2" cy="5" r="2.6"/><circle cx="26" cy="5" r="2.6" class="hollow"/><circle cx="50" cy="5" r="2.6"/><circle cx="74" cy="5" r="2.6" class="hollow"/><circle cx="98" cy="5" r="2.6"/></svg>
    </div>

    <h3 class="subsection-title">Peer-Reviewed Publications</h3>
    <ol class="pub-list">
      <li>Transmission Zero Forcing (2026), with A. Berliner, C. Bozeman, K. Collins, M. Flagg, and V. Furst. Under review, DGMT. <a class="pub-link" href="https://arxiv.org/abs/2606.22246" target="_blank" rel="noopener">[link]</a></li>
      <li>Zero forcing propagation time intervals and graphs with fixed propagation time (2026), with D. Ferrero, H.T. Hall, and L. Hogben. Accepted, <em>Australasian Journal of Combinatorics</em>. <a class="pub-link" href="https://arxiv.org/abs/2511.16335" target="_blank" rel="noopener">[link]</a></li>
      <li>Fault Tolerant Zero Forcing (2026). Under review. <a class="pub-link" href="https://arxiv.org/abs/2509.07854" target="_blank" rel="noopener">[link]</a></li>
      <li>Reconfiguration of zero forcing sets under the PSD and skew forcing rules (2026). Accepted pending revisions. <a class="pub-link" href="https://arxiv.org/abs/2501.03642" target="_blank" rel="noopener">[link]</a></li>
      <li>The Classification of Graphs on 8 Vertices with Coinciding Zero Forcing Number and Maximum Nullity (2025). <em>Electronic Journal of Linear Algebra</em>, 41 (2025), 643–668. <a class="pub-link" href="https://journals.uwyo.edu/index.php/ela/article/view/9635" target="_blank" rel="noopener">[link]</a></li>
      <li>Topological Symmetry Groups of the Generalized Petersen Graphs (2025), with A. Alvarez, E. Davis, E. Flapan, J. Hutchens, P. Lewis, C. Price, and R. Vanderpool. <em>Algebraic and Geometric Topology</em>. <a class="pub-link" href="https://msp.org/agt/2025/25-8/p13.xhtml" target="_blank" rel="noopener">[link]</a></li>
      <li>New Structures and Their Applications to Variants of Zero Forcing and Propagation Time (2025). <em>Electronic Journal of Combinatorics</em>, 32(2), P2.19. <a class="pub-link" href="https://doi.org/10.37236/12237" target="_blank" rel="noopener">[link]</a></li>
      <li>Fixed Point Groups of Involutions of O(q,k) for a Field of Characteristic 2 (2025), with J. Hutchens. <em>Linear and Multilinear Algebra</em>. <a class="pub-link" href="https://www.tandfonline.com/doi/full/10.1080/03081087.2024.2340743" target="_blank" rel="noopener">[link]</a></li>
      <li>Upper Bounds for Positive Semidefinite Propagation Time (2022). <em>Discrete Mathematics</em>. <a class="pub-link" href="https://doi.org/10.1016/j.disc.2022.112967" target="_blank" rel="noopener">[link]</a></li>
      <li>Orbits of Minimal Parabolic Subgroups Acting on Symmetric k-Varieties Corresponding to k-split Groups (2021). <em>Journal of Algebra and its Applications</em>. <a class="pub-link" href="https://doi.org/10.1142/S0219498821501991" target="_blank" rel="noopener">[link]</a></li>
      <li>On Involutions of Type O(q,k) over a Field of Characteristic Two (2020), with J. Hutchens and N. Schwarz. <em>Linear Algebra and its Applications</em>, Vol. 593, 228–250. <a class="pub-link" href="https://doi.org/10.1016/j.laa.2020.02.006" target="_blank" rel="noopener">[link]</a></li>
      <li>Isomorphy Classes of Finite Order Automorphisms of SL(2,k) (2017), with R.W. Benim and A.K. Sutherland. <em>Communications in Algebra</em>, Vol. 45, No. 12. <a class="pub-link" href="https://doi.org/10.1080/00927872.2017.1298770" target="_blank" rel="noopener">[link]</a></li>
    </ol>

    <h3 class="subsection-title">Manuscripts in Preparation</h3>
    <ul class="cv-list tight">
      <li>The Symplectic Inverse Eigenvalue Problem for a Graph II, with L. Hogben, H. Gupta, B. Shader, and T. Wong.</li>
      <li>Splitting Sets, with R. Davila, H. Schuerger, and B. Small.</li>
      <li>An Asymptotic n/2 Lower Bound for the Maximum Possible Zero-Forcing–Maximum-Nullity Gap, with J. Geneson and J. Sinkovic.</li>
      <li>Broadcast Forcing, with A. Li, M. Ginn, H. Azuibuke, K. Karber, and L. Wong.</li>
      <li>An Exploration of Enhanced Zero Forcing, with M. Flagg, H. Schuerger, and B. Small.</li>
      <li>Machine Learning Applied to the Minimum Rank Problem, with J. Hutchens and K. Urgo.</li>
      <li>Loop Maximum Nullity, with L. Hogben.</li>
    </ul>

    <h3 class="subsection-title">Conference Presentations</h3>
    <ul class="cv-list tight">
      <li>Fault Tolerant Zero Forcing — Joint Mathematics Meetings, Washington, D.C., 2026.</li>
      <li>New Tools for the Minimum Rank Problem for Graphs — Joint Mathematics Meetings, Washington, D.C., 2026.</li>
      <li>Minimum Rank for Small Graphs — Southeast International Conference on Combinatorics, Graph Theory, and Computing, 2025.</li>
      <li>Minimum Rank for Graphs of Order Eight — Joint Mathematics Meetings, Seattle, WA, 2025.</li>
      <li>Fault Tolerant Zero Forcing — WSSU Scholarship Day Departmental Showcase, 2024.</li>
      <li>Reconfiguration for Positive Semidefinite Zero Forcing — Joint Mathematics Meetings, San Francisco, CA, 2024.</li>
      <li>On Involutions of Orthogonal Groups Defined Over a Field of Characteristic 2 — AMS Special Session on Generalizations of Symmetric Spaces, II, Honolulu, HI, 2019.</li>
      <li>Generalized Symmetric k-Varieties Corresponding to Finite Order Automorphisms — Joint Mathematics Meetings Special Session on Lie Group Representations, Discretization, and Gelfand Pairs (MRC Session), I, Atlanta, GA, 2017.</li>
      <li>Generalized Complexification of the Orbits of Parabolic k-Subgroups Acting on Symmetric k-Varieties — MAA General Contributed Paper Session on Research in Algebra, I, San Antonio, TX, 2015.</li>
    </ul>

    <h3 class="subsection-title">External Funding</h3>
    <ul class="cv-list tight">
      <li><strong class="field">PRIMES: Zero Forcing in Graphs and Applications</strong> (2025–2027), $369,599. PI. NSF Award No. 2447261.</li>
      <li><strong class="field">Mosaic Mathematics Research Assistantship Fund</strong> (2024–present), $25,000 annually with renewal.</li>
      <li><strong class="field">UNC Undergraduate Research Award Program: Fault Tolerant Zero Forcing</strong> (2023–2024), $34,997. PI.</li>
    </ul>

    <h3 class="subsection-title">Research Awards</h3>
    <ul class="cv-list tight">
      <li>New Researcher of the Year, Winston-Salem State University, 2025–2026.</li>
      <li>Emerging Researcher of the Year, Winston-Salem State University, 2023–2024.</li>
    </ul>

    <h3 class="subsection-title">Research with Undergraduates</h3>
    <ul class="cv-list tight">
      <li><strong class="field">WSSU Zero Forcing Research Group</strong> (2023–present). Team of four undergraduates conducting ongoing research; funding provided by the Mosaic Fund.</li>
      <li><em>Vertex Fault Tolerant Zero Forcing II</em> — GIRAFFE 2026 Zero Forcing Research Group.</li>
      <li><em>WSSU Zero Forcing Research Group Summer Workshop</em> (2025) — Asher Brown, Za'Kiyah Toomer-Sanders, Sarah Weber. Week-long intensive research workshop funded by a PRIMES award; manuscript under review.</li>
      <li><em>Fault Tolerant Zero Forcing</em> (2024–2025) — Asher Brown, Diana Holman, Amiya Sanford, and ZaKiya Toomer-Sanders. Funded by the Mosaic Mathematics Research Assistantship Fund. Two posters at University Scholarship Day 2025; poster at NAM MathFest 2024.</li>
      <li><em>Fault Tolerant Zero Forcing</em> (2023–2024) — Kyasia Avery, Asher Brown, Diana Holman, Amiya Sanford, and ZaKiya Toomer-Sanders. Funded by the UNC Undergraduate Research Program. Poster at University Scholarship Day 2024; poster at NAM MathFest 2024.</li>
      <li><em>Zero Forcing for Some Families of Graphs</em> (2021–2022) — Dezmen Howard, Galen Mackaronis, Christopher Johnson, Abre'a Curtis, Jenaira Edmonds. Two posters presented at University Scholarship Day 2022.</li>
      <li><em>Generalized Symmetric Spaces for SL(2,k)</em> (2016–2017) — MARC Affiliate Scholar Eric Pridgen.</li>
      <li><em>Finite Order Automorphisms of SL(3)</em> (2015–2016) — MARC Affiliate Scholar Eric Pridgen. Disseminated at ABRCMS 2015 (poster session) and University Scholarship Day, Fall 2016.</li>
      <li><em>An Application of the PageRank Algorithm to a Marketing Problem</em> — Summer Research Fellow Alexus Deese. Presented at the Summer Research Fellows Symposium, WSSU, 2016.</li>
    </ul>

    <h3 class="subsection-title">Conferences Attended with Undergraduates</h3>
    <ul class="cv-list tight">
      <li>Joint Mathematics Meetings, Washington, D.C., 2026. Funded by PRIMES award.</li>
      <li>NAM MathFest, Tennessee State University, 2025. Funded by NAM. <em>Third place, best undergraduate poster presentation: Via Weber.</em></li>
      <li>NAM MathFest, Prairie View A&amp;M, 2024. Funded by NAM.</li>
      <li>AMS Spring Western Sectional Meeting, San Francisco, CA, 2024. Funded by UNC-URPA award.</li>
    </ul>
  </section>

  <!-- ============================================================ -->
  <section class="cv-section">
    <h2 class="section-title">Teaching Experience</h2>
    <div class="node-rule" aria-hidden="true">
      <svg preserveAspectRatio="none" viewBox="0 0 100 10"><line x1="0" y1="5" x2="100" y2="5"/><circle cx="2" cy="5" r="2.6"/><circle cx="26" cy="5" r="2.6" class="hollow"/><circle cx="50" cy="5" r="2.6"/><circle cx="74" cy="5" r="2.6" class="hollow"/><circle cx="98" cy="5" r="2.6"/></svg>
    </div>

    <div class="entry-row"><span class="entry-title">Professor, Winston-Salem State University</span><span class="entry-date">2026 – Present</span></div>
    <div class="entry-row"><span class="entry-title">Associate Professor, Winston-Salem State University</span><span class="entry-date">2021 – 2026</span></div>
    <div class="entry-row"><span class="entry-title">Assistant Professor, Winston-Salem State University</span><span class="entry-date">2015 – 2021</span></div>

    <h3 class="subsection-title">Courses Taught</h3>
    <ul class="courses">
      <li>MAT 4388 — Advanced Linear Algebra</li>
      <li>MAT 4330 — Graph Theory and Applications</li>
      <li>MAT 2326 — Elementary Statistics</li>
      <li>MAT 2321 — Foundations of Modern Mathematics</li>
      <li>MAT 2316 — Linear Algebra</li>
      <li>MAT 2317 — Calculus I</li>
      <li>MAT 2318 — Calculus II</li>
      <li>MAT 3350 — Linear Programming</li>
      <li>MAT 3341 — Algebraic Structures I</li>
      <li>MAT 4342 — Algebraic Structures II</li>
      <li>MAT 4330 — Directed Study Seminar: Linear Algebra II</li>
      <li>MAT 4330 — Directed Study Seminar: Graph Theory</li>
      <li>MAT 4388 — Senior Seminar II</li>
      <li>MAT 1312 — Precalculus Mathematics I</li>
    </ul>

    <h3 class="subsection-title">Teaching Awards</h3>
    <ul class="cv-list tight">
      <li>John Patterson Master Teaching Award, May 2025</li>
      <li>John Patterson Master Teaching Award, May 2019</li>
      <li>Maltbie Award Finalist, NCSU, March 2015</li>
      <li>Outstanding Teaching Assistant, NCSU, March 2015</li>
    </ul>
  </section>

  <!-- ============================================================ -->
  <section class="cv-section">
    <h2 class="section-title">Service Experience</h2>
    <div class="node-rule" aria-hidden="true">
      <svg preserveAspectRatio="none" viewBox="0 0 100 10"><line x1="0" y1="5" x2="100" y2="5"/><circle cx="2" cy="5" r="2.6"/><circle cx="26" cy="5" r="2.6" class="hollow"/><circle cx="50" cy="5" r="2.6"/><circle cx="74" cy="5" r="2.6" class="hollow"/><circle cx="98" cy="5" r="2.6"/></svg>
    </div>

    <h3 class="subsection-title">University and College</h3>
    <ul class="cv-list tight">
      <li>Academic Program Review Committee (2025–2026)</li>
      <li>Faculty Senate Committee for Tenure, Promotion, and Academic Freedom (2023–2024)</li>
      <li>CASE Academic Restructuring Subcommittee (2024)</li>
      <li>General Education Implementation Committee (2023–2024)</li>
      <li>Committee for Faculty Hearing on Discharge and Non-reappointment (2022–present)</li>
      <li>Quality Enhancement Plan Course Representative (2019–2021)</li>
      <li>Chair, Faculty Senate Bylaws Committee (2019–2021)</li>
      <li>Faculty Senate Delegate (2018–2024)</li>
      <li>Title IX Hearing Committee (2019–present)</li>
      <li>Nominating Committee of the Faculty Senate (2018)</li>
      <li>Dean Search Committee, College of Arts, Sciences, Business, and Education — Member (2017–2018)</li>
      <li>Sexual Misconduct Hearing Panel — Member (2018–present)</li>
      <li>Academic Standards and Curriculum Committee — Alternate (2015–2018)</li>
      <li>Committee to Rethink Critical Thinking — Member (2016–2017)</li>
      <li>Reimagining the First Year (RFY) Committee (2016–2017)</li>
      <li>Student Success Symposium — Delegate (2016)</li>
      <li>Indirect Cost Policy Review Committee — Member (2016)</li>
      <li>Strategic Planning Committee, Goal 1 Objective 2 — Member (2015–2016)</li>
    </ul>

    <h3 class="subsection-title">Department</h3>
    <ul class="cv-list tight">
      <li>Co-Chair, Faculty Bylaws Committee</li>
      <li>Chair, Faculty Search Committee (2024–2025)</li>
      <li>Chair, Policies and Procedures Working Group (2023–present)</li>
      <li>Course Coordinator, MAT 2326 Elementary Statistics (2018–2024)</li>
      <li>Committee to Review Tenure and Promotion Guidelines (2019–2020)</li>
      <li>Curricular Coherence Committee (2018–2019)</li>
      <li>Quality Matters Course Review — Course Representative (2018)</li>
      <li>Committee to Review Departmental Curriculum — Member (2016–2017)</li>
      <li>Co-Course Coordinator, MAT 2326 Elementary Statistics (2016–2017)</li>
      <li>Faculty Liaison to the Center for Excellence in Teaching and Learning (CETL) (2015–2017)</li>
    </ul>

    <h3 class="subsection-title">Community and Professional</h3>
    <ul class="cv-list tight">
      <li>Local Organizing Committee, NAM MathFest, 2027</li>
      <li>Session Organizer, IEPG-ZF ARC, Joint Mathematics Meetings, 2027</li>
      <li>Session Organizer, Graphs and Matrices, Southeast International Conference on Combinatorics, Graph Theory, and Computing, 2027</li>
      <li>Project Leader, Research Experience for Undergraduate Faculty (REUF), 2026</li>
      <li>Lead Organizer, GIRAFFE Workshop (2026–present)</li>
      <li>Session Organizer, Graphs and Matrices, Southeast International Conference on Combinatorics, Graph Theory, and Computing, 2026</li>
      <li>Co-Organizer, AIM Research Community — Inverse Eigenvalue Problem for Graphs (2025–present)</li>
      <li>CUR National Conference Advisory Committee Member (2025–present)</li>
      <li>Professional Organization Member: AMS, MAA, SIAM, NAM, CUR</li>
      <li>Mathematical Reviews Reviewer, No. 152463</li>
      <li>Elementary Mathematics Invitational Speaker, <em>What Does a Mathematician Do All Day?</em> (2019)</li>
      <li>Elementary Mathematics Invitational — Activity Design Committee and Facilitator (2019)</li>
      <li>Elementary Mathematics Invitational Speaker, <em>Mathematics in the Modern World</em> (2018)</li>
      <li>ACT Preparatory Workshop, Carver High School — Volunteer, Mathematics Section Preparation (2015–2019)</li>
      <li>Symmetric Spaces and Their Generalizations in Honor of A.G. Helminck on the Occasion of His 60th Birthday — Session Chair (2014)</li>
    </ul>
  </section>

  <footer class="cv-footer">Mark C. Hunnell &middot; Curriculum Vitae &middot; Updated August 2026</footer>

</div>
</body>
</html>
