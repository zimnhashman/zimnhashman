<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Awesome GitHub Profile</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Roboto+Mono:wght@400;700&family=Space+Grotesk:wght@400;700&display=swap');
        
        :root {
            --primary: #0d1117;
            --secondary: #161b22;
            --accent: #58a6ff;
            --text: #c9d1d9;
            --highlight: #ff7b72;
            --purple: #d2a8ff;
            --green: #3fb950;
            --orange: #ffa657;
            --border: #30363d;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            background-color: var(--primary);
            color: var(--text);
            font-family: 'Space Grotesk', sans-serif;
            line-height: 1.6;
            padding: 20px;
            max-width: 900px;
            margin: 0 auto;
        }
        
        .container {
            background-color: var(--secondary);
            border-radius: 16px;
            padding: 30px;
            border: 1px solid var(--border);
            box-shadow: 0 8px 30px rgba(0, 0, 0, 0.3);
        }
        
        .header {
            text-align: center;
            margin-bottom: 30px;
            position: relative;
        }
        
        .banner {
            background: linear-gradient(135deg, var(--accent), var(--purple));
            height: 150px;
            border-radius: 12px 12px 0 0;
            margin: -30px -30px 30px -30px;
            position: relative;
            overflow: hidden;
        }
        
        .banner::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('https://media.giphy.com/media/KzJkzjggfGN5Py6nkT/giphy.gif');
            background-size: cover;
            opacity: 0.2;
        }
        
        .profile {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 20px;
            margin-top: -75px;
        }
        
        .avatar {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 5px solid var(--secondary);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
            animation: float 6s ease-in-out infinite;
        }
        
        .intro {
            text-align: left;
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            color: var(--accent);
            font-family: 'Roboto Mono', monospace;
        }
        
        h2 {
            font-size: 1.5rem;
            margin: 20px 0 10px;
            color: var(--purple);
            border-bottom: 2px solid var(--border);
            padding-bottom: 5px;
        }
        
        h3 {
            font-size: 1.2rem;
            margin: 15px 0 10px;
            color: var(--green);
        }
        
        .tagline {
            font-size: 1.2rem;
            color: var(--highlight);
            margin-bottom: 15px;
        }
        
        .socials {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin: 20px 0;
        }
        
        .socials a {
            color: var(--text);
            font-size: 1.8rem;
            transition: all 0.3s ease;
        }
        
        .socials a:hover {
            color: var(--accent);
            transform: translateY(-3px);
        }
        
        .badges {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin: 20px 0;
        }
        
        .badge {
            background: var(--primary);
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 5px;
            border: 1px solid var(--border);
        }
        
        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin: 15px 0;
        }
        
        .skill {
            background: linear-gradient(135deg, var(--accent), var(--purple));
            color: var(--primary);
            padding: 6px 14px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 5px;
            transition: all 0.3s ease;
        }
        
        .skill:hover {
            transform: scale(1.05);
            box-shadow: 0 0 15px rgba(88, 166, 255, 0.5);
        }
        
        .projects {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin: 20px 0;
        }
        
        .project {
            background: var(--primary);
            border-radius: 12px;
            padding: 20px;
            border: 1px solid var(--border);
            transition: all 0.3s ease;
        }
        
        .project:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.4);
        }
        
        .project h3 {
            color: var(--orange);
            margin-bottom: 10px;
        }
        
        .gif-container {
            text-align: center;
            margin: 30px 0;
        }
        
        .gif-container img {
            max-width: 100%;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }
        
        .stats {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 30px 0;
        }
        
        .stat {
            text-align: center;
            background: var(--primary);
            padding: 15px;
            border-radius: 12px;
            border: 1px solid var(--border);
            min-width: 120px;
        }
        
        .stat-number {
            font-size: 2rem;
            font-weight: bold;
            color: var(--accent);
        }
        
        .stat-label {
            font-size: 0.9rem;
            color: var(--text);
        }
        
        .quote {
            text-align: center;
            font-style: italic;
            margin: 30px 0;
            padding: 20px;
            border-radius: 12px;
            background: var(--primary);
            border-left: 4px solid var(--highlight);
        }
        
        .footer {
            text-align: center;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid var(--border);
            color: var(--text);
            font-size: 0.9rem;
        }
        
        .highlight {
            color: var(--highlight);
            font-weight: bold;
        }
        
        /* Animations */
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }
        
        @keyframes glow {
            0% { text-shadow: 0 0 5px var(--accent); }
            50% { text-shadow: 0 0 20px var(--accent); }
            100% { text-shadow: 0 0 5px var(--accent); }
        }
        
        .animated-text {
            animation: glow 2s ease-in-out infinite;
        }
        
        /* Responsive design */
        @media (max-width: 768px) {
            .profile {
                flex-direction: column;
                text-align: center;
            }
            
            .stats {
                flex-direction: column;
                align-items: center;
            }
            
            .stat {
                width: 100%;
                max-width: 200px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="banner"></div>
        
        <div class="header">
            <div class="profile">
                <img src="https://avatars.githubusercontent.com/u/example" alt="Profile" class="avatar">
                <div class="intro">
                    <h1>Nhaniso J. Undenge</h1>
                    <p class="tagline">Mobile & Full Stack Developer | Blockchain & AI Enthusiast</p>
                </div>
            </div>
            
            <div class="socials">
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-linkedin"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-dev"></i></a>
                <a href="#"><i class="fas fa-envelope"></i></a>
            </div>
            
            <div class="badges">
                <div class="badge"><i class="fas fa-map-marker-alt"></i> Harare, Zimbabwe</div>
                <div class="badge"><i class="fas fa-code"></i> Full Stack Developer</div>
                <div class="badge"><i class="fas fa-mobile-alt"></i> Mobile Developer</div>
                <div class="badge"><i class="fas fa-brain"></i> AI Enthusiast</div>
            </div>
        </div>
        
        <div class="gif-container">
            <img src="https://media.giphy.com/media/coxQHKASG60HrHtvkt/giphy.gif" alt="Coding GIF" width="500">
        </div>
        
        <h2>👨‍💻 About Me</h2>
        <p>Hello! I'm <span class="highlight">Nhaniso J. Undenge</span>, a passionate developer with 5+ years of experience in iOS and mobile development. I specialize in <span class="highlight">Flutter, Swift, and modern web technologies</span>.</p>
        
        <p>I've developed many cool applications on GitHub and built numerous commercial apps using Flutter. I'm passionate about <span class="highlight">Blockchain, Data Analytics, Computer Vision & Artificial Intelligence</span>. I'm quick to grasp new concepts and enjoy solving complex problems.</p>
        
        <div class="stats">
            <div class="stat">
                <div class="stat-number">5+</div>
                <div class="stat-label">Years Experience</div>
            </div>
            <div class="stat">
                <div class="stat-number">50+</div>
                <div class="stat-label">Projects</div>
            </div>
            <div class="stat">
                <div class="stat-number">15+</div>
                <div class="stat-label">Technologies</div>
            </div>
            <div class="stat">
                <div class="stat-number">∞</div>
                <div class="stat-label">Coffee Cups</div>
            </div>
        </div>
        
        <h2>🛠️ Technologies & Skills</h2>
        <div class="skills">
            <div class="skill"><i class="fab fa-flutter"></i> Flutter</div>
            <div class="skill"><i class="fab fa-swift"></i> Swift</div>
            <div class="skill"><i class="fab fa-android"></i> Android</div>
            <div class="skill"><i class="fab fa-js"></i> JavaScript</div>
            <div class="skill"><i class="fab fa-react"></i> React</div>
            <div class="skill"><i class="fab fa-node-js"></i> Node.js</div>
            <div class="skill"><i class="fab fa-python"></i> Python</div>
            <div class="skill"><i class="fas fa-database"></i> PostgreSQL</div>
            <div class="skill"><i class="fab fa-ethereum"></i> Blockchain</div>
            <div class="skill"><i class="fas fa-brain"></i> Machine Learning</div>
            <div class="skill"><i class="fas fa-robot"></i> AI</div>
            <div class="skill"><i class="fas fa-server"></i> Backend Development</div>
        </div>
        
        <div class="gif-container">
            <img src="https://media.giphy.com/media/L1R1tvI9svkIWwpVYr/giphy.gif" alt="Development GIF" width="500">
        </div>
        
        <h2>🚀 Projects</h2>
        <div class="projects">
            <div class="project">
                <h3><i class="fas fa-rocket"></i> Perigee Application</h3>
                <p>Flutter application developed for Kalekt Analytics with comprehensive testing for all mobile resolutions.</p>
            </div>
            
            <div class="project">
                <h3><i class="fas fa-extract"></i> Ditto Application</h3>
                <p>JavaScript-based data extraction tool for client data management.</p>
            </div>
            
            <div class="project">
                <h3><i class="fas fa-tools"></i> Kassi Tool</h3>
                <p>Data analysis tool with Java SpringBoot backend and Angular frontend.</p>
            </div>
            
            <div class="project">
                <h3><i class="fas fa-music"></i> Hitcore Music App</h3>
                <p>iOS application for music management with database setup and UI design.</p>
            </div>
        </div>
        
        <div class="quote">
            <p>"First, solve the problem. Then, write the code."</p>
            <p>- John Johnson</p>
        </div>
        
        <h2>📊 GitHub Stats</h2>
        <div class="gif-container">
            <img src="https://media.giphy.com/media/du3J3cXyzhj75IOgvA/giphy.gif" alt="GitHub Stats" width="500">
            <p><span class="animated-text">Loading awesome stats...</span></p>
        </div>
        
        <h2>📫 How to Reach Me</h2>
        <p>Feel free to reach out if you want to collaborate on something, have questions, or just want to connect!</p>
        
        <div class="skills">
            <div class="skill"><i class="fas fa-envelope"></i> nhanitech@gmail.com</div>
            <div class="skill"><i class="fas fa-phone"></i> +263 714 024267</div>
            <div class="skill"><i class="fab fa-linkedin"></i> LinkedIn</div>
            <div class="skill"><i class="fab fa-twitter"></i> Twitter</div>
        </div>
        
        <div class="gif-container">
            <img src="https://media.giphy.com/media/LmNwrBhejkK9EFP504/giphy.gif" alt="Contact Me" width="400">
        </div>
        
        <div class="footer">
            <p>Made with ❤️ by <span class="highlight">Nhaniso J. Undenge</span></p>
            <p>© 2023 - All rights reserved</p>
        </div>
    </div>

    <script>
        // Simple animation for elements when they come into view
        document.addEventListener('DOMContentLoaded', function() {
            const animatedElements = document.querySelectorAll('.skill, .project, .stat');
            
            animatedElements.forEach(element => {
                element.style.opacity = '0';
                element.style.transform = 'translateY(20px)';
                element.style.transition = 'all 0.5s ease';
            });
            
            setTimeout(() => {
                animatedElements.forEach((element, index) => {
                    setTimeout(() => {
                        element.style.opacity = '1';
                        element.style.transform = 'translateY(0)';
                    }, 100 + (index * 100));
                });
            }, 500);
            
            // Animated text effect
            const animatedText = document.querySelector('.animated-text');
            setInterval(() => {
                animatedText.style.animation = 'none';
                setTimeout(() => {
                    animatedText.style.animation = 'glow 2s ease-in-out infinite';
                }, 10);
            }, 4000);
        });
    </script>
</body>
</html>
