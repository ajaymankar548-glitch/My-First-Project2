<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Computer Science & Engineering Department</title>
    <style>
        /* Reset and Base Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary: #2c3e50;
            --secondary: #3498db;
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --text: #333;
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        body {
            color: var(--text);
            line-height: 1.6;
            background-color: #f9f9f9;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }

        /* Header Styles */
        header {
            background-color: var(--primary);
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: var(--shadow);
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo img {
            height: 50px;
        }

        .logo h1 {
            font-size: 1.5rem;
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 1.5rem;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }

        nav ul li a:hover {
            color: var(--secondary);
        }

        .mobile-menu {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(44, 62, 80, 0.8), rgba(44, 62, 80, 0.8)), 
                        url('https://images.unsplash.com/photo-1517077304055-6e89abbf09b0?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 5rem 0;
            text-align: center;
        }

        .hero h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 2rem;
        }

        .btn {
            display: inline-block;
            background-color: var(--secondary);
            color: white;
            padding: 0.8rem 1.5rem;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 600;
            transition: background-color 0.3s;
        }

        .btn:hover {
            background-color: #2980b9;
        }

        /* Sections */
        section {
            padding: 4rem 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            color: var(--primary);
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background-color: var(--secondary);
            margin: 10px auto;
        }

        /* About Section */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
            align-items: center;
        }

        .about-image img {
            width: 100%;
            border-radius: 10px;
            box-shadow: var(--shadow);
        }

        /* Programs Section */
        .programs-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .program-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: transform 0.3s;
        }

        .program-card:hover {
            transform: translateY(-10px);
        }

        .program-image {
            height: 200px;
            background-color: var(--secondary);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
            font-weight: bold;
        }

        .program-content {
            padding: 1.5rem;
        }

        /* Faculty Section */
        .faculty-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .faculty-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: var(--shadow);
            text-align: center;
        }

        .faculty-image {
            height: 250px;
            background-color: #ddd;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #777;
        }

        .faculty-content {
            padding: 1.5rem;
        }

        /* Research Section */
        .research-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
        }

        .research-areas {
            background-color: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: var(--shadow);
        }

        .research-areas ul {
            list-style-type: none;
        }

        .research-areas li {
            padding: 0.8rem 0;
            border-bottom: 1px solid #eee;
        }

        .research-areas li:last-child {
            border-bottom: none;
        }

        /* News Section */
        .news-container {
            background-color: white;
            border-radius: 10px;
            padding: 2rem;
            box-shadow: var(--shadow);
        }

        .news-item {
            padding: 1rem 0;
            border-bottom: 1px solid #eee;
        }

        .news-item:last-child {
            border-bottom: none;
        }

        .news-date {
            color: var(--secondary);
            font-weight: bold;
        }

        /* Contact Section */
        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
        }

        .contact-form {
            background-color: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: var(--shadow);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
        }

        .contact-info {
            background-color: var(--primary);
            color: white;
            padding: 2rem;
            border-radius: 10px;
        }

        .contact-info h3 {
            margin-bottom: 1.5rem;
            color: var(--secondary);
        }

        .contact-details {
            margin-bottom: 2rem;
        }

        .contact-details p {
            margin-bottom: 0.8rem;
            display: flex;
            align-items: center;
        }

        .contact-details i {
            margin-right: 10px;
            color: var(--secondary);
        }

        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 3rem 0 1rem;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-section h3 {
            margin-bottom: 1.5rem;
            color: var(--secondary);
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section ul li {
            margin-bottom: 0.8rem;
        }

        .footer-section a {
            color: #ddd;
            text-decoration: none;
            transition: color 0.3s;
        }

        .footer-section a:hover {
            color: var(--secondary);
        }

        .social-links {
            display: flex;
            gap: 1rem;
        }

        .social-links a {
            display: inline-block;
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            text-align: center;
            line-height: 40px;
            transition: background-color 0.3s;
        }

        .social-links a:hover {
            background-color: var(--secondary);
        }

        .copyright {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }

            nav ul {
                margin-top: 1rem;
                flex-direction: column;
                gap: 0.5rem;
            }

            .mobile-menu {
                display: block;
                position: absolute;
                top: 1rem;
                right: 1rem;
            }

            .about-content,
            .research-content,
            .contact-content {
                grid-template-columns: 1fr;
            }

            .hero h2 {
                font-size: 2rem;
            }

            .hero p {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <div class="logo-placeholder">CSE</div>
                    <h1>Computer Science & Engineering</h1>
                </div>
                <div class="mobile-menu">☰</div>
                <nav>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#about">About</a></li>
                        <li><a href="#programs">Programs</a></li>
                        <li><a href="#faculty">Faculty</a></li>
                        <li><a href="#research">Research</a></li>
                        <li><a href="#news">News</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <h2>Shaping the Future of Technology</h2>
            <p>Join our innovative Computer Science and Engineering department to explore cutting-edge technologies and develop solutions for tomorrow's challenges.</p>
            <a href="#programs" class="btn">Explore Programs</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <h2 class="section-title">About Our Department</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>Founded in 1990, our Computer Science and Engineering department has been at the forefront of technological education and research. We are committed to providing world-class education and fostering innovation in computing.</p>
                    <p>Our department offers a comprehensive curriculum that balances theoretical foundations with practical applications, preparing students for successful careers in industry, research, and entrepreneurship.</p>
                    <p>With state-of-the-art laboratories, experienced faculty, and strong industry connections, we provide an environment where students can thrive and develop into technology leaders.</p>
                </div>
                <div class="about-image">
                    <div class="image-placeholder" style="background-color: #3498db; height: 300px; display: flex; align-items: center; justify-content: center; color: white; border-radius: 10px;">
                        Department Building Image
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Programs Section -->
    <section id="programs" class="programs">
        <div class="container">
            <h2 class="section-title">Academic Programs</h2>
            <div class="programs-grid">
                <div class="program-card">
                    <div class="program-image" style="background-color: #3498db;">
                        B.Tech in CSE
                    </div>
                    <div class="program-content">
                        <h3>Bachelor of Technology</h3>
                        <p>Our four-year undergraduate program provides a strong foundation in computer science fundamentals along with specialized electives in emerging technologies.</p>
                        <a href="#" class="btn" style="margin-top: 1rem;">Learn More</a>
                    </div>
                </div>
                <div class="program-card">
                    <div class="program-image" style="background-color: #e74c3c;">
                        M.Tech in CSE
                    </div>
                    <div class="program-content">
                        <h3>Master of Technology</h3>
                        <p>Our postgraduate program offers advanced specializations in areas like AI, Data Science, Cybersecurity, and more with research opportunities.</p>
                        <a href="#" class="btn" style="margin-top: 1rem;">Learn More</a>
                    </div>
                </div>
                <div class="program-card">
                    <div class="program-image" style="background-color: #2ecc71;">
                        Ph.D. Programs
                    </div>
                    <div class="program-content">
                        <h3>Doctoral Programs</h3>
                        <p>Pursue cutting-edge research in various domains of computer science under the guidance of our experienced faculty members.</p>
                        <a href="#" class="btn" style="margin-top: 1rem;">Learn More</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Faculty Section -->
    <section id="faculty" class="faculty">
        <div class="container">
            <h2 class="section-title">Our Faculty</h2>
            <div class="faculty-grid">
                <div class="faculty-card">
                    <div class="faculty-image">
                        Faculty Image
                    </div>
                    <div class="faculty-content">
                        <h3>Dr. Sarah Johnson</h3>
                        <p>Professor & Head of Department</p>
                        <p>Specialization: Artificial Intelligence</p>
                    </div>
                </div>
                <div class="faculty-card">
                    <div class="faculty-image">
                        Faculty Image
                    </div>
                    <div class="faculty-content">
                        <h3>Dr. Michael Chen</h3>
                        <p>Professor</p>
                        <p>Specialization: Data Science</p>
                    </div>
                </div>
                <div class="faculty-card">
                    <div class="faculty-image">
                        Faculty Image
                    </div>
                    <div class="faculty-content">
                        <h3>Dr. Priya Sharma</h3>
                        <p>Associate Professor</p>
                        <p>Specialization: Cybersecurity</p>
                    </div>
                </div>
                <div class="faculty-card">
                    <div class="faculty-image">
                        Faculty Image
                    </div>
                    <div class="faculty-content">
                        <h3>Dr. Robert Williams</h3>
                        <p>Assistant Professor</p>
                        <p>Specialization: Cloud Computing</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Research Section -->
    <section id="research" class="research">
        <div class="container">
            <h2 class="section-title">Research Areas</h2>
            <div class="research-content">
                <div class="research-areas">
                    <h3>Key Research Domains</h3>
                    <ul>
                        <li>Artificial Intelligence & Machine Learning</li>
                        <li>Data Science & Big Data Analytics</li>
                        <li>Cybersecurity & Cryptography</li>
                        <li>Internet of Things (IoT)</li>
                        <li>Cloud Computing & Distributed Systems</li>
                        <li>Computer Vision & Image Processing</li>
                        <li>Human-Computer Interaction</li>
                        <li>Software Engineering</li>
                    </ul>
                </div>
                <div class="research-labs">
                    <h3>Research Labs & Facilities</h3>
                    <p>Our department houses several state-of-the-art research laboratories equipped with the latest hardware and software:</p>
                    <ul>
                        <li>AI & Robotics Lab</li>
                        <li>Data Analytics Center</li>
                        <li>Cybersecurity Research Lab</li>
                        <li>High Performance Computing Cluster</li>
                        <li>IoT Innovation Lab</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- News Section -->
    <section id="news" class="news">
        <div class="container">
            <h2 class="section-title">Department News</h2>
            <div class="news-container">
                <div class="news-item">
                    <div class="news-date">June 15, 2023</div>
                    <h3>Students Win National Hackathon Competition</h3>
                    <p>Our team of CSE students secured first place in the National Tech Innovation Hackathon with their AI-powered healthcare solution.</p>
                </div>
                <div class="news-item">
                    <div class="news-date">May 28, 2023</div>
                    <h3>New Research Grant Awarded</h3>
                    <p>The department has received a $2 million grant from the National Science Foundation for research in quantum computing applications.</p>
                </div>
                <div class="news-item">
                    <div class="news-date">April 10, 2023</div>
                    <h3>Industry Collaboration with Tech Giants</h3>
                    <p>We've partnered with leading technology companies to establish new internship programs and collaborative research initiatives.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <h2 class="section-title">Contact Us</h2>
            <div class="contact-content">
                <div class="contact-form">
                    <h3>Send us a Message</h3>
                    <form id="contactForm">
                        <div class="form-group">
                            <label for="name">Name</label>
                            <input type="text" id="name" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" required>
                        </div>
                        <div class="form-group">
                            <label for="subject">Subject</label>
                            <input type="text" id="subject" required>
                        </div>
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" rows="5" required></textarea>
                        </div>
                        <button type="submit" class="btn">Send Message</button>
                    </form>
                </div>
                <div class="contact-info">
                    <h3>Get in Touch</h3>
                    <div class="contact-details">
                        <p><i>📍</i>Priyadarshini J L College of Engineering and Technology,Nagpur-440002</p>
                        <p><i>📞</i> +91  5874-123-4567</p>
                        <p><i>✉️</i> cse.department@university.edu</p>
                    </div>
                    <div class="map-placeholder" style="background-color: rgba(255,255,255,0.1); height: 200px; display: flex; align-items: center; justify-content: center; border-radius: 5px;">
                        Interactive Map
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#about">About Us</a></li>
                        <li><a href="#programs">Programs</a></li>
                        <li><a href="#faculty">Faculty</a></li>
                        <li><a href="#research">Research</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Resources</h3>
                    <ul>
                        <li><a href="#">Student Portal</a></li>
                        <li><a href="#">Course Catalog</a></li>
                        <li><a href="#">Research Publications</a></li>
                        <li><a href="#">Alumni Network</a></li>
                        <li><a href="#">Career Services</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Connect With Us</h3>
                    <div class="social-links">
                        <a href="#">FB</a>
                        <a href="#">TW</a>
                        <a href="#">IG</a>
                        <a href="#">LI</a>
                        <a href="#">YT</a>
                    </div>
                    <p style="margin-top: 1.5rem;">Subscribe to our newsletter for updates</p>
                    <div class="newsletter-form" style="margin-top: 1rem;">
                        <input type="email" placeholder="Your email" style="padding: 0.5rem; width: 70%; border: none; border-radius: 3px;">
                        <button style="background: var(--secondary); color: white; border: none; padding: 0.5rem 1rem; border-radius: 3px; margin-left: 5px;">Subscribe</button>
                    </div>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2026 CSE Department. All rights reserved.</p>
                <p>&copy;WebDevwithAjay</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        document.querySelector('.mobile-menu').addEventListener('click', function() {
            document.querySelector('nav ul').classList.toggle('show');
        });

        // Smooth scrolling for navigation links
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                window.scrollTo({
                    top: targetElement.offsetTop - 80,
                    behavior: 'smooth'
                });
            });
        });

        // Form submission
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you for your message! We will get back to you soon.');
            this.reset();
        });

        // Simple animation on scroll
        window.addEventListener('scroll', function() {
            const sections = document.querySelectorAll('section');
            const navLinks = document.querySelectorAll('nav a');
            
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                if (pageYOffset >= sectionTop - 100) {
                    current = section.getAttribute('id');
                }
            });
            
            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href').substring(1) === current) {
                    link.classList.add('active');
                }
            });
        });
    </script>
</body>
</html>
