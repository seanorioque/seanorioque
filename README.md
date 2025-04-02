<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sean Orioque - GitHub Profile</title>
    <style>
        :root {
            --primary-color: #0366d6;
            --secondary-color: #2ea44f;
            --dark-bg: #0d1117;
            --light-bg: #ffffff;
            --text-primary: #24292e;
            --text-secondary: #586069;
            --accent: #f1e05a;
            --border: #e1e4e8;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica, Arial, sans-serif;
            line-height: 1.6;
            color: var(--text-primary);
            background-color: var(--light-bg);
            margin: 0;
            padding: 20px;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
        }

        .header {
            display: flex;
            align-items: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 1px solid var(--border);
            position: relative;
        }

        .profile-img {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            margin-right: 30px;
            border: 4px solid var(--primary-color);
        }

        .header-text {
            flex: 1;
        }

        h1 {
            color: var(--primary-color);
            margin: 0 0 10px 0;
            font-size: 2.5rem;
            position: relative;
            display: inline-block;
        }

        h1::after {
            content: "";
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 60%;
            height: 4px;
            background: linear-gradient(90deg, var(--primary-color), var(--secondary-color));
            border-radius: 2px;
        }

        .tagline {
            font-size: 1.2rem;
            color: var(--text-secondary);
            margin-bottom: 15px;
            font-style: italic;
        }

        .bio {
            font-size: 1.1rem;
            line-height: 1.7;
            margin-bottom: 20px;
        }

        .section {
            margin-bottom: 30px;
            position: relative;
            padding: 20px;
            border-radius: 8px;
            transition: all 0.3s ease;
            border-left: 4px solid var(--primary-color);
            background-color: #f6f8fa;
        }

        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }

        h2 {
            color: var(--primary-color);
            margin-top: 0;
            font-size: 1.5rem;
            display: flex;
            align-items: center;
        }

        h2 i {
            margin-right: 10px;
            font-size: 1.2em;
        }

        ul {
            list-style-type: none;
            padding: 0;
        }

        li {
            margin-bottom: 15px;
            position: relative;
            padding-left: 25px;
        }

        li::before {
            content: "▹";
            position: absolute;
            left: 0;
            color: var(--secondary-color);
            font-size: 1.2em;
        }

        .certifications li {
            padding-left: 30px;
            margin-bottom: 20px;
        }

        .certifications li::before {
            content: "🏆";
            font-size: 1.3em;
        }

        a {
            color: var(--primary-color);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.2s;
            position: relative;
        }

        a:hover {
            color: var(--secondary-color);
        }

        a::after {
            content: "";
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -2px;
            left: 0;
            background-color: var(--secondary-color);
            transition: width 0.3s;
        }

        a:hover::after {
            width: 100%;
        }

        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
        }

        .skill-category {
            flex: 1;
            min-width: 200px;
        }

        .skill-badge {
            display: inline-block;
            background-color: #e7f3ff;
            color: var(--primary-color);
            padding: 5px 12px;
            border-radius: 15px;
            margin: 5px;
            font-size: 0.9rem;
            border: 1px solid var(--primary-color);
            transition: all 0.2s;
        }

        .skill-badge:hover {
            background-color: var(--primary-color);
            color: white;
            transform: scale(1.05);
        }

        .contact {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 20px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            padding: 10px 15px;
            background-color: #f0f4f8;
            border-radius: 8px;
            transition: all 0.3s;
        }

        .contact-item:hover {
            background-color: var(--primary-color);
        }

        .contact-item:hover a {
            color: white;
        }

        .contact-item:hover a::after {
            background-color: white;
        }

        .contact-item i {
            margin-right: 10px;
            font-size: 1.2em;
            color: var(--primary-color);
        }

        .contact-item:hover i {
            color: white;
        }

        .footer {
            text-align: center;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid var(--border);
            color: var(--text-secondary);
            font-size: 0.9rem;
        }

        .stats {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
        }

        .theme-toggle {
            position: absolute;
            top: 20px;
            right: 20px;
            background: none;
            border: none;
            cursor: pointer;
            font-size: 1.5rem;
            color: var(--text-secondary);
            transition: color 0.3s;
        }

        .theme-toggle:hover {
            color: var(--primary-color);
        }

        @media (max-width: 768px) {
            .header {
                flex-direction: column;
                text-align: center;
            }
            
            .profile-img {
                margin-right: 0;
                margin-bottom: 20px;
            }
            
            h1::after {
                left: 20%;
                width: 60%;
            }
            
            .skills {
                flex-direction: column;
            }
            
            .stats {
                flex-direction: column;
                align-items: center;
            }
            
            .theme-toggle {
                top: 10px;
                right: 10px;
            }
        }
    </style>
    <!-- Font Awesome for icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
</head>
<body>
    <div class="container">
        <button class="theme-toggle" id="themeToggle">
            <i class="fas fa-moon"></i>
        </button>
        
        <div class="header">
            <img src="/api/placeholder/120/120" alt="Sean Orioque" class="profile-img">
            <div class="header-text">
                <h1>Sean Orioque</h1>
                <div class="tagline">Aspiring Developer | Computer Science Student</div>
                <p class="bio">
                    Enthusiastic about building small projects to strengthen my coding skills and gain practical experience. 
                    Eager to collaborate with others and contribute to open-source projects while continuously expanding my 
                    knowledge in software development. Committed to lifelong learning and exploring new technologies to create 
                    innovative solutions.
                </p>
            </div>
        </div>

        <div class="section education">
            <h2><i class="fas fa-graduation-cap"></i> EDUCATION</h2>
            <ul>
                <li>
                    <strong>BS Computer Science</strong><br>
                    New Era University (2024-Present)
                </li>
            </ul>
        </div>

        <div class="section certifications">
            <h2><i class="fas fa-certificate"></i> CERTIFICATIONS</h2>
            <ul>
                <li>
                    <a href="https://courses.cognitiveclass.ai/certificates/8cf71d0105af4257a31e3bc29aaa848e" target="_blank">
                        SQL and Relational Databases 101
                    </a>
                </li>
                <li>
                    <a href="https://catalog-education.oracle.com/ords/certview/sharebadge?id=D3253DC3EB8FCB05E2C2FD8EDE344A0F1E0F72A832E2615D15EEC51B18DF406C" target="_blank">
                        Oracle Cloud Infrastructure 2024 Certified Foundations Associate
                    </a>
                </li>
                <li>
                    <a href="https://catalog-education.oracle.com/ords/certview/sharebadge?id=D3253DC3EB8FCB05E2C2FD8EDE344A0FB4E8D5C102A2F2A56F16A12E59DE2166" target="_blank">
                        Oracle Cloud Infrastructure 2024 Data Certified Foundations Associate
                    </a>
                </li>
                <li>
                    <a href="https://catalog-education.oracle.com/ords/certview/sharebadge?id=AB3357B6A26A740871EA824AB39DF1A132660906EF0724BB0CB45E3FD8079FE9" target="_blank">
                        Oracle Cloud Infrastructure 2024 Certified AI Foundations Associate
                    </a>
                </li>
            </ul>
        </div>

        <div class="section">
            <h2><i class="fas fa-code"></i> SKILL SETS</h2>
            <div class="skills">
                <div class="skill-category">
                    <h3>Programming</h3>
                    <div class="skill-badge">Java</div>
                </div>
                <div class="skill-category">
                    <h3>Databases</h3>
                    <div class="skill-badge">IBM DB2 Cloud</div>
                    <div class="skill-badge">SQL</div>
                </div>
                <div class="skill-category">
                    <h3>Tools</h3>
                    <div class="skill-badge">Lucidchart</div>
                    <div class="skill-badge">Visual Studio Code</div>
                    <div class="skill-badge">Eclipse</div>
                    <div class="skill-badge">HTML</div>
                </div>
            </div>
        </div>

        <div class="section">
            <h2><i class="fas fa-project-diagram"></i> PROJECTS</h2>
            <p style="text-align: center; color: var(--text-secondary);">
                Currently building my portfolio. Check back soon!
            </p>
        </div>

        <div class="section">
            <h2><i class="fas fa-handshake"></i> LET'S CONNECT!</h2>
            <div class="contact">
                <div class="contact-item">
                    <i class="fab fa-linkedin"></i>
                    <a href="https://www.linkedin.com/in/sean-orioque" target="_blank">Sean Orioque</a>
                </div>
                <div class="contact-item">
                    <i class="fas fa-envelope"></i>
                    <a href="mailto:seanorioque23@gmail.com">seanorioque23@gmail.com</a>
                </div>
                <div class="contact-item">
                    <i class="fab fa-github"></i>
                    <a href="#">GitHub Profile</a>
                </div>
            </div>
        </div>

        <div class="stats">
            <img src="/api/placeholder/400/120" alt="GitHub stats">
        </div>

        <div class="footer">
            <p>© 2025 Sean Orioque | Last Updated: April 2025</p>
        </div>
    </div>

    <script>
        // Theme toggle functionality
        const themeToggle = document.getElementById('themeToggle');
        const body = document.body;
        const container = document.querySelector('.container');
        const toggleIcon = themeToggle.querySelector('i');

        themeToggle.addEventListener('click', () => {
            body.classList.toggle('dark-mode');
            
            if (toggleIcon.classList.contains('fa-moon')) {
                toggleIcon.classList.remove('fa-moon');
                toggleIcon.classList.add('fa-sun');
                
                document.documentElement.style.setProperty('--primary-color', '#58a6ff');
                document.documentElement.style.setProperty('--secondary-color', '#3fb950');
                document.documentElement.style.setProperty('--text-primary', '#c9d1d9');
                document.documentElement.style.setProperty('--text-secondary', '#8b949e');
                document.documentElement.style.setProperty('--light-bg', '#0d1117');
                document.documentElement.style.setProperty('--border', '#30363d');
                
                document.querySelectorAll('.section').forEach(section => {
                    section.style.backgroundColor = '#161b22';
                });
                
                document.querySelectorAll('.contact-item').forEach(item => {
                    item.style.backgroundColor = '#161b22';
                });
                
                document.querySelectorAll('.skill-badge').forEach(badge => {
                    badge.style.backgroundColor = '#1f2937';
                });
            } else {
                toggleIcon.classList.remove('fa-sun');
                toggleIcon.classList.add('fa-moon');
                
                document.documentElement.style.setProperty('--primary-color', '#0366d6');
                document.documentElement.style.setProperty('--secondary-color', '#2ea44f');
                document.documentElement.style.setProperty('--text-primary', '#24292e');
                document.documentElement.style.setProperty('--text-secondary', '#586069');
                document.documentElement.style.setProperty('--light-bg', '#ffffff');
                document.documentElement.style.setProperty('--border', '#e1e4e8');
                
                document.querySelectorAll('.section').forEach(section => {
                    section.style.backgroundColor = '#f6f8fa';
                });
                
                document.querySelectorAll('.contact-item').forEach(item => {
                    item.style.backgroundColor = '#f0f4f8';
                });
                
                document.querySelectorAll('.skill-badge').forEach(badge => {
                    badge.style.backgroundColor = '#e7f3ff';
                });
            }
        });
    </script>
</body>
</html>
