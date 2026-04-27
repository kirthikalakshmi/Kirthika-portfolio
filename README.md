<!DOCTYPE html>
<html>
<head>
    <title>Kirthika Portfolio</title>

    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

    <style>
        body {
            margin: 0;
            font-family: 'Segoe UI', sans-serif;
            background: linear-gradient(270deg, #020617, #0f172a, #020617);
            background-size: 600% 600%;
            animation: gradientMove 12s ease infinite;
            color: #e2e8f0;
        }

        @keyframes gradientMove {
            0% {background-position: 0% 50%;}
            50% {background-position: 100% 50%;}
            100% {background-position: 0% 50%;}
        }

        /* BANNER */
        .banner {
            width: 100%;
            height: 260px;
            overflow: hidden;
        }

        .banner img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        /* NAV BAR */
        .main-nav {
            display: flex;
            justify-content: center;
            gap: 40px;
            padding: 15px;
            background: rgba(15,23,42,0.9);
            backdrop-filter: blur(10px);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .main-nav a {
            color: #e2e8f0;
            text-decoration: none;
            font-weight: bold;
            transition: 0.3s;
        }

        .main-nav a:hover {
            color: #22c55e;
        }

        .main-nav a.active {
            color: #22c55e;
            position: relative;
        }

        .main-nav a.active::after {
            content: "";
            position: absolute;
            width: 100%;
            height: 2px;
            bottom: -5px;
            left: 0;
            background: #22c55e;
        }

        /* HERO */
        .hero {
            padding: 60px 50px 30px;
        }

        h2 {
            font-size: 40px;
        }

        section {
            padding: 40px 50px;
            opacity: 0;
            transform: translateY(30px);
            transition: 0.8s;
        }

        section.show {
            opacity: 1;
            transform: translateY(0);
        }

        h3 {
            color: #22c55e;
        }

        .card {
            background: #1e293b;
            padding: 20px;
            border-radius: 10px;
        }

        /* SKILLS */
        .skills {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
        }

        .skill-box {
            background: #020617;
            padding: 15px;
            border-radius: 10px;
            width: 100px;
            text-align: center;
            transition: 0.3s;
        }

        .skill-box:hover {
            transform: scale(1.15);
            background: #22c55e;
            color: black;
        }

        .skill-box i {
            font-size: 28px;
        }

        /* PROJECTS */
        .projects {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
        }

        .project-card {
            background: #1e293b;
            width: 300px;
            border-radius: 10px;
            overflow: hidden;
            transition: 0.3s;
        }

        .project-card:hover {
            transform: scale(1.05);
        }

        .project-card img {
            width: 100%;
            height: 160px;
            object-fit: cover;
        }

        .project-content {
            padding: 15px;
        }

        .btn {
            display: inline-block;
            margin-top: 10px;
            padding: 8px 12px;
            background: #22c55e;
            color: black;
            text-decoration: none;
            border-radius: 5px;
        }

        /* SCROLL BUTTON */
        #topBtn {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: #22c55e;
            color: black;
            border: none;
            padding: 12px;
            border-radius: 50%;
            display: none;
            cursor: pointer;
        }

        footer {
            text-align: center;
            padding: 20px;
        }
    </style>
</head>

<body>

<!-- BANNER -->
<header class="banner">
    <img src="Kirthika Lakshmi.png">
</header>

<!-- NAV -->
<nav class="main-nav">
    <a href="#about">About</a>
    <a href="#skills">Skills</a>
    <a href="#projects">Projects</a>
    <a href="#contact">Contact</a>
</nav>

<!-- HERO -->
<div class="hero">
    <h2>Hi, I'm Kirthika Lakshmi 👋</h2>
    <p>Data Analyst | BE, MBA | Excel • Power BI • SQL</p>
</div>

<!-- ABOUT -->
<section id="about">
    <h3>About Me</h3>
    <div class="card">
        <p>Detail-oriented Data Analyst with strong skills in Excel, Power BI, and SQL. Focused on transforming raw data into actionable insights.</p>
    </div>
</section>

<!-- SKILLS -->
<section id="skills">
    <h3>Skills</h3>
    <div class="skills">
        <div class="skill-box"><i class="fa-solid fa-file-excel"></i><p>Excel</p></div>
        <div class="skill-box"><i class="fa-brands fa-python"></i><p>Python</p></div>
        <div class="skill-box"><i class="fa-solid fa-database"></i><p>SQL</p></div>
        <div class="skill-box"><i class="fa-solid fa-chart-line"></i><p>Power BI</p></div>
    </div>
</section>

<!-- PROJECTS -->
<section id="projects">
    <h3>Projects</h3>
    <div class="projects">

        <div class="project-card">
            <img src="icon1.jpg">
            <div class="project-content">
                <h4>Sales Dashboard</h4>
                <p>Excel dashboard analyzing sales performance.</p>
                <a href="sales-project.html" class="btn">View Project</a>
            </div>
        </div>

        <div class="project-card">
            <img src="https://via.placeholder.com/300x160">
            <div class="project-content">
                <h4>Customer Analysis</h4>
                <p>Customer segmentation using Excel.</p>
                <a href="#" class="btn">In Progress</a>
            </div>
        </div>

    </div>
</section>

<!-- CONTACT -->
<section id="contact">
    <h3>Contact</h3>
    <div class="card">
        <p>Email: kirthikaviru@gmail.com</p>
    </div>
</section>

<footer>
    <p>© 2026 Kirthika Lakshmi</p>
</footer>

<!-- SCROLL BUTTON -->
<button id="topBtn"><i class="fa-solid fa-arrow-up"></i></button>

<script>
    const sections = document.querySelectorAll("section");
    const navLinks = document.querySelectorAll(".main-nav a");
    const topBtn = document.getElementById("topBtn");

    window.addEventListener("scroll", () => {

        let current = "";

        sections.forEach(sec => {
            const sectionTop = sec.offsetTop - 150;

            if (pageYOffset >= sectionTop) {
                current = sec.getAttribute("id");
            }

            if (sec.getBoundingClientRect().top < window.innerHeight - 100) {
                sec.classList.add("show");
            }
        });

        navLinks.forEach(link => {
            link.classList.remove("active");
            if (link.getAttribute("href") === "#" + current) {
                link.classList.add("active");
            }
        });

        if (document.documentElement.scrollTop > 200) {
            topBtn.style.display = "block";
        } else {
            topBtn.style.display = "none";
        }
    });

    topBtn.onclick = () => {
        window.scrollTo({ top: 0, behavior: "smooth" });
    };
</script>

</body>
</html>
