<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>M Prathip | Software Engineer Portfolio</title>

  <!-- SEO -->
  <meta name="description" content="M Prathip – B.Tech AI & Data Science student, problem solver, aspiring software engineer.">

  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap" rel="stylesheet">

  <!-- Font Awesome -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

  <style>
    :root {
      --primary: #6366f1;
      --secondary: #22d3ee;
      --dark: #0f172a;
      --gray: #64748b;
      --bg: #f1f5f9;
      --card: #ffffff;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Inter', sans-serif;
    }

    html { scroll-behavior: smooth; }

    body {
      background: linear-gradient(180deg, #eef2ff, #f8fafc);
      color: var(--dark);
      line-height: 1.7;
    }

    /* ===== NAVBAR ===== */
    header {
      position: fixed;
      width: 100%;
      top: 0;
      backdrop-filter: blur(12px);
      background: rgba(255,255,255,0.85);
      border-bottom: 1px solid #e5e7eb;
      z-index: 1000;
    }

    .navbar {
      max-width: 1100px;
      margin: auto;
      padding: 15px 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      font-size: 22px;
      font-weight: 800;
      background: linear-gradient(90deg, var(--primary), var(--secondary));
      -webkit-background-clip: text;
      color: transparent;
    }

    .nav-links {
      display: flex;
      gap: 24px;
      list-style: none;
    }

    .nav-links a {
      text-decoration: none;
      color: var(--dark);
      font-weight: 500;
    }

    .nav-links a:hover {
      color: var(--primary);
    }

    /* ===== HERO ===== */
    .hero {
      padding: 170px 20px 110px;
      text-align: center;
      background: radial-gradient(circle at top, #c7d2fe, transparent 60%);
    }

    .hero h1 {
      font-size: 48px;
      font-weight: 800;
    }

    .hero span {
      background: linear-gradient(90deg, var(--primary), var(--secondary));
      -webkit-background-clip: text;
      color: transparent;
    }

    .hero p {
      max-width: 750px;
      margin: 20px auto;
      color: var(--gray);
      font-size: 18px;
    }

    .hero-btns {
      margin-top: 35px;
      display: flex;
      justify-content: center;
      gap: 15px;
      flex-wrap: wrap;
    }

    .btn {
      padding: 13px 32px;
      border-radius: 30px;
      font-weight: 600;
      text-decoration: none;
      transition: all 0.3s;
    }

    .btn.primary {
      background: linear-gradient(90deg, var(--primary), var(--secondary));
      color: #fff;
    }

    .btn.secondary {
      border: 2px solid var(--primary);
      color: var(--primary);
      background: #fff;
    }

    .btn:hover {
      transform: translateY(-4px);
      box-shadow: 0 12px 30px rgba(99,102,241,0.25);
    }

    /* ===== SECTIONS ===== */
    .section {
      padding: 90px 20px;
      max-width: 1100px;
      margin: auto;
    }

    .section h2 {
      text-align: center;
      font-size: 34px;
      margin-bottom: 15px;
    }

    .section-desc {
      text-align: center;
      color: var(--gray);
      max-width: 780px;
      margin: auto;
    }

    /* ===== SKILLS ===== */
    .skills-grid {
      margin-top: 50px;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
      gap: 22px;
    }

    .skill-card {
      background: var(--card);
      padding: 22px;
      text-align: center;
      font-weight: 600;
      border-radius: 18px;
      box-shadow: 0 15px 35px rgba(0,0,0,0.08);
      transition: transform 0.3s;
    }

    .skill-card:hover {
      transform: translateY(-8px);
    }

    /* ===== PROJECTS ===== */
    .projects-grid {
      margin-top: 50px;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 30px;
    }

    .project-card {
      background: var(--card);
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 25px 50px rgba(0,0,0,0.1);
      transition: transform 0.3s;
    }

    .project-card:hover {
      transform: translateY(-10px);
    }

    /* ===== PROFILES ===== */
    .profiles {
  margin-top: 45px;
  display: flex;
  justify-content: center;
  gap: 18px;
  flex-wrap: wrap;
}

.profiles a {
  display: flex;
  align-items: center;
  gap: 12px;
  padding: 16px 28px;
  color: #fff;
  border-radius: 20px;
  text-decoration: none;
  font-weight: 600;
  font-size: 16px;
  transition: transform 0.3s, box-shadow 0.3s, filter 0.3s;
}

.profiles a:hover {
  transform: translateY(-6px);
  box-shadow: 0 15px 40px rgba(0,0,0,0.4);
  filter: brightness(1.1);
}

.profiles a i {
  font-size: 20px;
}


    /* ===== CONTACT ===== */
    .contact-card {
      margin-top: 45px;
      background: linear-gradient(135deg, #6366f1, #22d3ee);
      color: #fff;
      padding: 45px;
      border-radius: 26px;
      text-align: center;
      box-shadow: 0 30px 60px rgba(0,0,0,0.25);
    }

    .contact-card p {
      margin: 14px 0;
      font-size: 18px;
    }

    /* ===== FOOTER ===== */
    footer {
      background: #020617;
      color: #94a3b8;
      padding: 30px;
      text-align: center;
    }

    /* ===== ANIMATION ===== */
    .fade {
      opacity: 0;
      transform: translateY(30px);
      transition: all 0.9s ease;
    }

    .fade.show {
      opacity: 1;
      transform: translateY(0);
    }

    @media (max-width: 768px) {
      .hero h1 { font-size: 36px; }
    }

    /* ===== FEEDBACK CARD ===== */
.feedback-card {
  background: linear-gradient(135deg, #6366f1, #22d3ee);
  padding: 50px;
  border-radius: 26px;
  box-shadow: 0 25px 50px rgba(0,0,0,0.3);
  transition: transform 0.3s, box-shadow 0.3s, background 0.3s;
}


.feedback-card:hover {
  
  transform: translateY(-6px);
  box-shadow: 0 35px 70px rgba(0,0,0,0.35);
  background: linear-gradient(135deg, #4f52e0, #1fb6dd);
}

/* ===== FORM ELEMENTS ===== */
#feedbackForm input,
#feedbackForm textarea {
  width: 100%;
  padding: 14px;
  margin: 12px 0;
  border-radius: 12px;
  border: 1px solid rgba(255,255,255,0.5);
  background: rgba(255,255,255,0.1);
  color: #fff;
  font-size: 16px;
  transition: all 0.3s;
}

#feedbackForm input::placeholder,
#feedbackForm textarea::placeholder {
  color: rgba(255,255,255,0.7);
  transition: all 0.3s;
}

#feedbackForm input:focus,
#feedbackForm textarea:focus {
  border: 2px solid #fff;
  box-shadow: 0 0 15px rgba(255,255,255,0.6);
  outline: none;
  background: rgba(255,255,255,0.2);
}

#feedbackForm input:focus::placeholder,
#feedbackForm textarea:focus::placeholder {
  color: rgba(255,255,255,0.5);
}

#feedbackForm textarea {
  resize: vertical;
  min-height: 120px;
}

/* ===== SUBMIT BUTTON ===== */
#feedbackForm .btn.primary {
  background: linear-gradient(90deg, #22d3ee, #6366f1);
  color: #fff;
  font-weight: 600;
  padding: 14px;
  border-radius: 30px;
  border: none;
  transition: all 0.3s;
  cursor: pointer;
}

#feedbackForm .btn.primary:hover {
  transform: translateY(-4px);
  box-shadow: 0 12px 30px rgba(99,102,241,0.4);
}

#feedbackForm .btn.primary:active {
  transform: scale(0.96);
  box-shadow: 0 8px 20px rgba(99,102,241,0.5);
}

/* ===== FEEDBACK MESSAGE ===== */
#feedbackMessage {
  margin-top: 12px;
  font-weight: 600;
  color: #fff;
  text-align: center;
  opacity: 0;
  transition: opacity 0.5s ease;
}

#feedbackMessage.show {
  opacity: 1;
}

  </style>
</head>

<body>

<header>
  <nav class="navbar">
    <div class="logo">M Prathip</div>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#profiles">Profiles</a></li>
      <li><a href="#contact">Contact</a></li>
      <li><a href="#feedback">Feedback</a></li>
    </ul>
  </nav>
</header>

<section class="hero fade">
  <h1>Hello, I'm <span>M Prathip</span></h1>
  <p>
    B.Tech AI & Data Science student passionate about problem-solving,
    scalable software systems, and modern UI engineering.
  </p>
  <div class="hero-btns">
    <a href="#projects" class="btn primary">View Projects</a>
    <a href="#profiles" class="btn secondary">Coding Profiles</a>
  </div>
</section>

<section id="about" class="section fade">
  <h2>About Me</h2>
  <p class="section-desc">
  I am M. Prathip, an aspiring software engineer with a strong focus on
  Data Structures and Algorithms, solid core fundamentals, and building
  real-world applications using clean and maintainable code.
  I actively practice DSA and engage in competitive programming on
  platforms such as LeetCode, CodeChef, and GeeksforGeeks, which has
  strengthened my problem-solving skills, analytical thinking, and
  consistency.
</p>
</section>

<section id="skills" class="section fade">
  <h2>Technical Skills</h2>
  <div class="skills-grid">
    <div class="skill-card">Java</div>
    <div class="skill-card">Python</div>
    <div class="skill-card">C</div>
    <div class="skill-card">HTML & CSS</div>
    <div class="skill-card">JavaScript</div>
    <div class="skill-card">Git & GitHub</div>
    <div class="skill-card">DSA</div>
    <div class="skill-card">Problem Solving</div>
    <div class="skill-card">UI Development</div>
    <div class="skill-card">Responsive Design</div>
  </div>
</section>

<section id="projects" class="section fade">
  <h2>Projects</h2>
  <div class="projects-grid">

  <div class="project-card">
    <h3>Elite Portfolio Website</h3>
    <p>Modern, animated, fully responsive portfolio with 95% Lighthouse score.</p>
    <p><strong>Tech:</strong> HTML, CSS, JavaScript</p>
  </div>

  <div class="project-card">
    <h3>Responsive Landing Page</h3>
    <p>High-performance landing page with clean UI and mobile-first design.</p>
    <p><strong>Tech:</strong> HTML, CSS</p>
  </div>

  <div class="project-card">
    <h3>Event Management Website</h3>
    <p>Interactive event website with organized sections and smooth navigation.</p>
    <p><strong>Tech:</strong> HTML, CSS, JavaScript</p>
  </div>

</div>

    
</section>

<section id="profiles" class="section fade">
  <h2>Profile Links</h2>
  <p class="section-desc">
    Connect with me on my coding and professional platforms.
  </p>
  <div class="profiles">
    <a href="https://leetcode.com/u/Prathip_2628/" target="_blank" style="background:#FFA116;">
      <i class="fa-brands fa-leanpub"></i> LeetCode
    </a>
    <a href="https://www.codechef.com/users/prathip_2826" target="_blank" style="background:#BB0000;">
      <i class="fa-solid fa-utensils"></i> CodeChef
    </a>
    <a href="https://www.geeksforgeeks.org/profile/prathipro4el" target="_blank" style="background:#0F9D58;">
      <i class="fa-brands fa-git-alt"></i> GeeksforGeeks
    </a>
    <a href="https://www.linkedin.com/in/prathip-raja-a9a179330/" target="_blank" style="background:#0077B5;">
      <i class="fa-brands fa-linkedin"></i> LinkedIn
    </a>
    <a href="https://github.com/Prathip2826" target="_blank" style="background:#171515;">
      <i class="fa-brands fa-github"></i> GitHub
    </a>
  </div>
</section>



<section id="contact" class="section fade">
  <h2>Contact</h2>
  <div class="contact-card">
    <p><strong>Email:</strong> prathipraja777@gmail.com</p>
    <p><strong>Phone:</strong> 9790862545</p>
    <p><strong>Location:</strong> Namakkal,Tamil Nadu.</p>
  </div>
</section>
<section id="feedback" class="section fade">
  <h2>Feedback</h2>
  <p class="section-desc">
    Your feedback helps me improve and grow as a developer.
  </p>
  <h3 style="font-size:26px;margin-bottom:15px;">
  💬 Share Your Feedback
  </h3>
  <div class="feedback-card">
    <form id="feedbackForm">
      <input type="text" name="name" placeholder="Your Name" required>
      <input type="email" name="email" placeholder="Your Email" required>
      <textarea name="message" placeholder="Your Feedback" required></textarea>
      <button type="submit" class="btn primary">
  Send Feedback 🚀
</button>
      <p id="feedbackMessage"></p>
    </form>
  </div>
</section>

 <script>
const feedbackForm = document.getElementById('feedbackForm');
const feedbackMessage = document.getElementById('feedbackMessage');

feedbackForm.addEventListener('submit', function(e) {
  e.preventDefault();

  feedbackMessage.textContent = "✅ Feedback submitted successfully!";
  feedbackMessage.classList.add("show");

  feedbackForm.reset();

  setTimeout(() => {
    feedbackMessage.classList.remove("show");
    feedbackMessage.textContent = "";
  }, 3500);
});
</script>

<footer>
  © 2025 M Prathip · Built using HTML, CSS & JavaScript
</footer>


<script>
  // Fade-in animation on scroll
  const faders = document.querySelectorAll('.fade');

  const appearOptions = {
    threshold: 0.1,
    rootMargin: "0px 0px -50px 0px"
  };

  const appearOnScroll = new IntersectionObserver(function(
    entries,
    appearOnScroll
  ) {
    entries.forEach(entry => {
      if (!entry.isIntersecting) {
        return;
      } else {
        entry.target.classList.add('show');
        appearOnScroll.unobserve(entry.target);
      }
    });
  },
  appearOptions);

  faders.forEach(fader => {
    appearOnScroll.observe(fader);
  });
  
</script>

</body>
</html>
