<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Tharun Mula | Data Analyst Portfolio</title>

  <!-- Bootstrap CSS (CDN) -->
  <link
    href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
    rel="stylesheet"
    integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH"
    crossorigin="anonymous"
  />

  <style>
    :root{
      --bg: #0b1220;
      --card: rgba(255,255,255,0.06);
      --border: rgba(255,255,255,0.12);
      --text: rgba(255,255,255,0.90);
      --muted: rgba(255,255,255,0.70);
      --accent: #7c3aed; /* purple */
      --accent2: #22c55e; /* green */
      --shadow: 0 10px 30px rgba(0,0,0,0.35);
      --radius: 18px;
    }

    body{
      background:
        radial-gradient(900px 500px at 15% 10%, rgba(124,58,237,0.25), transparent 60%),
        radial-gradient(900px 500px at 85% 30%, rgba(34,197,94,0.18), transparent 55%),
        radial-gradient(900px 500px at 50% 95%, rgba(59,130,246,0.12), transparent 60%),
        var(--bg);
      color: var(--text);
      font-family: system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, "Apple Color Emoji", "Segoe UI Emoji";
      line-height: 1.55;
    }

    a{ color: #c4b5fd; text-decoration: none; }
    a:hover{ text-decoration: underline; }

    /* Navbar */
    .navbar{
      backdrop-filter: blur(10px);
      background: rgba(11,18,32,0.65);
      border-bottom: 1px solid var(--border);
    }
    .brand-dot{
      width: 10px; height: 10px; border-radius: 999px;
      background: linear-gradient(135deg, var(--accent), #60a5fa);
      display: inline-block;
      box-shadow: 0 0 0 4px rgba(124,58,237,0.15);
    }

    /* Hero */
    .hero{
      padding: 5rem 0 2.25rem;
    }
    .hero-card{
      background: linear-gradient(180deg, rgba(255,255,255,0.08), rgba(255,255,255,0.04));
      border: 1px solid var(--border);
      border-radius: calc(var(--radius) + 8px);
      box-shadow: var(--shadow);
      overflow: hidden;
      position: relative;
    }
    .hero-card::before{
      content:"";
      position:absolute; inset:0;
      background:
        radial-gradient(700px 250px at 10% 10%, rgba(124,58,237,0.35), transparent 60%),
        radial-gradient(700px 250px at 90% 30%, rgba(34,197,94,0.22), transparent 55%);
      opacity: 0.9;
      pointer-events:none;
    }
    .hero-card > .card-body{ position: relative; }

    .badge-soft{
      background: rgba(124,58,237,0.16);
      border: 1px solid rgba(124,58,237,0.35);
      color: #e9d5ff;
      font-weight: 600;
    }

    /* Sections + cards */
    .section{
      padding: 1.75rem 0;
    }
    .section-title{
      display:flex; align-items:center; gap:.6rem;
      margin-bottom: 1rem;
    }
    .section-title h2{
      font-size: 1.35rem;
      margin: 0;
      letter-spacing: 0.2px;
    }
    .section-title .line{
      flex:1;
      height: 1px;
      background: linear-gradient(90deg, rgba(255,255,255,0.18), transparent);
    }

    .glass-card{
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      box-shadow: 0 6px 20px rgba(0,0,0,0.22);
    }

    .muted{ color: var(--muted); }
    .pill{
      display:inline-flex; align-items:center; gap:.45rem;
      padding: .35rem .7rem;
      border-radius: 999px;
      background: rgba(255,255,255,0.07);
      border: 1px solid rgba(255,255,255,0.12);
      margin: .25rem .35rem 0 0;
      font-size: 0.9rem;
    }
    .pill .dot{
      width: 7px; height: 7px; border-radius: 999px;
      background: rgba(255,255,255,0.55);
    }

    .meta{
      font-size: 0.95rem;
      color: var(--muted);
    }

    .list-tight li{ margin-bottom: .5rem; }

    /* Timeline-ish left border */
    .accent-border{
      border-left: 3px solid rgba(124,58,237,0.7);
      padding-left: 1rem;
    }

    /* Footer */
    footer{
      padding: 2.5rem 0 3rem;
      color: var(--muted);
    }
    .footer-card{
      border-radius: var(--radius);
      border: 1px solid var(--border);
      background: rgba(255,255,255,0.04);
    }

    /* Small tweaks */
    .btn-accent{
      background: linear-gradient(135deg, var(--accent), #2563eb);
      border: none;
      color: #fff;
      font-weight: 600;
      box-shadow: 0 10px 25px rgba(124,58,237,0.25);
    }
    .btn-accent:hover{
      filter: brightness(1.05);
      color: #fff;
    }
    .btn-outline-glass{
      border: 1px solid rgba(255,255,255,0.18);
      color: #fff;
      background: rgba(255,255,255,0.04);
    }
    .btn-outline-glass:hover{
      background: rgba(255,255,255,0.08);
      color: #fff;
    }
  </style>
</head>

<body data-bs-spy="scroll" data-bs-target="#topNav" data-bs-smooth-scroll="true" tabindex="0">

  <!-- Navbar -->
  <nav id="topNav" class="navbar navbar-expand-lg navbar-dark sticky-top">
    <div class="container">
      <a class="navbar-brand d-flex align-items-center gap-2" href="#top">
        <span class="brand-dot"></span>
        <span class="fw-semibold">Tharun Mula</span>
        <span class="text-white-50 d-none d-sm-inline">| Data Analyst</span>
      </a>

      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navLinks">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navLinks">
        <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
          <li class="nav-item"><a class="nav-link" href="#about">About</a></li>
          <li class="nav-item"><a class="nav-link" href="#skills">Skills</a></li>
          <li class="nav-item"><a class="nav-link" href="#experience">Experience</a></li>
          <li class="nav-item"><a class="nav-link" href="#projects">Projects</a></li>
          <li class="nav-item"><a class="nav-link" href="#education">Education</a></li>
          <li class="nav-item"><a class="nav-link" href="#certifications">Certifications</a></li>
          <li class="nav-item"><a class="nav-link" href="#contact">Contact</a></li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- Hero -->
  <header id="top" class="hero">
    <div class="container">
      <div class="hero-card">
        <div class="card-body p-4 p-md-5">
          <div class="d-flex flex-column flex-lg-row gap-4 align-items-start align-items-lg-center justify-content-between">
            <div>
              <span class="badge badge-soft rounded-pill px-3 py-2 mb-3">Entry-level → Junior Data Analyst</span>
              <h1 class="display-6 fw-bold mb-2">Turning messy data into clear decisions.</h1>
              <p class="muted mb-3" style="max-width: 900px;">
                I am a Data Analyst with hands-on experience in data analytics, business intelligence, and dashboard development.
                Strong technical foundation in <strong>Python, SQL, Tableau, Excel, and Power BI</strong>. Experienced with real-world datasets
                across healthcare, sales, marketing, and operations—building dashboards, predictive models, and structured reports.
              </p>

              <div class="d-flex flex-wrap gap-2">
                <a class="btn btn-accent px-4" href="#projects">View Projects</a>
                <a class="btn btn-outline-glass px-4" href="#contact">Contact</a>
              </div>
            </div>

            <div class="glass-card p-3 p-md-4" style="min-width: 280px;">
              <div class="d-flex justify-content-between">
                <div>
                  <div class="meta">Location</div>
                  <div class="fw-semibold">Leicester, UK</div>
                </div>
                <div class="text-end">
                  <div class="meta">Work Status</div>
                  <div class="fw-semibold">Full Working Rights</div>
                </div>
              </div>
              <hr class="border-white border-opacity-10 my-3" />
              <div class="meta mb-2">Core stack</div>
              <div class="d-flex flex-wrap">
                <span class="pill"><span class="dot"></span>Python</span>
                <span class="pill"><span class="dot"></span>SQL</span>
                <span class="pill"><span class="dot"></span>Tableau</span>
                <span class="pill"><span class="dot"></span>Excel</span>
                <span class="pill"><span class="dot"></span>Power BI</span>
              </div>
            </div>

          </div>
        </div>
      </div>
    </div>
  </header>

  <main>
    <!-- About -->
    <section id="about" class="section">
      <div class="container">
        <div class="section-title">
          <h2>👋 About Me</h2><span class="line"></span>
        </div>

        <div class="glass-card p-4 p-md-5">
          <p class="mb-3">
            I am a Data Analyst with hands-on experience in data analytics, business intelligence, and dashboard development.
            I have professional exposure through a data analytics internship and a strong technical background in Python, SQL,
            Tableau, Excel, and Power BI.
          </p>
          <p class="mb-3">
            I have worked on real-world datasets across healthcare, sales, marketing, and operations, building dashboards,
            predictive models, and structured reports to support data-driven decision-making. With a foundation in software
            development and enterprise applications, I bring both analytical thinking and technical execution to analytics problems.
          </p>
          <p class="mb-0">
            I am actively seeking entry-level to junior data analyst roles where I can contribute to impactful, data-centric projects.
          </p>
        </div>
      </div>
    </section>

    <!-- Skills -->
    <section id="skills" class="section">
      <div class="container">
        <div class="section-title">
          <h2>🧠 Skills</h2><span class="line"></span>
        </div>

        <div class="row g-4">
          <div class="col-lg-4">
            <div class="glass-card p-4 h-100">
              <h3 class="h5 fw-semibold mb-3">Tools &amp; Technologies</h3>
              <div class="d-flex flex-wrap">
                <span class="pill"><span class="dot"></span>Python</span>
                <span class="pill"><span class="dot"></span>SQL</span>
                <span class="pill"><span class="dot"></span>Tableau</span>
                <span class="pill"><span class="dot"></span>Excel</span>
                <span class="pill"><span class="dot"></span>Power BI</span>
              </div>
            </div>
          </div>

          <div class="col-lg-4">
            <div class="glass-card p-4 h-100">
              <h3 class="h5 fw-semibold mb-3">Analytics &amp; Processes</h3>
              <ul class="list-unstyled list-tight mb-0">
                <li>Data Analysis &amp; Visualization</li>
                <li>Dashboard Creation &amp; Reporting</li>
                <li>Data Extraction &amp; Manipulation</li>
                <li>Statistical Analysis &amp; Data Modeling</li>
                <li>Data Accuracy &amp; Integrity Management</li>
              </ul>
            </div>
          </div>

          <div class="col-lg-4">
            <div class="glass-card p-4 h-100">
              <h3 class="h5 fw-semibold mb-3">Soft Skills</h3>
              <ul class="list-unstyled list-tight mb-0">
                <li>Attention to Detail</li>
                <li>Cross-Functional Communication</li>
                <li>Team Collaboration</li>
                <li>Problem Solving</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Experience -->
    <section id="experience" class="section">
      <div class="container">
        <div class="section-title">
          <h2>💼 Experience</h2><span class="line"></span>
        </div>

        <div class="row g-4">
          <div class="col-lg-6">
            <div class="glass-card p-4 h-100 accent-border">
              <div class="d-flex justify-content-between flex-wrap gap-2">
                <h3 class="h5 fw-semibold mb-0">Junior Data Analyst (Intern)</h3>
                <span class="meta">May 2025 – Present</span>
              </div>
              <div class="meta mb-3">Fortray Global Services Ltd, London, UK</div>
              <ul class="list-tight mb-0">
                <li>Built interactive dashboards using Tableau and Excel for sales, marketing, and operations.</li>
                <li>Performed SQL-based analysis to extract insights and generate structured reports.</li>
                <li>Developed predictive models in Python to estimate medical insurance costs (+25% accuracy).</li>
                <li>Led dashboard development for a Marketing Analytics capstone project (+40% reporting speed).</li>
                <li>Worked in Agile sprints and stakeholder reviews to track deliverables.</li>
              </ul>
            </div>
          </div>

          <div class="col-lg-6">
            <div class="glass-card p-4 h-100 accent-border" style="border-left-color: rgba(34,197,94,0.7);">
              <div class="d-flex justify-content-between flex-wrap gap-2">
                <h3 class="h5 fw-semibold mb-0">Software Developer &amp; Unqork Configurator</h3>
                <span class="meta">May 2021 – Jul 2023</span>
              </div>
              <div class="meta mb-3">Integra Solutions, India</div>
              <ul class="list-tight mb-0">
                <li>Built and maintained 6 enterprise applications for finance/insurance clients.</li>
                <li>Created automated reporting scripts with SQL and Python to improve data flow accuracy.</li>
                <li>Integrated DocuSign and ARTMS APIs, reducing verification time by 40%.</li>
                <li>Optimized SQL queries, improving retrieval performance by 50%.</li>
                <li>Collaborated across teams to deliver custom dashboards and support users under tight deadlines.</li>
              </ul>
            </div>
          </div>
        </div>

      </div>
    </section>

    <!-- Projects -->
    <section id="projects" class="section">
      <div class="container">
        <div class="section-title">
          <h2>📁 Projects</h2><span class="line"></span>
        </div>

        <div class="row g-4">
          <div class="col-lg-4">
            <div class="glass-card p-4 h-100">
              <h3 class="h5 fw-semibold mb-2">❤️ Heart Attack Prediction &amp; Risk Analysis</h3>
              <div class="meta mb-3"><strong>Tools:</strong> Python, SQL, Tableau</div>
              <p class="mb-2"><strong>Objective:</strong> Identify high-risk patients and predict heart attack likelihood.</p>
              <ul class="list-tight">
                <li>Cleaned and analyzed 4,000+ patient records.</li>
                <li>Identified key risk factors.</li>
                <li>Built logistic regression model (84% accuracy).</li>
                <li>Created Tableau dashboards for risk distribution.</li>
              </ul>
              <p class="mb-0"><strong>Impact:</strong> Clarified risk drivers to support preventive strategy and prioritization.</p>
            </div>
          </div>

          <div class="col-lg-4">
            <div class="glass-card p-4 h-100">
              <h3 class="h5 fw-semibold mb-2">🍽️ Restaurant Recommendation &amp; Rating Analysis</h3>
              <div class="meta mb-3"><strong>Tools:</strong> Python, SQL, Tableau, Excel</div>
              <p class="mb-2"><strong>Objective:</strong> Improve customer recommendations and business decisions.</p>
              <ul class="list-tight">
                <li>Processed/validated 50,000+ records across 20 countries.</li>
                <li>Improved data quality via duplicate removal and validation.</li>
                <li>Built dashboards for customer behavior and insights.</li>
              </ul>
              <p class="mb-0"><strong>Impact:</strong> Improved recommendation accuracy and strategic decision-making.</p>
            </div>
          </div>

          <div class="col-lg-4">
            <div class="glass-card p-4 h-100">
              <h3 class="h5 fw-semibold mb-2">📈 Regional Sales Comparison Dashboard</h3>
              <div class="meta mb-3"><strong>Tools:</strong> Tableau</div>
              <p class="mb-2"><strong>Objective:</strong> Compare and visualize sales performance between two regions.</p>
              <ul class="list-tight">
                <li>Designed an interactive Tableau dashboard.</li>
                <li>Implemented dynamic filters for time and region comparison.</li>
              </ul>
              <p class="mb-0"><strong>Impact:</strong> Supported regional sales strategy and performance optimization.</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Education -->
    <section id="education" class="section">
      <div class="container">
        <div class="section-title">
          <h2>🎓 Education</h2><span class="line"></span>
        </div>

        <div class="glass-card p-4 p-md-5">
          <div class="row g-4">
            <div class="col-md-6">
              <h3 class="h5 fw-semibold mb-1">Master of Business Administration (MBA)</h3>
              <div class="meta">University of East London, United Kingdom</div>
              <div class="meta">Oct 2023 – Dec 2024</div>
            </div>
            <div class="col-md-6">
              <h3 class="h5 fw-semibold mb-1">Bachelor of Technology (B.Tech)</h3>
              <div class="meta">CMR College of Engineering &amp; Technology, India</div>
              <div class="meta">Aug 2016 – Sep 2020</div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Certifications -->
    <section id="certifications" class="section">
      <div class="container">
        <div class="section-title">
          <h2>📜 Training &amp; Certifications</h2><span class="line"></span>
        </div>

        <div class="glass-card p-4 p-md-5">
          <ul class="list-tight mb-0">
            <li>Business Analytics with Excel (Training)</li>
            <li>PC DA – Industry Master Class in Data Analytics – Simplilearn</li>
            <li>Programming Basics and Data Analytics with Python</li>
            <li>SQL Training</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- Contact -->
    <section id="contact" class="section">
      <div class="container">
        <div class="section-title">
          <h2>📬 Contact</h2><span class="line"></span>
        </div>

        <div class="glass-card p-4 p-md-5">
          <div class="row g-3">
            <div class="col-md-6">
              <div class="meta mb-1">Email</div>
              <div class="fw-semibold">
                <a href="mailto:mulatharun45@gmail.com">mulatharun45@gmail.com</a>
              </div>
            </div>

            <div class="col-md-6">
              <div class="meta mb-1">LinkedIn</div>
              <div class="fw-semibold">
                <a href="http://www.linkedin.com/in/tharun-mula-data-anayst" target="_blank" rel="noreferrer">
                  linkedin.com/in/tharun-mula-data-anayst
                </a>
              </div>
            </div>

            <div class="col-md-6">
              <div class="meta mb-1">GitHub</div>
              <div class="fw-semibold">
                <a href="https://github.com/TharunMula" target="_blank" rel="noreferrer">
                  github.com/TharunMula
                </a>
              </div>
            </div>

            <div class="col-md-6">
              <div class="meta mb-1">Location</div>
              <div class="fw-semibold">Leicester, UK</div>
            </div>

            <div class="col-12">
              <div class="meta mb-1">Work Status</div>
              <div class="fw-semibold">Full Working Rights (UK)</div>
            </div>
          </div>
        </div>
      </div>
    </section>

  </main>

  <footer>
    <div class="container">
      <div class="footer-card p-4 d-flex flex-column flex-md-row justify-content-between align-items-start gap-2">
        <div>
          <div class="fw-semibold">Tharun Mula</div>
          <div class="muted">Data Analyst • Python • SQL • Tableau</div>
        </div>
        <div class="muted">© <span id="year"></span></div>
      </div>
    </div>
  </footer>

  <!-- Bootstrap JS -->
  <script
    src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
    integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
    crossorigin="anonymous"
  ></script>

  <script>
    document.getElementById("year").textContent = new Date().getFullYear();
  </script>
</body>
</html>
