<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Web Developer Internship | Cognifyz Technologies</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #2563eb;
            --primary-dark: #1d4ed8;
            --secondary: #f59e0b;
            --dark: #1e293b;
            --light: #f8fafc;
            --gray: #94a3b8;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header */
        header {
            background: linear-gradient(135deg, var(--primary), var(--primary-dark));
            color: white;
            padding: 20px 0;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 24px;
            font-weight: 700;
            display: flex;
            align-items: center;
        }
        
        .logo i {
            margin-right: 10px;
            color: var(--secondary);
        }
        
        .nav-links {
            display: flex;
            gap: 30px;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
        }
        
        .nav-links a:hover {
            color: var(--secondary);
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1499951360447-b19be8fe80f5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 100px 0;
            text-align: center;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            animation: fadeIn 1s ease;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 30px;
            animation: fadeIn 1.5s ease;
        }
        
        .cta-button {
            display: inline-block;
            background-color: var(--secondary);
            color: var(--dark);
            padding: 12px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            animation: fadeIn 2s ease;
            box-shadow: 0 4px 15px rgba(245, 158, 11, 0.4);
        }
        
        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(245, 158, 11, 0.6);
            background-color: #e69009;
        }
        
        /* Internship Info */
        .info-section {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            font-size: 2.2rem;
            color: var(--primary);
            position: relative;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background-color: var(--secondary);
            border-radius: 2px;
        }
        
        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .info-card {
            background-color: white;
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
            text-align: center;
        }
        
        .info-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .info-card i {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 20px;
        }
        
        .info-card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: var(--primary);
        }
        
        /* Qualifications */
        .qualifications {
            background-color: var(--primary);
            color: white;
            padding: 80px 0;
        }
        
        .qualifications .section-title {
            color: white;
        }
        
        .qualifications .section-title::after {
            background-color: var(--secondary);
        }
        
        .skills-list {
            max-width: 800px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }
        
        .skill-item {
            background-color: rgba(255, 255, 255, 0.1);
            padding: 20px;
            border-radius: 8px;
            text-align: center;
            transition: all 0.3s ease;
        }
        
        .skill-item:hover {
            background-color: rgba(255, 255, 255, 0.2);
            transform: scale(1.05);
        }
        
        .skill-item i {
            font-size: 1.8rem;
            margin-bottom: 10px;
            color: var(--secondary);
        }
        
        /* CTA Section */
        .cta-section {
            padding: 80px 0;
            text-align: center;
            background-color: white;
        }
        
        .cta-section h2 {
            font-size: 2rem;
            margin-bottom: 20px;
            color: var(--primary);
        }
        
        .cta-section p {
            max-width: 600px;
            margin: 0 auto 30px;
            color: var(--dark);
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 50px 0 20px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-bottom: 40px;
        }
        
        .footer-column h3 {
            font-size: 1.3rem;
            margin-bottom: 20px;
            color: var(--secondary);
        }
        
        .footer-column p, .footer-column a {
            color: var(--gray);
            margin-bottom: 10px;
            display: block;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .footer-column a:hover {
            color: var(--secondary);
        }
        
        .social-links {
            display: flex;
            gap: 15px;
        }
        
        .social-links a {
            color: white;
            background-color: rgba(255, 255, 255, 0.1);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            background-color: var(--secondary);
            color: var(--dark);
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: var(--gray);
            font-size: 0.9rem;
        }
        
        /* Animations */
        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .section-title {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <div class="logo">
                    <i class="fas fa-code"></i>
                    <span>Cognifyz Technologies</span>
                </div>
                <div class="nav-links">
                    <a href="#overview">Overview</a>
                    <a href="#benefits">Benefits</a>
                    <a href="#qualifications">Qualifications</a>
                    <a href="#apply">Apply</a>
                </div>
            </nav>
        </div>
    </header>
    
    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h1>Web Developer Internship Opportunities</h1>
            <p>Jumpstart your career with hands-on experience at Cognifyz Technologies. Our 3-6 month internship program is designed to transform your theoretical knowledge into practical skills.</p>
            <a href="#apply" class="cta-button">Apply Now</a>
        </div>
    </section>
    
    <!-- Overview Section -->
    <section id="overview" class="info-section">
        <div class="container">
            <h2 class="section-title">Program Overview</h2>
            <div class="info-grid">
                <div class="info-card">
                    <i class="fas fa-calendar-alt"></i>
                    <h3>Duration</h3>
                    <p>Our internship program runs for 3-6 months, with flexible start dates throughout the year to accommodate your academic schedule.</p>
                </div>
                <div class="info-card">
                    <i class="fas fa-laptop-code"></i>
                    <h3>Real Projects</h3>
                    <p>Work on live projects for real clients, gaining experience that will make your resume stand out in the competitive tech industry.</p>
                </div>
                <div class="info-card">
                    <i class="fas fa-users"></i>
                    <h3>Team Environment</h3>
                    <p>Collaborate with our team of experienced developers, designers, and project managers in an agile work environment.</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Benefits Section -->
    <section id="benefits" class="info-section" style="background-color: #f5f7fa;">
        <div class="container">
            <h2 class="section-title">Internship Benefits</h2>
            <div class="info-grid">
                <div class="info-card">
                    <i class="fas fa-chalkboard-teacher"></i>
                    <h3>Mentorship</h3>
                    <p>Receive one-on-one guidance from senior developers who will help you grow your skills and navigate your career path.</p>
                </div>
                <div class="info-card">
                    <i class="fas fa-certificate"></i>
                    <h3>Certificate</h3>
                    <p>Earn a completion certificate and letter of recommendation based on your performance during the internship.</p>
                </div>
                <div class="info-card">
                    <i class="fas fa-briefcase"></i>
                    <h3>Career Opportunities</h3>
                    <p>Top performers may receive full-time employment offers or referrals to our partner companies.</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Qualifications Section -->
    <section id="qualifications" class="qualifications">
        <div class="container">
            <h2 class="section-title">Desired Qualifications</h2>
            <div class="skills-list">
                <div class="skill-item">
                    <i class="fab fa-html5"></i>
                    <p>HTML5 & CSS3</p>
                </div>
                <div class="skill-item">
                    <i class="fab fa-js"></i>
                    <p>JavaScript</p>
                </div>
                <div class="skill-item">
                    <i class="fab fa-react"></i>
                    <p>React.js</p>
                </div>
                <div class="skill-item">
                    <i class="fab fa-node-js"></i>
                    <p>Node.js</p>
                </div>
                <div class="skill-item">
                    <i class="fas fa-database"></i>
                    <p>SQL/NoSQL</p>
                </div>
                <div class="skill-item">
                    <i class="fab fa-git-alt"></i>
                    <p>Git Version Control</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- CTA Section -->
    <section id="apply" class="cta-section">
        <div class="container">
            <h2>Ready to Launch Your Career?</h2>
            <p>Applications are reviewed on a rolling basis. Don't miss this opportunity to work with industry experts on cutting-edge projects.</p>
            <a href="#" class="cta-button">Apply Now</a>
            <p style="margin-top: 20px;">or <a href="#" style="color: var(--primary); text-decoration: underline;">Learn More</a> about the program</p>
        </div>
    </section>
    
    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>About Cognifyz</h3>
                    <p>We're a leading tech company specializing in web development, AI solutions, and digital transformation services.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-github"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Contact Us</h3>
                    <a href="mailto:internships@cognifyz.com"><i class="fas fa-envelope"></i> internships@cognifyz.com</a>
                    <a href="tel:+11234567890"><i class="fas fa-phone"></i> +1 (123) 456-7890</a>
                    <a href="#"><i class="fas fa-map-marker-alt"></i> 123 Tech Park, Innovation City</a>
                </div>
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <a href="#overview">Program Overview</a>
                    <a href="#benefits">Benefits</a>
                    <a href="#qualifications">Qualifications</a>
                    <a href="#apply">Application</a>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Cognifyz Technologies. All rights reserved.</p>
            </div>
        </div>
    </footer>
    
    <script>
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
        
        // Animation on scroll
        const observerOptions = {
            threshold: 0.1
        };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('animated');
                }
            });
        }, observerOptions);
        
        document.querySelectorAll('.info-card, .skill-item').forEach(card => {
            card.classList.add('animated');
            observer.observe(card);
        });
    </script>
</body>
</html>
