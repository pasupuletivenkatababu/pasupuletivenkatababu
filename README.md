<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Venkata Babu - Python Developer | GenAI Engineer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #0f172a;
            --secondary: #1e293b;
            --accent: #3b82f6;
            --accent-light: #60a5fa;
            --accent-dark: #1d4ed8;
            --text-primary: #f1f5f9;
            --text-secondary: #cbd5e1;
            --border: #334155;
            --success: #10b981;
            --warning: #f59e0b;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, var(--primary) 0%, #0a0e27 50%, var(--secondary) 100%);
            color: var(--text-primary);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* BACKGROUND ANIMATION */
        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 20% 50%, rgba(59, 130, 246, 0.1) 0%, transparent 50%),
                        radial-gradient(circle at 80% 80%, rgba(16, 185, 129, 0.05) 0%, transparent 50%);
            pointer-events: none;
            z-index: -1;
        }

        /* NAVBAR */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(15, 23, 42, 0.9);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid var(--border);
            z-index: 1000;
            padding: 1rem 2rem;
            animation: slideDown 0.6s ease-out;
        }

        @keyframes slideDown {
            from {
                transform: translateY(-100%);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        .navbar-content {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            background: linear-gradient(135deg, var(--accent) 0%, var(--accent-light) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            color: var(--text-secondary);
            text-decoration: none;
            transition: color 0.3s ease;
            font-size: 0.95rem;
            font-weight: 500;
        }

        .nav-links a:hover {
            color: var(--accent-light);
        }

        /* HERO SECTION */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 2rem;
            margin-top: 60px;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -10%;
            width: 600px;
            height: 600px;
            background: radial-gradient(circle, rgba(59, 130, 246, 0.15) 0%, transparent 70%);
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(30px); }
        }

        .hero-content {
            z-index: 10;
            text-align: center;
            animation: fadeInUp 1s ease-out;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero h1 {
            font-size: clamp(2.5rem, 8vw, 4rem);
            font-weight: 800;
            margin-bottom: 1rem;
            line-height: 1.2;
        }

        .hero .highlight {
            background: linear-gradient(135deg, var(--accent) 0%, var(--success) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero p {
            font-size: 1.25rem;
            color: var(--text-secondary);
            margin-bottom: 2rem;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .cta-buttons {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            flex-wrap: wrap;
            margin-bottom: 3rem;
        }

        .btn {
            padding: 0.75rem 2rem;
            border: none;
            border-radius: 8px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            font-size: 1rem;
            text-decoration: none;
            display: inline-block;
        }

        .btn-primary {
            background: linear-gradient(135deg, var(--accent) 0%, var(--accent-light) 100%);
            color: white;
            box-shadow: 0 8px 24px rgba(59, 130, 246, 0.4);
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 12px 32px rgba(59, 130, 246, 0.6);
        }

        .btn-secondary {
            background: transparent;
            color: var(--accent-light);
            border: 2px solid var(--accent-light);
        }

        .btn-secondary:hover {
            background: var(--accent);
            border-color: var(--accent);
            color: white;
            transform: translateY(-2px);
        }

        .social-links {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            margin-top: 2rem;
        }

        .social-links a {
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            background: var(--secondary);
            color: var(--text-secondary);
            transition: all 0.3s ease;
            text-decoration: none;
            font-weight: 600;
        }

        .social-links a:hover {
            background: var(--accent);
            color: white;
            transform: translateY(-3px);
        }

        /* CONTAINER */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        /* SECTION STYLES */
        section {
            padding: 4rem 0;
            scroll-margin-top: 80px;
        }

        .section-title {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 3rem;
            text-align: center;
            position: relative;
            padding-bottom: 1rem;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 60px;
            height: 4px;
            background: linear-gradient(135deg, var(--accent) 0%, var(--success) 100%);
            border-radius: 2px;
        }

        /* ABOUT SECTION */
        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
            margin-top: 3rem;
        }

        .about-text h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--accent-light);
        }

        .about-text p {
            margin-bottom: 1rem;
            color: var(--text-secondary);
            line-height: 1.8;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 1.5rem;
            margin-top: 1.5rem;
        }

        .skill-card {
            background: var(--secondary);
            padding: 1.5rem;
            border-radius: 8px;
            border: 1px solid var(--border);
            transition: all 0.3s ease;
        }

        .skill-card:hover {
            border-color: var(--accent);
            background: rgba(59, 130, 246, 0.05);
            transform: translateY(-2px);
        }

        .skill-card h4 {
            color: var(--accent-light);
            margin-bottom: 0.75rem;
            font-size: 1.1rem;
        }

        .skill-card p {
            color: var(--text-secondary);
            font-size: 0.95rem;
            margin: 0;
        }

        /* PROJECTS SECTION */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .project-card {
            background: linear-gradient(135deg, var(--secondary) 0%, rgba(30, 41, 59, 0.5) 100%);
            border: 1px solid var(--border);
            border-radius: 12px;
            overflow: hidden;
            transition: all 0.3s ease;
            cursor: pointer;
            position: relative;
            display: flex;
            flex-direction: column;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, var(--accent) 0%, var(--success) 100%);
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-8px);
            border-color: var(--accent);
            box-shadow: 0 20px 40px rgba(59, 130, 246, 0.2);
        }

        .project-card:hover::before {
            opacity: 1;
        }

        .project-header {
            padding: 2rem;
            background: linear-gradient(135deg, rgba(59, 130, 246, 0.1) 0%, rgba(16, 185, 129, 0.05) 100%);
            border-bottom: 1px solid var(--border);
        }

        .project-title {
            font-size: 1.3rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            color: var(--accent-light);
        }

        .project-subtitle {
            color: var(--text-secondary);
            font-size: 0.9rem;
            margin-bottom: 1rem;
        }

        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }

        .tag {
            display: inline-block;
            background: rgba(59, 130, 246, 0.2);
            color: var(--accent-light);
            padding: 0.3rem 0.8rem;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
        }

        .project-body {
            padding: 2rem;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }

        .project-description {
            color: var(--text-secondary);
            margin-bottom: 1.5rem;
            flex-grow: 1;
        }

        .project-features {
            list-style: none;
            margin-bottom: 1.5rem;
        }

        .project-features li {
            color: var(--text-secondary);
            margin-bottom: 0.5rem;
            padding-left: 1.5rem;
            position: relative;
        }

        .project-features li::before {
            content: '✓';
            position: absolute;
            left: 0;
            color: var(--success);
            font-weight: 700;
        }

        /* EXPERIENCE SECTION */
        .experience-timeline {
            position: relative;
            margin-top: 3rem;
        }

        .experience-timeline::before {
            content: '';
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            width: 2px;
            height: 100%;
            background: linear-gradient(180deg, var(--accent) 0%, transparent 100%);
        }

        .experience-item {
            margin-bottom: 3rem;
            width: 45%;
            position: relative;
        }

        .experience-item:nth-child(odd) {
            margin-left: 0;
            text-align: right;
            padding-right: 5%;
        }

        .experience-item:nth-child(even) {
            margin-left: 55%;
        }

        .experience-dot {
            position: absolute;
            width: 12px;
            height: 12px;
            background: var(--accent);
            border-radius: 50%;
            top: 0;
            border: 3px solid var(--primary);
        }

        .experience-item:nth-child(odd) .experience-dot {
            right: -7.5%;
        }

        .experience-item:nth-child(even) .experience-dot {
            left: -7.5%;
        }

        .experience-card {
            background: var(--secondary);
            padding: 1.5rem;
            border-radius: 8px;
            border-left: 3px solid var(--accent);
            transition: all 0.3s ease;
        }

        .experience-card:hover {
            background: rgba(59, 130, 246, 0.1);
            transform: translateY(-2px);
        }

        .experience-title {
            font-size: 1.2rem;
            font-weight: 700;
            color: var(--accent-light);
            margin-bottom: 0.3rem;
        }

        .experience-date {
            color: var(--text-secondary);
            font-size: 0.9rem;
            margin-bottom: 0.8rem;
        }

        .experience-description {
            color: var(--text-secondary);
            line-height: 1.6;
        }

        /* CONTACT SECTION */
        .contact-content {
            text-align: center;
            max-width: 600px;
            margin: 3rem auto 0;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
            margin-bottom: 2rem;
        }

        .contact-item {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 1rem;
            color: var(--text-secondary);
        }

        .contact-item strong {
            color: var(--accent-light);
        }

        .contact-item a {
            color: var(--accent-light);
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .contact-item a:hover {
            color: var(--accent);
            text-decoration: underline;
        }

        /* FOOTER */
        footer {
            background: var(--secondary);
            border-top: 1px solid var(--border);
            padding: 2rem;
            text-align: center;
            color: var(--text-secondary);
        }

        /* RESPONSIVE */
        @media (max-width: 768px) {
            .nav-links {
                gap: 1rem;
                font-size: 0.85rem;
            }

            .about-grid {
                grid-template-columns: 1fr;
            }

            .skills-grid {
                grid-template-columns: 1fr;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }

            .experience-timeline::before {
                left: 0;
            }

            .experience-item,
            .experience-item:nth-child(odd) {
                width: 100%;
                margin-left: 2rem;
                padding-right: 0;
                text-align: left;
            }

            .experience-item:nth-child(even) {
                margin-left: 2rem;
            }

            .experience-dot {
                left: -15px !important;
            }

            .cta-buttons {
                flex-direction: column;
            }

            .btn {
                width: 100%;
            }

            .section-title {
                font-size: 2rem;
            }

            .hero {
                margin-top: 80px;
            }

            .hero h1 {
                font-size: 2rem;
            }

            .hero p {
                font-size: 1rem;
            }
        }

        /* SCROLL ANIMATION */
        .fade-in {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.6s ease, transform 0.6s ease;
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- NAVBAR -->
    <nav>
        <div class="navbar-content">
            <div class="logo">VB</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#experience">Experience</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

    <!-- HERO SECTION -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>
                Hi, I'm <span class="highlight">Venkata Babu</span>
                <br>Python Developer & <span class="highlight">GenAI Engineer</span>
            </h1>
            <p>Building intelligent applications with Python, LangChain, and Generative AI. Full-stack developer passionate about solving real-world problems.</p>
            
            <div class="cta-buttons">
                <a href="#projects" class="btn btn-primary">View My Work</a>
                <a href="#contact" class="btn btn-secondary">Get In Touch</a>
            </div>

            <div class="social-links">
                <a href="mailto:venkatababupasupuleti@gmail.com" title="Email">✉</a>
                <a href="https://linkedin.com/in/pasupuletivenkatababu" target="_blank" title="LinkedIn">in</a>
                <a href="https://github.com" target="_blank" title="GitHub">⚙</a>
            </div>
        </div>
    </section>

    <!-- ABOUT SECTION -->
    <section id="about" class="fade-in">
        <div class="container">
            <h2 class="section-title">About Me</h2>
            
            <div class="about-grid">
                <div class="about-text">
                    <h3>Python Developer | GenAI Engineer | Full-Stack Developer</h3>
                    <p>
                        I'm an aspiring Software Engineer with hands-on experience in Generative AI, LangChain, RAG applications, and modern web development. I have a strong background in engineering with a B.Tech degree from CMR Engineering College.
                    </p>
                    <p>
                        My passion is building intelligent applications that solve real-world problems. I combine backend expertise (Python) with frontend skills (React) to create complete solutions. Currently exploring the cutting-edge possibilities of Generative AI and Large Language Models.
                    </p>
                    <p>
                        When I'm not coding, I'm learning new technologies, contributing to open-source projects, and staying updated with the latest trends in AI and web development.
                    </p>
                </div>

                <div class="skills-grid">
                    <div class="skill-card fade-in">
                        <h4>🤖 Generative AI</h4>
                        <p>LangChain, RAG, Prompt Engineering, Gemini API, FAISS</p>
                    </div>
                    <div class="skill-card fade-in">
                        <h4>🐍 Backend</h4>
                        <p>Python, REST APIs, Problem Solving, System Design</p>
                    </div>
                    <div class="skill-card fade-in">
                        <h4>⚛️ Frontend</h4>
                        <p>React.js, JavaScript, HTML5, CSS3, Responsive Design</p>
                    </div>
                    <div class="skill-card fade-in">
                        <h4>🔧 Tools & More</h4>
                        <p>Git, GitHub, Streamlit, REST APIs, Database Design</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- PROJECTS SECTION -->
    <section id="projects" class="fade-in">
        <div class="container">
            <h2 class="section-title">Featured Projects</h2>
            
            <div class="projects-grid">
                <!-- Project 1 -->
                <div class="project-card fade-in">
                    <div class="project-header">
                        <h3 class="project-title">PDF Chatbot with RAG</h3>
                        <p class="project-subtitle">Generative AI Application</p>
                        <div class="project-tags">
                            <span class="tag">Python</span>
                            <span class="tag">LangChain</span>
                            <span class="tag">RAG</span>
                            <span class="tag">Streamlit</span>
                        </div>
                    </div>
                    <div class="project-body">
                        <p class="project-description">
                            Intelligent document analysis system that reads PDFs and provides context-aware responses using Retrieval-Augmented Generation (RAG) architecture.
                        </p>
                        <ul class="project-features">
                            <li>Intelligent document parsing with FAISS vector database</li>
                            <li>Context-aware responses powered by Gemini API</li>
                            <li>Interactive Streamlit interface</li>
                            <li>Real-time PDF processing</li>
                        </ul>
                        <a href="#" class="btn btn-primary" style="width: 100%; text-align: center;">Learn More</a>
                    </div>
                </div>

                <!-- Project 2 -->
                <div class="project-card fade-in">
                    <div class="project-header">
                        <h3 class="project-title">AI Resume Analyzer</h3>
                        <p class="project-subtitle">Career Development Tool</p>
                        <div class="project-tags">
                            <span class="tag">Python</span>
                            <span class="tag">Gemini API</span>
                            <span class="tag">NLP</span>
                            <span class="tag">Streamlit</span>
                        </div>
                    </div>
                    <div class="project-body">
                        <p class="project-description">
                            Automated resume parsing and analysis tool using Generative AI for skill extraction and career recommendations.
                        </p>
                        <ul class="project-features">
                            <li>Automatic skill extraction from CVs</li>
                            <li>Job match analysis with recommendations</li>
                            <li>Career gap identification</li>
                            <li>Improvement suggestions</li>
                        </ul>
                        <a href="#" class="btn btn-primary" style="width: 100%; text-align: center;">Learn More</a>
                    </div>
                </div>

                <!-- Project 3 -->
                <div class="project-card fade-in">
                    <div class="project-header">
                        <h3 class="project-title">Doorstep Repair Service</h3>
                        <p class="project-subtitle">Web Application</p>
                        <div class="project-tags">
                            <span class="tag">React</span>
                            <span class="tag">JavaScript</span>
                            <span class="tag">HTML5</span>
                            <span class="tag">CSS3</span>
                        </div>
                    </div>
                    <div class="project-body">
                        <p class="project-description">
                            Complete service booking platform for mobile repair services with intuitive user interface and service management.
                        </p>
                        <ul class="project-features">
                            <li>Service browsing and selection</li>
                            <li>Real-time service booking</li>
                            <li>Customer inquiry forms</li>
                            <li>Responsive mobile design</li>
                        </ul>
                        <a href="#" class="btn btn-primary" style="width: 100%; text-align: center;">Learn More</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- EXPERIENCE SECTION -->
    <section id="experience" class="fade-in">
        <div class="container">
            <h2 class="section-title">Professional Experience</h2>
            
            <div class="experience-timeline">
                <div class="experience-item fade-in">
                    <div class="experience-dot"></div>
                    <div class="experience-card">
                        <h3 class="experience-title">Python Developer | GenAI Projects</h3>
                        <p class="experience-date">January 2026 - March 2026</p>
                        <p class="experience-description">
                            Built production-ready AI applications using Python, LangChain, and RAG. Developed PDF Chatbot with intelligent document analysis and AI Resume Analyzer with automated skill extraction. Implemented advanced prompt engineering for optimal AI model performance.
                        </p>
                    </div>
                </div>

                <div class="experience-item fade-in">
                    <div class="experience-dot"></div>
                    <div class="experience-card">
                        <h3 class="experience-title">Frontend Developer | React Projects</h3>
                        <p class="experience-date">October 2025 - January 2026</p>
                        <p class="experience-description">
                            Developed responsive web applications using React.js with focus on user experience. Built service booking platforms with complete UI/UX implementation. Created reusable component library and implemented mobile-first responsive design across all projects.
                        </p>
                    </div>
                </div>

                <div class="experience-item fade-in">
                    <div class="experience-dot"></div>
                    <div class="experience-card">
                        <h3 class="experience-title">B.Tech in Mechanical Engineering</h3>
                        <p class="experience-date">2020 - 2024</p>
                        <p class="experience-description">
                            CMR Engineering College, Hyderabad. Developed strong analytical and problem-solving skills through engineering coursework. Transitioned to software development with focus on Python and AI technologies.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CONTACT SECTION -->
    <section id="contact" class="fade-in">
        <div class="container">
            <h2 class="section-title">Get In Touch</h2>
            
            <div class="contact-content">
                <p style="font-size: 1.1rem; color: var(--text-secondary); margin-bottom: 2rem;">
                    I'm always interested in hearing about new projects and opportunities. Whether you have a question or just want to say hi, feel free to reach out!
                </p>

                <div class="contact-info">
                    <div class="contact-item">
                        <strong>📧 Email:</strong>
                        <a href="mailto:venkatababupasupuleti@gmail.com">venkatababupasupuleti@gmail.com</a>
                    </div>
                    <div class="contact-item">
                        <strong>📱 Phone:</strong>
                        <a href="tel:+919640501890">+91-9640501890</a>
                    </div>
                    <div class="contact-item">
                        <strong>🔗 LinkedIn:</strong>
                        <a href="https://linkedin.com/in/pasupuletivenkatababu" target="_blank">linkedin.com/in/pasupuletivenkatababu</a>
                    </div>
                    <div class="contact-item">
                        <strong>📍 Location:</strong>
                        <span>Hyderabad, Telangana, India</span>
                    </div>
                </div>

                <div style="margin-top: 2.5rem;">
                    <a href="mailto:venkatababupasupuleti@gmail.com" class="btn btn-primary">Send Me an Email</a>
                </div>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer>
        <div class="container">
            <p>&copy; 2026 Pasupuleti Venkata Babu. All rights reserved.</p>
            <p style="margin-top: 1rem; font-size: 0.9rem;">
                Crafted with 💙 | Python Developer | GenAI Engineer
            </p>
        </div>
    </footer>

    <script>
        // Smooth scroll animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -100px 0px'
        };

        const observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));

        // Scroll to section behavior
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                if (this.getAttribute('href') !== '#') {
                    e.preventDefault();
                    const target = document.querySelector(this.getAttribute('href'));
                    if (target) {
                        target.scrollIntoView({ behavior: 'smooth' });
                    }
                }
            });
        });

        // Add animation on load
        window.addEventListener('load', () => {
            document.querySelectorAll('.fade-in').forEach((el, index) => {
                setTimeout(() => {
                    el.style.animation = `fadeInUp 0.6s ease-out forwards`;
                }, index * 100);
            });
        });
    </script>
</body>
</html>
