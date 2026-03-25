<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ritesh Pal | Backend Developer</title>

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600&display=swap" rel="stylesheet">

<style>
:root {
  --bg: #0f172a;
  --card: #1e293b;
  --text: #e2e8f0;
  --muted: #94a3b8;
  --accent: #38bdf8;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Inter', sans-serif;
}

html {
  scroll-behavior: smooth;
}

body {
  background: var(--bg);
  color: var(--text);
}

/* NAV */
nav {
  position: fixed;
  width: 100%;
  top: 0;
  background: rgba(15, 23, 42, 0.9);
  padding: 15px;
  text-align: center;
  backdrop-filter: blur(10px);
  z-index: 1000;
}

nav a {
  color: var(--text);
  margin: 0 15px;
  text-decoration: none;
}

nav a:hover {
  color: var(--accent);
}

/* HERO */
.hero {
  text-align: center;
  padding: 140px 20px 80px;
}

.hero h1 {
  font-size: 3rem;
}

.hero span {
  color: var(--accent);
}

.hero p {
  color: var(--muted);
  max-width: 600px;
  margin: 15px auto;
}

.btn {
  display: inline-block;
  margin: 10px;
  padding: 12px 22px;
  background: var(--accent);
  color: #000;
  border-radius: 6px;
  text-decoration: none;
  font-weight: 600;
}

/* SECTION */
section {
  max-width: 1000px;
  margin: auto;
  padding: 70px 20px;
}

h2 {
  color: var(--accent);
  margin-bottom: 20px;
}

/* CARDS */
.card {
  background: var(--card);
  padding: 20px;
  border-radius: 12px;
  margin-bottom: 20px;
  transition: 0.3s;
}

.card:hover {
  transform: translateY(-5px);
}

/* SKILLS */
.skills span {
  display: inline-block;
  background: #334155;
  padding: 8px 12px;
  margin: 5px;
  border-radius: 20px;
}

/* PROJECT */
.project a {
  color: var(--accent);
  text-decoration: none;
}

/* FOOTER */
footer {
  text-align: center;
  padding: 20px;
  color: var(--muted);
}

/* ANIMATION */
.hidden {
  opacity: 0;
  transform: translateY(40px);
  transition: 0.8s;
}

.show {
  opacity: 1;
  transform: translateY(0);
}

@media(max-width:600px){
  .hero h1 {
    font-size: 2rem;
  }
}
</style>
</head>

<body>

<nav>
  <a href="#about">About</a>
  <a href="#skills">Skills</a>
  <a href="#projects">Projects</a>
  <a href="#contact">Contact</a>
</nav>

<section class="hero">
  <h1>Hi, I'm <span>Ritesh Pal</span></h1>
  <p>Backend Developer | Python | Django | REST APIs</p>
  <p>I build scalable backend systems and real-world applications that solve practical problems.</p>
  <a href="#projects" class="btn">View Projects</a>
  <a href="#contact" class="btn">Contact Me</a>
</section>

<section id="about" class="hidden">
  <h2>About Me</h2>
  <div class="card">
    <p>
      MCA student with hands-on experience in Python, Django, and full-stack development.
      I specialize in backend systems, API development, and building scalable applications.
    </p>
  </div>
</section>

<section id="skills" class="hidden">
  <h2>Skills</h2>
  <div class="card skills">
    <span>Python</span><span>Django</span><span>REST APIs</span>
    <span>React</span><span>SQL</span><span>MySQL</span>
    <span>PostgreSQL</span><span>JavaScript</span>
    <span>OpenCV</span><span>MediaPipe</span>
    <span>Pandas</span><span>Git</span>
  </div>
</section>

<section id="projects" class="hidden">
  <h2>Projects</h2>

  <div class="card project">
    <h3>HOS Compliance Planner</h3>
    <p>Built a full-stack application for HOS-compliant trip planning with real-time route visualization.</p>
    <p><strong>Tech:</strong> Django, React, REST API</p>
    <a href="https://github.com/riteshpal1/HOS_Project" target="_blank">View Project</a>
  </div>

  <div class="card project">
    <h3>GystureSync</h3>
    <p>Gesture-based system for controlling mouse and volume using computer vision.</p>
    <p><strong>Tech:</strong> Python, OpenCV, MediaPipe</p>
  </div>

</section>

<section id="contact" class="hidden">
  <h2>Contact</h2>
  <div class="card">
    <p>Email: 8052ritesh@gmail.com</p>
    <p>
      <a href="https://github.com/riteshpal1">GitHub</a> |
      <a href="https://linkedin.com/in/ritesh-pal1">LinkedIn</a>
    </p>
  </div>
</section>

<footer>
  <p>© 2026 Ritesh Pal</p>
</footer>

<script>
const elements = document.querySelectorAll(".hidden");

const observer = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if(entry.isIntersecting){
      entry.target.classList.add("show");
    }
  });
});

elements.forEach(el => observer.observe(el));
</script>

</body>
</html>
