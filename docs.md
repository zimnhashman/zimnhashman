<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GitHub Profile README Generator</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #2d2b55;
            --secondary-color: #b831ae;
            --accent-color: #00a2ff;
            --light-color: #f8f8f2;
            --dark-color: #1e1e3f;
            --success-color: #a6e22e;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--dark-color);
            color: var(--light-color);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        header {
            text-align: center;
            padding: 40px 20px;
            background: linear-gradient(135deg, var(--primary-color), var(--dark-color));
            border-radius: 10px;
            margin-bottom: 30px;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
            position: relative;
            overflow: hidden;
        }
        
        .capsule-container {
            margin: 20px 0;
            height: 100px;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .capsule-text {
            font-size: 2rem;
            font-weight: bold;
            background: linear-gradient(90deg, #ff8a00, #e52e71, #9b59b6, #3498db);
            background-size: 300% 300%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: gradient 3s ease infinite, fadeIn 2s ease;
            text-shadow: 0 0 10px rgba(255, 255, 255, 0.3);
        }
        
        @keyframes gradient {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid var(--secondary-color);
            margin-bottom: 20px;
            animation: pulse 3s infinite;
            box-shadow: 0 0 20px rgba(184, 49, 174, 0.5);
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            color: var(--accent-color);
            animation: fadeIn 1s ease;
        }
        
        h2 {
            font-size: 1.8rem;
            margin: 20px 0;
            color: var(--secondary-color);
            border-bottom: 2px solid var(--secondary-color);
            padding-bottom: 5px;
            animation: fadeIn 1.2s ease;
        }
        
        h3 {
            font-size: 1.4rem;
            margin: 15px 0;
            color: var(--accent-color);
        }
        
        .tagline {
            font-size: 1.2rem;
            color: var(--light-color);
            margin-bottom: 20px;
            animation: fadeIn 1.4s ease;
        }
        
        .contact-info {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            margin-bottom: 20px;
            animation: fadeIn 1.6s ease;
        }
        
        .contact-info a {
            color: var(--light-color);
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .contact-info a:hover {
            color: var(--accent-color);
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 20px;
            animation: fadeIn 1.8s ease;
        }
        
        .social-links a {
            color: var(--light-color);
            font-size: 1.5rem;
            transition: transform 0.3s, color 0.3s;
        }
        
        .social-links a:hover {
            color: var(--accent-color);
            transform: translateY(-3px);
        }
        
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }
        
        .card {
            background: linear-gradient(135deg, var(--primary-color), var(--dark-color));
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s;
            animation: fadeIn 2s ease;
            position: relative;
            overflow: hidden;
        }
        
        .card::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(to bottom right, rgba(255,255,255,0.1), rgba(255,255,255,0));
            transform: rotate(45deg);
            z-index: 0;
        }
        
        .card:hover {
            transform: translateY(-5px);
        }
        
        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 15px;
        }
        
        .skill {
            background-color: var(--secondary-color);
            color: var(--light-color);
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 0.9rem;
            display: flex;
            align-items: center;
            gap: 5px;
            transition: all 0.3s;
        }
        
        .skill:hover {
            transform: scale(1.05);
            box-shadow: 0 0 10px rgba(184, 49, 174, 0.7);
        }
        
        .progress-bar {
            width: 100%;
            background-color: #444;
            border-radius: 10px;
            margin-top: 10px;
            overflow: hidden;
        }
        
        .progress {
            height: 8px;
            border-radius: 10px;
            background-color: var(--accent-color);
        }
        
        footer {
            text-align: center;
            padding: 20px;
            margin-top: 40px;
            border-top: 1px solid var(--primary-color);
        }
        
        .portfolio-link {
            display: inline-block;
            margin-top: 20px;
            padding: 12px 24px;
            background: var(--secondary-color);
            color: white;
            text-decoration: none;
            border-radius: 30px;
            font-weight: bold;
            transition: all 0.3s;
            animation: pulse 2s infinite;
        }
        
        .portfolio-link:hover {
            background: var(--accent-color);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }
        
        .tech-icon {
            font-size: 1.5rem;
            margin-right: 5px;
            vertical-align: middle;
        }
        
        .gif-container {
            text-align: center;
            margin: 20px 0;
        }
        
        .gif-container img {
            max-width: 100%;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }
        
        .floating {
            animation: float 6s ease-in-out infinite;
        }
        
        .github-setup {
            background: rgba(0, 0, 0, 0.2);
            padding: 20px;
            border-radius: 10px;
            margin: 30px 0;
            border-left: 4px solid var(--success-color);
        }
        
        .github-setup h3 {
            color: var(--success-color);
            margin-top: 0;
        }
        
        .github-setup ol {
            padding-left: 30px;
            margin: 15px 0;
        }
        
        .github-setup li {
            margin-bottom: 10px;
            position: relative;
        }
        
        .github-setup code {
            background: rgba(0, 0, 0, 0.3);
            padding: 2px 6px;
            border-radius: 4px;
            font-family: monospace;
        }
        
        .markdown-output {
            background: rgba(0, 0, 0, 0.2);
            padding: 20px;
            border-radius: 10px;
            margin: 30px 0;
            font-family: monospace;
            white-space: pre-wrap;
            max-height: 500px;
            overflow-y: auto;
        }
        
        .copy-btn {
            background: var(--secondary-color);
            color: white;
            border: none;
            padding: 8px 16px;
            border-radius: 4px;
            cursor: pointer;
            margin-top: 10px;
            transition: all 0.3s;
        }
        
        .copy-btn:hover {
            background: var(--accent-color);
        }
        
        @media (max-width: 768px) {
            .grid {
                grid-template-columns: 1fr;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            h2 {
                font-size: 1.5rem;
            }
            
            .contact-info {
                flex-direction: column;
                align-items: center;
                gap: 10px;
            }
            
            .capsule-text {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <div class="capsule-container">
                <div class="capsule-text">GitHub Profile README Generator 🚀</div>
            </div>
            <img src="https://avatars.githubusercontent.com/u/example" alt="Nhaniso J. Undenge" class="profile-img">
            <h1>Nhaniso J. Undenge</h1>
            <p class="tagline">Mobile & Full Stack Developer | Blockchain & AI Enthusiast</p>
            <div class="contact-info">
                <a href="mailto:nhanitech@gmail.com"><i class="fas fa-envelope"></i> nhanitech@gmail.com</a>
                <a href="tel:+263714024267"><i class="fas fa-phone"></i> +263 714 024267</a>
                <a href="#"><i class="fas fa-map-marker-alt"></i> Harare, Zimbabwe</a>
            </div>
            <div class="social-links">
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-linkedin"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-stack-overflow"></i></a>
            </div>
        </header>

        <div class="github-setup">
            <h3><i class="fab fa-github"></i> GitHub Profile README Instructions</h3>
            <p>Your GitHub profile README is displayed on your profile page. To set it up:</p>
            <ol>
                <li>Create a repository with the same name as your GitHub username</li>
                <li>Add a README.md file to this repository</li>
                <li>Use the markdown output below as a template</li>
                <li>Customize it with your own information</li>
            </ol>
        </div>

        <section>
            <h2>Your GitHub Profile README</h2>
            <div class="markdown-output" id="markdownOutput">
# Hey Everyone! 🕹️

I'm Nhaniso J. Undenge, a Mobile & Full Stack Developer with a passion for Blockchain and AI.

## 🚀 Skills & Expertise

### Mobile Development
- Flutter, iOS (Swift), Android, Dart, CoreML

### Web Development
- JavaScript, React, Angular, Node.js, SpringBoot, Nest.JS, Next.JS

### Blockchain
- Solidity, Web3.js, Truffle, Ethereum

### Data & AI
- TensorFlow, OpenCV, Keras, BigQuery, PostgreSQL

## 📈 GitHub Stats

![Your GitHub stats](https://github-readme-stats.vercel.app/api?username=zimnhashman&show_icons=true&theme=radical)

## 🔥 Recent Projects

- **Perigee Application**: Flutter application with comprehensive testing
- **Ditto Application**: JavaScript-based data extraction tool
- **Kassi Tool**: Data analysis tool with Java SpringBoot and Angular
- **Hitcore Music App**: iOS application for music management

## 📫 How to reach me

- Email: nhanitech@gmail.com
- Phone: +263 714 024267
- Location: Harare, Zimbabwe

## 😄 Fun fact

I love solving complex problems and exploring new technologies!
            </div>
            <button class="copy-btn" onclick="copyMarkdown()">Copy Markdown</button>
        </section>

        <section>
            <h2>Preview</h2>
            <div class="card">
                <p>This is a preview of how your GitHub profile README will look. The actual markdown code is above.</p>
                
                <div class="gif-container">
                    <img src="https://media.giphy.com/media/du3J3cXyzhj75IOgvA/giphy.gif" alt="GitHub Octocat" width="400">
                </div>
            </div>
        </section>

        <section>
            <h2>GitHub Badges to Consider</h2>
            <div class="grid">
                <div class="card">
                    <h3><i class="fas fa-chart-line"></i> Stats Badges</h3>
                    <p>Add GitHub stats badges to showcase your activity:</p>
                    <code>![Stats](https://github-readme-stats.vercel.app/api?username=YOUR_USERNAME&show_icons=true&theme=radical)</code>
                </div>
                
                <div class="card">
                    <h3><i class="fas fa-code"></i> Language Badges</h3>
                    <p>Show your most used languages:</p>
                    <code>![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_USERNAME&layout=compact)</code>
                </div>
                
                <div class="card">
                    <h3><i class="fas fa-trophy"></i> Achievement Badges</h3>
                    <p>Display your GitHub achievements:</p>
                    <code>![Achievements](https://github-profile-trophy.vercel.app/?username=YOUR_USERNAME&theme=radical)</code>
                </div>
            </div>
        </section>

        <footer>
            <p>© 2023 Nhaniso J. Undenge. All rights reserved.</p>
            <p>References available upon request.</p>
        </footer>
    </div>

    <script>
        function copyMarkdown() {
            const markdownText = document.getElementById('markdownOutput').textContent;
            navigator.clipboard.writeText(markdownText).then(() => {
                alert('Markdown copied to clipboard!');
            });
        }
        
        // Simple animation for progress bars
        document.addEventListener('DOMContentLoaded', function() {
            const progressBars = document.querySelectorAll('.progress');
            progressBars.forEach(bar => {
                const width = bar.style.width;
                bar.style.width = '0';
                setTimeout(() => {
                    bar.style.transition = 'width 1.5s ease-in-out';
                    bar.style.width = width;
                }, 500);
            });
            
            // Add animation to elements when they come into view
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.animation = 'fadeIn 1s forwards';
                        observer.unobserve(entry.target);
                    }
                });
            }, { threshold: 0.1 });
            
            document.querySelectorAll('section').forEach(section => {
                observer.observe(section);
            });
        });
    </script>
</body>
</html>
