
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio</title>
    <link rel="icon" type="image/png" href="/home/vishwanathsk/Downloads/vskfavicon.png">    
    <style>
        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background-color: #f8fafc;
            color: #1e293b;
            margin: 0;
            line-height: 1.6;
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 1.5rem;
        }
        .btn {
            display: inline-block;
            background-color: #4f46e5;
            color: #ffffff;
            padding: 0.75rem 1.5rem;
            border-radius: 0.5rem;
            text-decoration: none;
            font-weight: 500;
            transition: transform 0.2s ease, box-shadow 0.2s ease;
        }
        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        .btn-secondary {
             background-color: transparent;
             color: #4f46e5;
             border: 2px solid #4f46e5;
        }

        
        section {
            padding: 5rem 0;
        }
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #1e293b;
        }

        header {
            background-color: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid #e2e8f0;
            position: sticky;
            top: 0;
            z-index: 10;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 5rem;
        }

        .nav-logo {
            font-size: 1.5rem;
            font-weight: 700;
            text-decoration: none;
            color: #1e293b;
        }

        .nav-links {
            display: none; 
            list-style: none;
            margin: 0;
            padding: 0;
            gap: 2rem;
        }
        .nav-links a {
            text-decoration: none;
            color: #475569;
            font-weight: 500;
            transition: color 0.2s ease;
        }
        .nav-links a:hover {
            color: #4f46e5;
            transform: translateY(-2px); 
        }
        .hamburger-menu {
            display: block;
            cursor: pointer;
        }
        .hamburger-menu i {
            font-size: 1.5rem;
        }
        #menu-toggle {
            display: none;
        }
        .mobile-menu {
            display: none;
            padding-bottom: 1rem;
        }
        .mobile-menu ul {
            list-style: none;
            padding: 0;
            margin: 0;
            text-align: center;
        }
        .mobile-menu li {
            padding: 1rem 0;
        }
        .mobile-menu a {
            text-decoration: none;
            color: #475569;
            font-size: 1.1rem;
        }
        #menu-toggle:checked ~ .container .mobile-menu {
            display: block;
        }
        #menu-toggle:checked ~ .container nav .hamburger-menu i::before {
             content: '\f00d'; 
        }
        .hero {
            display: flex;
            align-items: center;
            min-height: calc(100vh - 5rem);
        }
        .hero-content {
            text-align: center;
        }
        .hero-content h1 {
            font-size: 2.5rem;
            line-height: 1.2;
            margin-bottom: 1rem;
        }
        .hero-content h1 span {
            color: #4f46e5;
        }
        .hero-content p {
            font-size: 1.1rem;
            color: #475569;
            max-width: 600px;
            margin: 0 auto 2rem;
        }
        .hero-buttons {
            display: flex;
            justify-content: center;
            gap: 1rem;
        }
        .about-content {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 3rem;
        }
        .about-image {
            width: 300px;
            height: 330px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid #ffffff;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }
         .about-image:hover {
            transform: scale(1.05);
        }
        .about-text {
            flex: 1;
            text-align: center;
        }
        .about-text p {
             max-width: 650px;
             margin: 0 auto 2rem;
        }
        .skills-list {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 1rem;
            list-style: none;
            padding: 0;
        }
        .skills-list li {
            background-color: #eef2ff;
            color: #4338ca;
            padding: 0.5rem 1rem;
            border-radius: 9999px;
            font-weight: 500;
            transition: transform 0.2s ease, background-color 0.2s ease; 
        }

        .skills-list li:hover {
            transform: scale(1.05); 
            background-color: #e0e7ff; 
        }
        #projects {
            background-color: #ffffff;
        }
        .projects-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 2rem;
        }
        .project-card {
            background-color: #ffffff;
            border: 1px solid #e2e8f0;
            border-radius: 0.75rem;
            overflow: hidden;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px rgba(0,0,0,0.1);
        }
        .project-image {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        .project-info {
            padding: 1.5rem;
        }
        .project-info h3 {
            margin-top: 0;
        }
        .project-info p {
            color: #475569;
            margin-bottom: 1rem;
        }
        .project-links a {
            margin-right: 1rem;
            color: #4f46e5;
            text-decoration: none;
            font-weight: 500;
        }
        .project-links a:hover {
            text-decoration: underline;
        }
        .contact-content p {
            text-align: center;
            max-width: 500px;
            margin: 0 auto 2rem;
        }
        .contact-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
        }
        .contact-links a {
            color: #475569;
            font-size: 2rem;
            transition: color 0.2s ease, transform 0.2s ease;
        }
        .contact-links a:hover {
            color: #4f46e5;
            transform: translateY(-2px);
        }
        footer {
            background-color: #1e293b;
            color: #cbd5e1;
            text-align: center;
            padding: 2rem 0;
        }

        .footer-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-bottom: 1rem;
        }

        .footer-links a {
            color: #cbd5e1;
            font-size: 1.5rem;
            transition: color 0.2s ease, transform 0.2s ease;
        }

        .footer-links a:hover {
            color: #ffffff;
            transform: translateY(-2px);
        }

        @media (min-width: 768px) {
            .hamburger-menu {
                display: none;
            }
            .nav-links {
                display: flex;
            }
            .hero-content {
                text-align: left;
            }
            .hero-content h1 {
                 font-size: 3.5rem;
            }
            .hero-content p, .hero-buttons {
                margin: 0 0 2rem 0;
                justify-content: flex-start;
            }
             .about-content {
                flex-direction: row;
                text-align: left;
            }
            .about-text {
                text-align: left;
            }
             .skills-list, .about-text p {
                justify-content: flex-start;
                margin: 0 0 2rem 0;
            }
            .projects-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (min-width: 1024px) {
            .projects-grid {
                grid-template-columns: repeat(3, 1fr);
            }
        }

    </style>
</head>
<body>

    <header>
        <input type="checkbox" id="menu-toggle">
        <div class="container">
            <nav>
                <a href="#" class="nav-logo">Vishwanath S K</a>
                <ul class="nav-links">
                    <li><a href="#">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
                <label for="menu-toggle" class="hamburger-menu">
                    <i class="fas fa-bars"></i>
                </label>
            </nav>
            <div class="mobile-menu">
                 <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </div>
        </div>
    </header>

    <main>
        <section class="hero">
            <div class="container">
                <div class="hero-content">
                    <h1>Hi, I'm <span>Vishwanath S K</span>.<br>A Creative Web Developer.</h1>
                    <p>I build clean, modern, and responsive websites. Let's turn your ideas into reality.</p>
                    <div class="hero-buttons">
                        <a href="#projects" class="btn">View My Work</a>
                        <a href="#" class="btn btn-secondary">Download Resume</a>
                    </div>
                </div>
            </div>
        </section>
        <article id="about">
            <div class="container">
                <h2 class="section-title">About Me</h2>
                <div class="about-content">
                    <img src="/home/vishwanathsk/Pictures/Screenshots/Screenshot from 2025-10-02 12-58-28.png" alt="image" class="about-image">
                    <div class="about-text">
                        <h3>Who I Am</h3>
                        <p>
                            Hello! I'm a passionate developer, with a love for creating beautiful and functional web experiences. My journey into coding started with a simple "Hello World", and since then, I've been dedicated to learning new technologies and building projects that solve real-world problems.
                        </p>
                        <h3>Skills</h3>
                        <ul class="skills-list">
                            <li>C++</li>
                            <li>HTML</li>
                            <li>CSS</li>
                            <li>JavaScript</li>
                            <li>Java</li>
                        </ul>
                    </div>
                </div>
            </div>
        </article>
        <section id="projects">
            <div class="container">
                <h2 class="section-title">Projects</h2>
                <div class="projects-grid">
                    <article class="project-card">
                        <img src="/home/vishwanathsk/Pictures/Screenshots/Screenshot from 2025-10-02 13-33-05.png" alt="Moon-Orbit" class="project-image">
                        <div class="project-info">
                            <h3>Moon-Orbit</h3>
                            <p>Animated project showing the Moon revolving around the Earth using CSS keyframes</p>
                            <div class="project-links">
                                <a href="/home/vishwanathsk/Desktop/htmlassignments/10moonorbit.html" target="_blank"><i class="fas fa-globe">Live Demo</i> </a>
                                <a href="#" target="_blank"><i class="fab fa-github">View Code</i> </a>
                            </div>
                        </div>
                    </article>
                     <article class="project-card">
                        <img src="/home/vishwanathsk/Downloads/dogimage.jpeg" alt="Dog-Gallery" class="project-image">
                        <div class="project-info">
                            <h3>Dog-Gallery</h3>
                            <p>A responsive gallery displaying cute dog images with clean layout design</p>
                            <div class="project-links">
                                <a href="/home/vishwanathsk/Desktop/htmlassignments/8dog-gallery.html" target="_blank"><i class="fas fa-globe"> Live Demo</i></a>
                                <a href="#"><i class="fab fa-github">View Code</i></a>
                            </div>
                        </div>
                    </article>
                     <article class="project-card">
                        <img src="/home/vishwanathsk/Downloads/ferriswheelimage.webp" alt="Ferris-Wheel" class="project-image">
                        <div class="project-info">
                            <h3>Ferris-Wheel</h3>
                            <p>Rotating Ferris wheel animation with color-changing cabins using CSS transforms</p>
                                <div class="project-links">
                                <a href="/home/vishwanathsk/Desktop/htmlassignments/10ferriswheel.html"target="_blank"><i class="fab fa-github">Live Demo</i></a>
                                <a href="#"target="_blank"><i class="fab fa-github">View Code</i></a>
                            </div>
                        </div>
                    </article>
                </div>
            </div>
        </section>

        <section id="contact">
            <div class="container">
                <h2 class="section-title">Get In Touch</h2>
                <div class="contact-content">
                    <p>I'm currently open to new opportunities and collaborations. Feel free to reach out via email or connect with me on social media!</p>
                   
                </div>
            </div>
        </section>
    </main>

    <footer>
        <div class="container">
            <div class="footer-links">
                <a href="#">Email</a>
                <a href="#">LinkedIn</a>
                <a href="#">GitHub</a>
            </div>
            <p>&copy; 2025 Vishwanath S K. All Rights Reserved.</p>
        </div>
    </footer>

</body>
</html>
