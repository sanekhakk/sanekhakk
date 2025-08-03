<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sanekha K K - GitHub Profile</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@300;400;500;600;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Fira Code', monospace;
            background: linear-gradient(-45deg, #ee7752, #e73c7e, #23a6d5, #23d5ab);
            background-size: 400% 400%;
            animation: gradientBG 15s ease infinite;
            min-height: 100vh;
            overflow-x: hidden;
            position: relative;
        }
        
        @keyframes gradientBG {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        /* Floating particles */
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }
        
        .particle {
            position: absolute;
            width: 4px;
            height: 4px;
            background: rgba(255, 255, 255, 0.8);
            border-radius: 50%;
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); opacity: 1; }
            50% { transform: translateY(-20px) rotate(180deg); opacity: 0.8; }
        }
        
        /* Glass morphism container */
        .container {
            position: relative;
            z-index: 10;
            max-width: 1000px;
            margin: 0 auto;
            padding: 20px;
            backdrop-filter: blur(20px);
            background: rgba(255, 255, 255, 0.1);
            border-radius: 25px;
            border: 1px solid rgba(255, 255, 255, 0.2);
            box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
            margin-top: 40px;
            margin-bottom: 40px;
        }
        
        /* Header section */
        .header {
            text-align: center;
            margin-bottom: 40px;
        }
        
        .wave {
            display: inline-block;
            animation: wave 2s ease-in-out infinite;
        }
        
        @keyframes wave {
            0%, 100% { transform: rotate(0deg); }
            25% { transform: rotate(20deg); }
            75% { transform: rotate(-10deg); }
        }
        
        .name {
            font-size: 3rem;
            font-weight: 700;
            background: linear-gradient(45deg, #ff6b9d, #c471ed, #12c2e9);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin: 20px 0;
            text-shadow: 0 0 30px rgba(255, 107, 157, 0.5);
        }
        
        .typing-container {
            margin: 30px 0;
        }
        
        .typing-text {
            font-size: 1.5rem;
            color: white;
            text-shadow: 0 0 20px rgba(255, 255, 255, 0.5);
        }
        
        /* Profile image with floating animation */
        .profile-section {
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin: 40px 0;
            flex-wrap: wrap;
        }
        
        .profile-info {
            flex: 1;
            min-width: 300px;
            color: white;
            font-size: 1.1rem;
            line-height: 1.8;
        }
        
        .profile-info h3 {
            color: #ff6b9d;
            margin-bottom: 20px;
            font-size: 1.8rem;
        }
        
        .coding-gif {
            flex: 1;
            text-align: center;
            animation: floatGif 6s ease-in-out infinite;
        }
        
        .coding-gif img {
            max-width: 350px;
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
        }
        
        @keyframes floatGif {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }
        
        /* Tech stack with hover effects */
        .tech-stack {
            margin: 50px 0;
            text-align: center;
        }
        
        .tech-stack h2 {
            color: white;
            font-size: 2.2rem;
            margin-bottom: 30px;
            text-shadow: 0 0 20px rgba(255, 255, 255, 0.5);
        }
        
        .tech-badges {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
        }
        
        .tech-badge {
            padding: 12px 20px;
            border-radius: 25px;
            background: linear-gradient(45deg, rgba(255, 255, 255, 0.2), rgba(255, 255, 255, 0.1));
            border: 1px solid rgba(255, 255, 255, 0.3);
            color: white;
            font-weight: 600;
            transition: all 0.3s ease;
            cursor: pointer;
            backdrop-filter: blur(10px);
        }
        
        .tech-badge:hover {
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 15px 30px rgba(255, 107, 157, 0.4);
            background: linear-gradient(45deg, #ff6b9d, #c471ed);
        }
        
        /* Stats section with animated cards */
        .stats-section {
            margin: 50px 0;
            text-align: center;
        }
        
        .stats-section h2 {
            color: white;
            font-size: 2.2rem;
            margin-bottom: 30px;
            text-shadow: 0 0 20px rgba(255, 255, 255, 0.5);
        }
        
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }
        
        .stat-card {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 20px;
            border: 1px solid rgba(255, 255, 255, 0.2);
            transition: all 0.3s ease;
            animation: cardFloat 8s ease-in-out infinite;
        }
        
        .stat-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(255, 107, 157, 0.3);
        }
        
        .stat-card:nth-child(2) {
            animation-delay: -2s;
        }
        
        .stat-card:nth-child(3) {
            animation-delay: -4s;
        }
        
        @keyframes cardFloat {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }
        
        /* Connect section */
        .connect-section {
            text-align: center;
            margin: 50px 0;
        }
        
        .connect-section h2 {
            color: white;
            font-size: 2.2rem;
            margin-bottom: 30px;
            text-shadow: 0 0 20px rgba(255, 255, 255, 0.5);
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }
        
        .social-link {
            display: inline-block;
            padding: 15px 30px;
            background: linear-gradient(45deg, rgba(255, 255, 255, 0.2), rgba(255, 255, 255, 0.1));
            border: 1px solid rgba(255, 255, 255, 0.3);
            border-radius: 50px;
            color: white;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
        }
        
        .social-link:hover {
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 15px 30px rgba(18, 194, 233, 0.4);
            background: linear-gradient(45deg, #12c2e9, #c471ed);
        }
        
        /* Footer */
        .footer {
            text-align: center;
            margin-top: 40px;
            padding: 20px;
            color: white;
            font-size: 1.2rem;
            text-shadow: 0 0 20px rgba(255, 255, 255, 0.5);
        }
        
        /* Responsive design */
        @media (max-width: 768px) {
            .name { font-size: 2rem; }
            .profile-section { flex-direction: column; text-align: center; }
            .coding-gif { margin-top: 30px; }
            .container { margin: 20px; padding: 15px; }
        }
        
        /* Loading animation */
        .loading {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(-45deg, #ee7752, #e73c7e, #23a6d5, #23d5ab);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 9999;
            animation: gradientBG 15s ease infinite;
        }
        
        .loading-text {
            color: white;
            font-size: 2rem;
            font-weight: 600;
            animation: pulse 2s ease-in-out infinite;
        }
        
        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.5; }
        }
    </style>
</head>
<body>
    <!-- Loading Screen -->
    <div class="loading" id="loading">
        <div class="loading-text">Loading Amazing Content...</div>
    </div>
    
    <!-- Floating Particles -->
    <div class="particles" id="particles"></div>
    
    <!-- Main Container -->
    <div class="container">
        <!-- Header -->
        <div class="header">
            <div class="wave">👋</div>
            <h1 class="name">Hi, I'm Sanekha K K</h1>
            <div class="typing-container">
                <div class="typing-text" id="typingText"></div>
            </div>
        </div>
        
        <!-- Profile Section -->
        <div class="profile-section">
            <div class="profile-info">
                <h3>🚀 Quick Intro</h3>
                <p><strong>Frontend Developer</strong> passionate about creating beautiful, responsive web interfaces</p>
                <p>🎓 <strong>B.Tech CS Student</strong> at Lovely Professional University</p>
                <p>💼 <strong>Frontend Intern</strong> at Pinnet Infosolutions</p>
                <p>📍 <strong>Kozhikode, Kerala, India</strong> 🇮🇳</p>
            </div>
            <div class="coding-gif">
                <img src="https://cdn.dribbble.com/users/1162077/screenshots/3848914/programmer.gif" alt="Coding Animation">
            </div>
        </div>
        
        <!-- Tech Stack -->
        <div class="tech-stack">
            <h2>🛠️ Tech Arsenal</h2>
            <div class="tech-badges">
                <div class="tech-badge">JavaScript</div>
                <div class="tech-badge">React.js</div>
                <div class="tech-badge">HTML5</div>
                <div class="tech-badge">CSS3</div>
                <div class="tech-badge">Python</div>
                <div class="tech-badge">C++</div>
            </div>
        </div>
        
        <!-- Stats Section -->
        <div class="stats-section">
            <h2>📊 GitHub Analytics</h2>
            <div class="stats-grid">
                <div class="stat-card">
                    <img src="https://github-readme-stats.vercel.app/api?username=YOUR_USERNAME&show_icons=true&theme=synthwave&hide_border=true" alt="GitHub Stats" style="width: 100%; border-radius: 10px;">
                </div>
                <div class="stat-card">
                    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_USERNAME&layout=compact&theme=synthwave&hide_border=true" alt="Top Languages" style="width: 100%; border-radius: 10px;">
                </div>
                <div class="stat-card">
                    <img src="https://github-readme-streak-stats.herokuapp.com/?user=YOUR_USERNAME&theme=synthwave&hide_border=true" alt="GitHub Streak" style="width: 100%; border-radius: 10px;">
                </div>
            </div>
        </div>
        
        <!-- Connect Section -->
        <div class="connect-section">
            <h2>🌐 Let's Connect!</h2>
            <div class="social-links">
                <a href="https://linkedin.com/in/sanekhakk" class="social-link">LinkedIn</a>
                <a href="mailto:sanekhakk@gmail.com" class="social-link">Email</a>
                <a href="https://github.com/YOUR_USERNAME" class="social-link">GitHub</a>
            </div>
        </div>
        
        <!-- Footer -->
        <div class="footer">
            ✨ Building beautiful interfaces, one component at a time! ✨
        </div>
    </div>
    
    <script>
        // Typing animation
        const phrases = [
            "Frontend Developer",
            "UI/UX Enthusiast", 
            "React.js Developer",
            "CS Student",
            "Tech Explorer"
        ];
        
        let currentPhrase = 0;
        let currentChar = 0;
        let isDeleting = false;
        
        function typeWriter() {
            const typingElement = document.getElementById('typingText');
            const currentText = phrases[currentPhrase];
            
            if (isDeleting) {
                typingElement.textContent = currentText.substring(0, currentChar - 1);
                currentChar--;
            } else {
                typingElement.textContent = currentText.substring(0, currentChar + 1);
                currentChar++;
            }
            
            let typeSpeed = 100;
            
            if (isDeleting) {
                typeSpeed /= 2;
            }
            
            if (!isDeleting && currentChar === currentText.length) {
                typeSpeed = 2000;
                isDeleting = true;
            } else if (isDeleting && currentChar === 0) {
                isDeleting = false;
                currentPhrase = (currentPhrase + 1) % phrases.length;
                typeSpeed = 500;
            }
            
            setTimeout(typeWriter, typeSpeed);
        }
        
        // Create floating particles
        function createParticles() {
            const particlesContainer = document.getElementById('particles');
            const particleCount = 50;
            
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                particle.style.left = Math.random() * 100 + '%';
                particle.style.top = Math.random() * 100 + '%';
                particle.style.animationDelay = Math.random() * 6 + 's';
                particle.style.animationDuration = (Math.random() * 3 + 3) + 's';
                particlesContainer.appendChild(particle);
            }
        }
        
        // Loading screen
        window.addEventListener('load', function() {
            setTimeout(() => {
                document.getElementById('loading').style.opacity = '0';
                setTimeout(() => {
                    document.getElementById('loading').style.display = 'none';
                }, 500);
            }, 2000);
        });
        
        // Initialize animations
        document.addEventListener('DOMContentLoaded', function() {
            typeWriter();
            createParticles();
        });
        
        // Add scroll animations
        window.addEventListener('scroll', function() {
            const scrolled = window.pageYOffset;
            const particles = document.querySelectorAll('.particle');
            
            particles.forEach((particle, index) => {
                const speed = (index % 5 + 1) * 0.5;
                particle.style.transform = `translateY(${scrolled * speed}px)`;
            });
        });
    </script>
</body>
</html>
