
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Portfolio</title>
    <style>
        /* General Styles */
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #1e1e2f;
            color: #fff;
            transition: background-color 0.5s, color 0.5s;
        }

        body.light-mode {
            background-color: #f4f4f9;
            color: #333;
        }

        /* Navigation Bar */
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px;
            background: rgba(30, 30, 47, 0.9);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        nav a {
            color: #fff;
            text-decoration: none;
            margin: 0 15px;
            font-size: 1.1rem;
        }

        nav a:hover {
            color: #2575fc;
        }

        /* Header Section */
        header {
            background: linear-gradient(135deg, #6a11cb, #2575fc);
            padding: 150px 20px 100px;
            text-align: center;
            color: white;
            position: relative;
            overflow: hidden;
        }

        header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.1);
            z-index: 1;
        }

        h1 {
            font-size: 3rem;
            margin: 0;
            z-index: 2;
            position: relative;
        }

        h2 {
            font-size: 2rem;
            text-align: center;
            margin: 40px 0;
        }

        /* About Me Section */
        #about {
            padding: 20px;
            text-align: center;
        }

        .about-content {
            max-width: 600px;
            margin: 0 auto;
        }

        /* Projects Section */
        #projects {
            padding: 20px;
        }

        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            padding: 20px;
        }

        .project-card {
            background: #2c2c44;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-10px);
        }

        /* Skills Section */
        #skills {
            padding: 20px;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 20px;
            padding: 20px;
        }

        .skill-card {
            background: #2c2c44;
            padding: 20px;
            text-align: center;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        .skill-card i {
            font-size: 2rem;
            margin-bottom: 10px;
        }

        /* Contact Section */
        #contact {
            padding: 20px;
            text-align: center;
        }

        .contact-form {
            max-width: 600px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .contact-form input, .contact-form textarea {
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-size: 1rem;
            background: #2c2c44;
            color: #fff;
        }

        .contact-form button {
            padding: 10px;
            background: #2575fc;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
        }

        .contact-form button:hover {
            background: #1a5bbf;
        }

        /* Blog Section */
        #blog {
            padding: 20px;
        }

        .blog-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            padding: 20px;
        }

        .blog-card {
            background: #2c2c44;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        /* Footer */
        footer {
            background: #1e1e2f;
            text-align: center;
            padding: 20px;
            margin-top: 40px;
        }

        /* Dark/Light Mode Toggle */
        .mode-toggle {
            position: fixed;
            top: 20px;
            right: 20px;
            background: #2575fc;
            color: white;
            border: none;
            padding: 10px;
            border-radius: 50%;
            cursor: pointer;
            z-index: 1000;
        }

        .mode-toggle:hover {
            background: #1a5bbf;
        }

        /* Light Mode Adjustments */
        body.light-mode nav {
            background: rgba(244, 244, 249, 0.9);
        }

        body.light-mode nav a {
            color: #333;
        }

        body.light-mode .project-card,
        body.light-mode .skill-card,
        body.light-mode .blog-card,
        body.light-mode .contact-form input,
        body.light-mode .contact-form textarea {
            background: #fff;
            color: #333;
        }

        body.light-mode .contact-form input::placeholder,
        body.light-mode .contact-form textarea::placeholder {
            color: #666;
        }
    </style>
</head>
<body>
    <!-- Navigation Bar -->
    <nav>
        <div>
            <a href="#about">About</a>
            <a href="#projects">Projects</a>
            <a href="#skills">Skills</a>
            <a href="#contact">Contact</a>
            <a href="#blog">Blog</a>
        </div>
    </nav>

    <!-- Dark/Light Mode Toggle -->
    <button class="mode-toggle" onclick="toggleMode()">🌓</button>

    <!-- Header Section -->
    <header>
        <div class="header-content">
            <h1>Welcome to My Portfolio</h1>
            <p>Computer Science & Technology Student</p>
        </div>
    </header>

    <!-- About Me Section -->
    <section id="about">
        <h2>About Me</h2>
        <div class="about-content">
            <p>Hello! I'm a passionate Computer Science student with a strong interest in software development, machine learning, and web technologies. I love solving problems and building innovative projects.</p>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <h2>Projects</h2>
        <div class="project-grid">
            <div class="project-card">
                <h3>Project 1: Web Scraper</h3>
                <p>A Python-based web scraper for data extraction.</p>
            </div>
            <div class="project-card">
                <h3>Project 2: Chat Application</h3>
                <p>A real-time chat app using Node.js and Socket.io.</p>
            </div>
            <div class="project-card">
                <h3>Project 3: Machine Learning Model</h3>
                <p>A predictive model for stock prices using TensorFlow.</p>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills">
        <h2>Skills</h2>
        <div class="skills-grid">
            <div class="skill-card">
                <i>💻</i>
                <p>Python</p>
            </div>
            <div class="skill-card">
                <i>🌐</i>
                <p>JavaScript</p>
            </div>
            <div class="skill-card">
                <i>🎨</i>
                <p>HTML/CSS</p>
            </div>
            <div class="skill-card">
                <i>🤖</i>
                <p>Machine Learning</p>
            </div>
            <div class="skill-card">
                <i>🔧</i>
                <p>Node.js</p>
            </div>
            <div class="skill-card">
                <i>📦</i>
                <p>Git</p>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <h2>Contact Me</h2>
        <form class="contact-form">
            <input type="text" placeholder="Your Name" required>
            <input type="email" placeholder="Your Email" required>
            <textarea placeholder="Your Message" rows="5" required></textarea>
            <button type="submit">Send Message</button>
        </form>
    </section>

    <!-- Blog Section -->
    <section id="blog">
        <h2>Blog</h2>
        <div class="blog-grid">
            <div class="blog-card">
                <h3>Blog Post 1</h3>
                <p>This is a sample blog post about web development.</p>
            </div>
            <div class="blog-card">
                <h3>Blog Post 2</h3>
                <p>This is a sample blog post about machine learning.</p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2023 Your Name. All rights reserved.</p>
    </footer>

    <script>
        // Dark/Light Mode Toggle
        function toggleMode() {
            document.body.classList.toggle('light-mode');
        }

        // Header Animation
        document.addEventListener("DOMContentLoaded", () => {
            const header = document.querySelector("header");
            header.style.opacity = 0;
            setTimeout(() => {
                header.style.transition = "opacity 2s";
                header.style.opacity = 1;
            }, 500);
        });
    </script>
</body>
</html>
