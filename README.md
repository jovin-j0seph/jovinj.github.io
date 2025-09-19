# jovinj.github.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Jovin Joseph | AI & Data Science Student</title>
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"
    />
    <style>
      :root {
        --vs-dark: #1e1e1e;
        --vs-blue: #007acc;
        --vs-light-blue: #4fc1ff;
        --vs-green: #4ec9b0;
        --vs-purple: #c586c0;
        --vs-yellow: #dcdcaa;
        --vs-comment: #6a9955;
        --vs-foreground: #d4d4d4;
        --vs-background: #1e1e1e;
        --vs-accent: #569cd6;
      }

      * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: "Consolas", "Monaco", "Courier New", monospace;
      }

      body {
        background-color: var(--vs-background);
        color: var(--vs-foreground);
        line-height: 1.6;
        overflow-x: hidden;
      }

      .container {
        width: 90%;
        max-width: 1200px;
        margin: 0 auto;
        padding: 20px;
      }

      /* Header Styles */
      header {
        background-color: var(--vs-dark);
        padding: 20px 0;
        border-bottom: 1px solid #3c3c3c;
        position: sticky;
        top: 0;
        z-index: 100;
      }

      .header-container {
        display: flex;
        justify-content: space-between;
        align-items: center;
      }

      .logo {
        color: var(--vs-light-blue);
        font-size: 24px;
        font-weight: bold;
        user-select: none;
      }

      nav ul {
        display: flex;
        list-style: none;
        gap: 20px;
      }

      nav a {
        color: var(--vs-foreground);
        text-decoration: none;
        padding: 5px 10px;
        border-radius: 4px;
        transition: color 0.3s, background-color 0.3s;
      }

      nav a:hover {
        color: var(--vs-light-blue);
        background-color: rgba(255, 255, 255, 0.1);
      }

      /* Hero Section */
      .hero {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        height: 80vh;
        text-align: center;
        padding: 40px 0;
        background: linear-gradient(135deg, var(--vs-dark) 0%, #252526 100%);
      }

      .hero h1 {
        font-size: 48px;
        margin-bottom: 20px;
        color: var(--vs-light-blue);
      }

      .hero h2 {
        font-size: 24px;
        margin-bottom: 30px;
        color: var(--vs-green);
      }

      .hero-code {
        background-color: rgba(30, 30, 30, 0.8);
        border: 1px solid #3c3c3c;
        border-radius: 8px;
        padding: 20px;
        margin: 20px 0;
        text-align: left;
        max-width: 600px;
        width: 100%;
      }

      .code-line {
        margin: 5px 0;
      }

      .code-comment {
        color: var(--vs-comment);
      }

      .code-function {
        color: var(--vs-purple);
      }

      .code-string {
        color: var(--vs-yellow);
      }

      .btn {
        display: inline-block;
        background-color: var(--vs-blue);
        color: white;
        padding: 12px 24px;
        border-radius: 4px;
        text-decoration: none;
        font-weight: bold;
        margin-top: 30px;
        transition: background-color 0.3s;
        cursor: pointer;
        border: none;
      }

      .btn:hover {
        background-color: var(--vs-light-blue);
      }

      /* Section Styles */
      section {
        padding: 80px 0;
      }

      section h2 {
        font-size: 36px;
        margin-bottom: 40px;
        color: var(--vs-light-blue);
        text-align: center;
      }

      .section-divider {
        height: 2px;
        background: linear-gradient(90deg, transparent, var(--vs-blue), transparent);
        margin: 20px 0 40px;
      }

      /* About Section */
      .about-content {
        display: grid;
        grid-template-columns: 1fr;
        gap: 40px;
        align-items: center;
      }

      .about-text p {
        margin-bottom: 20px;
        font-size: 18px;
      }

      /* Education Section */
      .education-item {
        background-color: #252526;
        border-radius: 8px;
        padding: 30px;
        margin-bottom: 30px;
        border-left: 4px solid var(--vs-blue);
      }

      .education-item h3 {
        color: var(--vs-light-blue);
        margin-bottom: 10px;
      }

      .education-detail {
        color: var(--vs-green);
        margin-bottom: 15px;
        font-size: 18px;
      }

      .education-description {
        color: var(--vs-foreground);
      }

      /* Skills Section */
      .skills-grid {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
        gap: 30px;
      }

      .skill-category {
        background-color: #252526;
        border-radius: 8px;
        padding: 30px;
        border: 1px solid #3c3c3c;
      }

      .skill-category h3 {
        color: var(--vs-purple);
        margin-bottom: 20px;
        font-size: 24px;
      }

      .skill-item {
        margin-bottom: 15px;
      }

      .skill-name {
        display: flex;
        justify-content: space-between;
        margin-bottom: 5px;
      }

      .skill-bar {
        height: 10px;
        background-color: #3c3c3c;
        border-radius: 5px;
        overflow: hidden;
      }

      .skill-progress {
        height: 100%;
        background-color: var(--vs-blue);
        border-radius: 5px;
      }

      /* Projects Section */
      .projects-grid {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
        gap: 30px;
      }

      .project-card {
        background-color: #252526;
        border-radius: 8px;
        overflow: hidden;
        border: 1px solid #3c3c3c;
        transition: transform 0.3s;
      }

      .project-card:hover {
        transform: translateY(-5px);
      }

      .project-image {
        height: 200px;
        background-color: #1e1e1e;
        display: flex;
        align-items: center;
        justify-content: center;
        color: var(--vs-comment);
        font-size: 48px;
      }

      .project-content {
        padding: 20px;
      }

      .project-content h3 {
        color: var(--vs-yellow);
        margin-bottom: 10px;
      }

      .project-tags {
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
        margin: 15px 0;
      }

      .project-tag {
        background-color: var(--vs-dark);
        color: var(--vs-light-blue);
        padding: 5px 10px;
        border-radius: 4px;
        font-size: 14px;
      }


      .form-group {
        margin-bottom: 20px;
      }

      .form-group label {
        display: block;
        margin-bottom: 8px;
        color: var(--vs-foreground);
      }

      .form-group input,
      .form-group textarea {
        width: 100%;
        padding: 12px;
        background-color: #1e1e1e;
        border: 1px solid #3c3c3c;
        border-radius: 4px;
        color: var(--vs-foreground);
      }

      .form-group textarea {
        min-height: 120px;
        resize: vertical;
      }

      /* Footer */
      footer {
        background-color: var(--vs-dark);
        padding: 40px 0;
        text-align: center;
        border-top: 1px solid #3c3c3c;
      }

      .social-links {
        display: flex;
        justify-content: center;
        gap: 20px;
        margin-bottom: 30px;
      }

      .social-link {
        color: var(--vs-foreground);
        font-size: 24px;
        transition: color 0.3s;
      }

      .social-link:hover {
        color: var(--vs-blue);
      }

      .copyright {
        color: var(--vs-comment);
      }

      /* Responsive Design */
      @media (max-width: 900px) {
        .about-content,
        .contact-content {
          grid-template-columns: 1fr;
        }

        .hero h1 {
          font-size: 36px;
        }

        .hero h2 {
          font-size: 20px;
        }
      }

      @media (max-width: 600px) {
        .header-container {
          flex-direction: column;
          gap: 15px;
        }

        nav ul {
          flex-wrap: wrap;
          justify-content: center;
        }

        .skills-grid,
        .projects-grid {
          grid-template-columns: 1fr;
        }

        .hero {
          height: auto;
          padding: 60px 0;
        }
      }
    </style>
  </head>
  <body>
    <!-- Header -->
    <header>
      <div class="container header-container">
        <div class="logo">Jovin Joseph</div>
        <nav>
          <ul>
            <li><a href="#about">About</a></li>
            <li><a href="#education">Education</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#projects">Projects</a></li>
          </ul>
        </nav>
      </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
      <h1>Hello, World!</h1>
      <h2>I'm a BTech AI & Data Science Student</h2>

      <div class="hero-code">
        <div class="code-line">
          <span class="code-function">print</span>(
          <span class="code-string">"Welcome to my portfolio"</span>)
        </div>
        <div class="code-line">
          <span class="code-comment"># Passionate about AI, ML and coding</span>
        </div>
        <div class="code-line"><span class="code-function">while</span> True:</div>
        <div class="code-line">&nbsp;&nbsp;<span class="code-function">learn</span>()</div>
        <div class="code-line">&nbsp;&nbsp;<span class="code-function">code</span>()</div>
        <div class="code-line">&nbsp;&nbsp;<span class="code-function">create</span>()</div>
      </div>

      <a href="#about" class="btn">Explore My Journey</a>
    </section>

    <!-- About Section -->
    <section id="about">
      <div class="container">
        <h2>About Me</h2>
        <div class="section-divider"></div>

        <div class="about-content">
          <div class="about-text">
            <p>
              I'm a first-year BTech student specializing in Artificial
              Intelligence and Data Science at Rajagiri School of Engineering
              and Technology.
            </p>
            <p>
              My passion for technology began when I wrote my first line of
              code, and since then I've been fascinated by how we can use
              programming to solve real-world problems.
            </p>
            <p>
              I'm particularly interested in machine learning algorithms, data
              visualization, and building intelligent systems that can learn and
              adapt.
            </p>
            <p>
              When I'm not coding, you can find me reading about the latest tech
              advancements, participating in hackathons, or exploring new
              programming paradigms.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Education Section -->
    <section id="education">
      <div class="container">
        <h2>Education</h2>
        <div class="section-divider"></div>

        <div class="education-item">
          <h3>SH CMI Public School</h3>
          <div class="education-detail">High School</div>
          <p class="education-description">
            Completed my schooling at SH CMI Public School, building a strong foundation in academics and extracurriculars.
          </p>
        </div>

        <div class="education-item">
          <h3>Rajagiri School of Engineering and Technology</h3>
          <div class="education-detail">BTech in Artificial Intelligence & Data Science</div>
          <div class="education-detail">2023 - Present</div>
          <p class="education-description">
            Currently in my first year, learning the fundamentals of programming,
            mathematics, and data structures while exploring the exciting fields
            of AI and machine learning.
          </p>
        </div>

        <div class="education-item">
          <h3>Relevant Coursework</h3>
          <p class="education-description">
            Programming in Python, C Programming, Data Structures, Mathematics for AI,
            Statistics, Database Management Systems, and Introduction to Machine Learning.
          </p>
        </div>
      </div>
    </section>

    <!-- Skills Section -->
    <section id="skills">
      <div class="container">
        <h2>Skills</h2>
        <div class="section-divider"></div>

        <div class="skills-grid">
          <div class="skill-category">
            <h3>Programming Languages</h3>

            <div class="skill-item">
              <div class="skill-name">
                <span>Python</span>
                <span>85%</span>
              </div>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 85%"></div>
              </div>
            </div>

            <div class="skill-item">
              <div class="skill-name">
                <span>C Programming</span>
                <span>70%</span>
              </div>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 70%"></div>
              </div>
            </div>
          </div>

          <div class="skill-category">
            <h3>Tools & Technologies</h3>

            <div class="skill-item">
              <div class="skill-name">
                <span>VS Code</span>
                <span>90%</span>
              </div>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 90%"></div>
              </div>
            </div>

            <div class="skill-item">
              <div class="skill-name">
                <span>Git & GitHub</span>
                <span>75%</span>
              </div>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 75%"></div>
              </div>
            </div>

            <div class="skill-item">
              <div class="skill-name">
                <span>Jupyter Notebooks</span>
                <span>85%</span>
              </div>
              <div class="skill-bar">
                <div class="skill-progress" style="width: 85%"></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
      <div class="container">
        <div class="projects-grid">
          <div class="project-card">
            <div class="project-image">
              <i class="fas fa-chart-line"></i>
            </div>
            <div class="project-content">
            
