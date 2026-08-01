<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Android Dev Portfolio</title>
  <!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  <!-- Lucide Icons -->
  <script src="https://unpkg.com/lucide@latest"></script>
  
  <style>
    /* RESET & BASE STYLES */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
    }

    :root {
      --bg-dark: #0a0c0e;
      --bg-card: #121518;
      --bg-input: #1a1e23;
      --border-color: #22272e;
      --text-main: #e6edf3;
      --text-muted: #8b949e;
      --accent-green: #2ecc71;
      --accent-green-hover: #27ae60;
      --accent-green-glow: rgba(46, 204, 113, 0.15);
    }

    body {
      background-color: var(--bg-dark);
      color: var(--text-main);
      line-height: 1.6;
      padding-bottom: 60px;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    /* CONTAINER */
    .container {
      max-width: 1100px;
      margin: 0 auto;
      padding: 0 24px;
    }

    /* HEADER & NAV */
    header {
      padding: 24px 0;
      border-bottom: 1px solid rgba(255, 255, 255, 0.05);
    }

    .nav-container {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      color: var(--accent-green);
      font-weight: 700;
      font-size: 1.1rem;
    }

    .nav-links {
      display: flex;
      gap: 24px;
      align-items: center;
      list-style: none;
    }

    .nav-links a {
      color: var(--text-muted);
      font-size: 0.9rem;
      transition: color 0.2s;
    }

    .nav-links a.active, .nav-links a:hover {
      color: var(--accent-green);
    }

    .theme-toggle {
      background: none;
      border: none;
      color: var(--text-muted);
      cursor: pointer;
      display: flex;
      align-items: center;
    }

    /* HERO SECTION */
    .hero {
      padding: 80px 0 100px;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 40px;
      align-items: center;
    }

    .badge {
      display: inline-block;
      padding: 4px 12px;
      background: rgba(46, 204, 113, 0.1);
      border: 1px solid rgba(46, 204, 113, 0.2);
      color: var(--accent-green);
      border-radius: 20px;
      font-size: 0.75rem;
      font-weight: 600;
      letter-spacing: 0.5px;
      text-transform: uppercase;
      margin-bottom: 20px;
    }

    .hero-title {
      font-size: 3rem;
      font-weight: 700;
      line-height: 1.2;
      margin-bottom: 20px;
    }

    .hero-title span {
      color: var(--accent-green);
    }

    .hero-desc {
      color: var(--text-muted);
      font-size: 1rem;
      margin-bottom: 32px;
      max-width: 480px;
    }

    .hero-buttons {
      display: flex;
      gap: 16px;
    }

    .btn {
      padding: 12px 24px;
      border-radius: 6px;
      font-weight: 600;
      font-size: 0.9rem;
      cursor: pointer;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      transition: all 0.2s;
    }

    .btn-primary {
      background-color: var(--accent-green);
      color: #000;
      border: none;
    }

    .btn-primary:hover {
      background-color: var(--accent-green-hover);
    }

    .btn-secondary {
      background-color: transparent;
      color: var(--text-main);
      border: 1px solid var(--border-color);
    }

    .btn-secondary:hover {
      border-color: var(--text-muted);
    }

    .hero-image-wrapper {
      position: relative;
      display: flex;
      justify-content: center;
    }

    .hero-image {
      width: 100%;
      max-width: 380px;
      border-radius: 12px;
      border: 1px solid var(--border-color);
      box-shadow: 0 0 50px var(--accent-green-glow);
      object-fit: cover;
    }

    /* SECTION GENERAL */
    .section-header {
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
      margin-bottom: 32px;
    }

    .section-title {
      font-size: 1.5rem;
      color: var(--accent-green);
      font-weight: 700;
    }

    .section-desc {
      color: var(--text-muted);
      font-size: 0.875rem;
      margin-top: 4px;
    }

    /* FEATURED WORK */
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 24px;
      margin-bottom: 100px;
    }

    .project-card {
      background: var(--bg-card);
      border: 1px solid var(--border-color);
      border-radius: 12px;
      overflow: hidden;
      padding: 20px;
    }

    .project-img {
      width: 100%;
      height: 180px;
      object-fit: cover;
      border-radius: 8px;
      background-color: #1a1a1a;
      margin-bottom: 16px;
    }

    .tags {
      display: flex;
      gap: 8px;
      margin-bottom: 12px;
    }

    .tag {
      font-size: 0.65rem;
      text-transform: uppercase;
      padding: 2px 8px;
      background: rgba(255, 255, 255, 0.05);
      border-radius: 4px;
      color: var(--text-muted);
    }

    .project-title {
      font-size: 1.2rem;
      font-weight: 600;
      margin-bottom: 8px;
    }

    .project-desc {
      color: var(--text-muted);
      font-size: 0.85rem;
      margin-bottom: 20px;
    }

    .project-links {
      display: flex;
      gap: 16px;
      font-size: 0.8rem;
    }

    .project-links a {
      color: var(--accent-green);
      display: flex;
      align-items: center;
      gap: 4px;
    }

    /* CONTACT SECTION */
    .contact-section {
      margin-bottom: 80px;
    }

    .contact-container {
      display: grid;
      grid-template-columns: 1fr 1.2fr;
      gap: 40px;
    }

    .contact-info h2 {
      font-size: 2rem;
      color: var(--accent-green);
      margin-bottom: 16px;
    }

    .contact-info p {
      color: var(--text-muted);
      font-size: 0.95rem;
      margin-bottom: 32px;
      max-width: 400px;
    }

    .contact-details {
      display: flex;
      flex-direction: column;
      gap: 20px;
      margin-bottom: 32px;
    }

    .contact-item {
      display: flex;
      align-items: center;
      gap: 16px;
    }

    .icon-wrapper {
      width: 40px;
      height: 40px;
      border-radius: 8px;
      background: var(--bg-card);
      border: 1px solid var(--border-color);
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--accent-green);
    }

    .contact-label {
      font-size: 0.7rem;
      text-transform: uppercase;
      color: var(--text-muted);
    }

    .contact-value {
      font-size: 0.9rem;
      font-weight: 500;
    }

    .social-links {
      display: flex;
      gap: 12px;
    }

    .social-icon {
      width: 36px;
      height: 36px;
      border-radius: 6px;
      background: var(--bg-card);
      border: 1px solid var(--border-color);
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--text-muted);
    }

    .contact-form {
      background: var(--bg-card);
      border: 1px solid var(--border-color);
      padding: 32px;
      border-radius: 12px;
    }

    .form-group {
      margin-bottom: 20px;
    }

    .form-group label {
      display: block;
      font-size: 0.75rem;
      text-transform: uppercase;
      color: var(--text-muted);
      margin-bottom: 8px;
    }

    .form-group input,
    .form-group textarea {
      width: 100%;
      padding: 12px 16px;
      background: var(--bg-input);
      border: 1px solid var(--border-color);
      border-radius: 6px;
      color: var(--text-main);
      font-size: 0.9rem;
      outline: none;
    }

    .form-group input:focus,
    .form-group textarea:focus {
      border-color: var(--accent-green);
    }

    .submit-btn {
      width: 100%;
      padding: 14px;
      background: var(--accent-green);
      color: #000;
      border: none;
      border-radius: 6px;
      font-weight: 600;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
    }

    /* FOOTER */
    footer {
      border-top: 1px solid rgba(255, 255, 255, 0.05);
      padding-top: 32px;
    }

    .footer-container {
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-size: 0.85rem;
      color: var(--text-muted);
    }

    .footer-links {
      display: flex;
      gap: 20px;
    }

    /* RESPONSIVE DESIGN */
    @media (max-width: 768px) {
      .hero {
        grid-template-columns: 1fr;
        text-align: center;
      }

      .hero-desc {
        margin: 0 auto 32px;
      }

      .hero-buttons {
        justify-content: center;
      }

      .contact-container {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>

  <!-- HEADER / NAVIGATION -->
  <header>
    <div class="container nav-container">
      <a href="#" class="logo">Android Dev Portfolio</a>
      <ul class="nav-links">
        <li><a href="#projects" class="active">Projects</a></li>
        <li><a href="#contact">Contact</a></li>
        <li>
          <button class="theme-toggle" aria-label="Toggle theme">
            <i data-lucide="moon" size="18"></i>
          </button>
        </li>
      </ul>
    </div>
  </header>

  <!-- MAIN CONTENT -->
  <main class="container">

    <!-- HERO SECTION -->
    <section class="hero">
      <div class="hero-content">
        <span class="badge">● Android Specialist</span>
        <h1 class="hero-title">Hi, I'm an <span>Android Developer</span></h1>
        <p class="hero-desc">
          I build high-quality Android apps with a focus on clean code and user experience. I'm passionate about creating intuitive mobile solutions that solve real-world problems.
        </p>
        <div class="hero-buttons">
          <a href="#projects" class="btn btn-primary">
            View Projects <i data-lucide="arrow-right" size="16"></i>
          </a>
          <a href="#contact" class="btn btn-secondary">Let's talk</a>
        </div>
      </div>
      <div class="hero-image-wrapper">
        <img src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&q=80&w=600" alt="Profile" class="hero-image">
      </div>
    </section>

    <!-- FEATURED WORK SECTION -->
    <section id="projects">
      <div class="section-header">
        <div>
          <h2 class="section-title">Featured Work</h2>
          <p class="section-desc">A curated selection of applications focusing on clean code, material design 3, and seamless user experiences.</p>
        </div>
        <span style="color: var(--text-muted); font-size: 0.8rem;">03 / PROJECTS</span>
      </div>

      <div class="projects-grid">
        <!-- Project 1 -->
        <div class="project-card">
          <img src="https://images.unsplash.com/photo-1616469829941-c7200edec809?auto=format&fit=crop&q=80&w=500" alt="Project 1" class="project-img">
          <div class="tags">
            <span class="tag">KOTLIN</span>
            <span class="tag">JETPACK COMPOSE</span>
          </div>
          <h3 class="project-title">Project Title</h3>
          <p class="project-desc">Detailed description of your app's features and your role in the...</p>
          <div class="project-links">
            <a href="#"><i data-lucide="code-2" size="14"></i> View Code</a>
            <a href="#"><i data-lucide="external-link" size="14"></i> Live Demo</a>
          </div>
        </div>

        <!-- Project 2 -->
        <div class="project-card">
          <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?auto=format&fit=crop&q=80&w=500" alt="Project 2" class="project-img">
          <div class="tags">
            <span class="tag">ROOM</span>
            <span class="tag">HILT</span>
          </div>
          <h3 class="project-title">Project Title</h3>
          <p class="project-desc">Detailed description of your app's features and your role in the...</p>
          <div class="project-links">
            <a href="#"><i data-lucide="code-2" size="14"></i> View Code</a>
            <a href="#"><i data-lucide="external-link" size="14"></i> Live Demo</a>
          </div>
        </div>

        <!-- Project 3 -->
        <div class="project-card">
          <img src="https://images.unsplash.com/photo-1526374965328-7f61d4dc18c5?auto=format&fit=crop&q=80&w=500" alt="Project 3" class="project-img">
          <div class="tags">
            <span class="tag">FIREBASE</span>
            <span class="tag">SDK</span>
          </div>
          <h3 class="project-title">Project Title</h3>
          <p class="project-desc">Detailed description of your app's features and your role in the...</p>
          <div class="project-links">
            <a href="#"><i data-lucide="code-2" size="14"></i> View Code</a>
            <a href="#"><i data-lucide="external-link" size="14"></i> Live Demo</a>
          </div>
        </div>
      </div>
    </section>

    <!-- CONTACT SECTION -->
    <section id="contact" class="contact-section">
      <div class="contact-container">
        <div class="contact-info">
          <h2>Let's build something epic.</h2>
          <p>I build high-quality Android apps with a focus on clean code and user experience. I'm passionate about creating intuitive mobile solutions that solve real-world problems.</p>
          
          <div class="contact-details">
            <div class="contact-item">
              <div class="icon-wrapper"><i data-lucide="mail" size="18"></i></div>
              <div>
                <div class="contact-label">EMAIL</div>
                <div class="contact-value">hello@androiddev.pro</div>
              </div>
            </div>
            
            <div class="contact-item">
              <div class="icon-wrapper"><i data-lucide="map-pin" size="18"></i></div>
              <div>
                <div class="contact-label">LOCATION</div>
                <div class="contact-value">San Francisco, CA (Remote Friendly)</div>
              </div>
            </div>
          </div>

          <div class="social-links">
            <a href="#" class="social-icon"><i data-lucide="github" size="18"></i></a>
            <a href="#" class="social-icon"><i data-lucide="linkedin" size="18"></i></a>
          </div>
        </div>

        <!-- Contact Form -->
        <form class="contact-form" onsubmit="event.preventDefault();">
          <div class="form-group">
            <label for="name">FULL NAME</label>
            <input type="text" id="name" placeholder="John Doe">
          </div>
          
          <div class="form-group">
            <label for="email">EMAIL ADDRESS</label>
            <input type="email" id="email" placeholder="john@example.com">
          </div>
          
          <div class="form-group">
            <label for="message">YOUR MESSAGE</label>
            <textarea id="message" rows="4" placeholder="Tell me about your project..."></textarea>
          </div>

          <button type="submit" class="submit-btn">
            Send Message <i data-lucide="send" size="16"></i>
          </button>
        </form>
      </div>
    </section>

  </main>

  <!-- FOOTER -->
  <footer>
    <div class="container footer-container">
      <div>
        <span style="color: var(--accent-green); font-weight: 600;">Android Dev Portfolio</span>
        <p style="margin-top: 4px; font-size: 0.75rem;">© 2026 Android Dev Portfolio. Built with precision.</p>
      </div>
      <div class="footer-links">
        <a href="#">GitHub</a>
        <a href="#">LinkedIn</a>
        <a href="#">CodePen</a>
      </div>
    </div>
  </footer>

  <!-- Initialize Lucide Icons -->
  <script>
    lucide.createIcons();
  </script>
</body>
</html>
