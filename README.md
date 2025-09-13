<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Seher Siddiqui - ML Engineer & Developer</title>
    <script src="https://cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@300;400;600;700&family=Orbitron:wght@400;700&display=swap');
        
        :root {
            --primary: #00D9FF;
            --secondary: #FF2A6D;
            --dark: #0D1117;
            --darker: #080B10;
            --light: #FFFFFF;
            --gray: #8B949E;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            background-color: var(--dark);
            color: var(--light);
            font-family: 'JetBrains Mono', monospace;
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        #particles-js {
            position: fixed;
            width: 100%;
            height: 100%;
            z-index: -1;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }
        
        header {
            text-align: center;
            padding: 4rem 0;
            position: relative;
        }
        
        .profile-img {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            border: 4px solid var(--primary);
            box-shadow: 0 0 30px var(--primary);
            margin: 0 auto 1.5rem;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            padding: 5px;
            transition: all 0.3s ease;
        }
        
        .profile-img:hover {
            transform: scale(1.05);
            box-shadow: 0 0 40px var(--secondary);
        }
        
        h1 {
            font-family: 'Orbitron', sans-serif;
            font-size: 3.5rem;
            margin-bottom: 1rem;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 10px rgba(0, 217, 255, 0.3);
        }
        
        .typing-container {
            min-height: 60px;
            margin-bottom: 2rem;
        }
        
        .typing-text {
            font-size: 1.8rem;
            font-weight: 600;
            color: var(--primary);
        }
        
        .section {
            background: rgba(13, 17, 23, 0.8);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 2.5rem;
            margin-bottom: 3rem;
            border: 1px solid rgba(0, 217, 255, 0.2);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            transition: transform 0.3s ease;
        }
        
        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(0, 217, 255, 0.1);
        }
        
        h2 {
            font-family: 'Orbitron', sans-serif;
            color: var(--primary);
            margin-bottom: 1.5rem;
            font-size: 2rem;
            display: flex;
            align-items: center;
        }
        
        h2::after {
            content: '';
            flex: 1;
            height: 2px;
            margin-left: 1rem;
            background: linear-gradient(90deg, var(--primary), transparent);
        }
        
        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            justify-content: center;
        }
        
        .tech-item {
            background: rgba(0, 217, 255, 0.1);
            padding: 0.8rem 1.5rem;
            border-radius: 30px;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            transition: all 0.3s ease;
            border: 1px solid rgba(0, 217, 255, 0.3);
        }
        
        .tech-item:hover {
            background: rgba(0, 217, 255, 0.2);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 217, 255, 0.2);
        }
        
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }
        
        .stat-card {
            background: linear-gradient(145deg, rgba(13, 17, 23, 0.8), rgba(8, 11, 16, 0.8));
            border-radius: 10px;
            padding: 1.5rem;
            text-align: center;
            border: 1px solid rgba(0, 217, 255, 0.2);
            transition: all 0.3s ease;
        }
        
        .stat-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 217, 255, 0.2);
        }
        
        .stat-value {
            font-size: 2.5rem;
            font-weight: 700;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 0.5rem;
        }
        
        .stat-label {
            color: var(--gray);
            font-size: 0.9rem;
        }
        
        .hackathon-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 1.5rem;
        }
        
        .hackathon-table th, .hackathon-table td {
            padding: 1rem;
            text-align: left;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .hackathon-table th {
            color: var(--primary);
            font-weight: 600;
        }
        
        .hackathon-table tr:hover {
            background: rgba(0, 217, 255, 0.05);
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-top: 2rem;
        }
        
        .social-link {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            background: rgba(0, 217, 255, 0.1);
            color: var(--primary);
            font-size: 1.5rem;
            transition: all 0.3s ease;
            border: 1px solid rgba(0, 217, 255, 0.3);
            text-decoration: none;
            position: relative;
            overflow: hidden;
        }
        
        .social-link::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(0, 217, 255, 0.2), transparent);
            transition: all 0.5s ease;
        }
        
        .social-link:hover::before {
            left: 100%;
        }
        
        .social-link:hover {
            transform: translateY(-5px) rotate(5deg);
            box-shadow: 0 10px 20px rgba(0, 217, 255, 0.3);
            color: var(--secondary);
        }
        
        .badge-container {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            justify-content: center;
            margin-top: 1.5rem;
        }
        
        .badge {
            background: linear-gradient(145deg, rgba(13, 17, 23, 0.8), rgba(8, 11, 16, 0.8));
            padding: 0.8rem 1.5rem;
            border-radius: 30px;
            display: flex;
            align-items: center;
            gap: 0.5rem;
            border: 1px solid rgba(0, 217, 255, 0.3);
            transition: all 0.3s ease;
        }
        
        .badge:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 217, 255, 0.2);
        }
        
        .counter {
            font-size: 1.2rem;
            font-weight: 700;
            color: var(--primary);
        }
        
        .pulse {
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% {
                box-shadow: 0 0 0 0 rgba(0, 217, 255, 0.4);
            }
            70% {
                box-shadow: 0 0 0 15px rgba(0, 217, 255, 0);
            }
            100% {
                box-shadow: 0 0 0 0 rgba(0, 217, 255, 0);
            }
        }
        
        .glow {
            text-shadow: 0 0 10px var(--primary), 0 0 20px var(--primary), 0 0 30px var(--primary);
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
            }
            
            .section {
                padding: 1.5rem;
            }
            
            .stats-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div id="particles-js"></div>
    
    <div class="container">
        <header>
            <img src="https://avatars.githubusercontent.com/u/123456789?v=4" alt="Seher Siddiqui" class="profile-img pulse">
            <h1>Seher Siddiqui</h1>
            
            <div class="typing-container">
                <span class="typing-text" id="typing-text"></span>
            </div>
            
            <div class="social-links">
                <a href="https://linkedin.com/in/seher-siddiqui-76041b234" class="social-link">
                    <i class="fab fa-linkedin-in"></i>
                </a>
                <a href="https://sehersiddiqui.vercel.app/" class="social-link">
                    <i class="fas fa-globe"></i>
                </a>
                <a href="mailto:sehersiddiqui2812@gmail.com" class="social-link">
                    <i class="fas fa-envelope"></i>
                </a>
                <a href="https://leetcode.com/sehersiddiqui28" class="social-link">
                    <i class="fas fa-code"></i>
                </a>
                <a href="https://github.com/esss-28" class="social-link">
                    <i class="fab fa-github"></i>
                </a>
            </div>
        </header>
        
        <section class="section">
            <h2>🚀 About Me</h2>
            <p>I'm a passionate Machine Learning Engineer and Competitive Programmer with a knack for solving complex problems. I love pushing the boundaries of technology and contributing to innovative projects that make a difference.</p>
            
            <div class="stats-grid">
                <div class="stat-card">
                    <div class="stat-value" id="project-count">15+</div>
                    <div class="stat-label">Projects Completed</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value" id="leetcode-solved">250+</div>
                    <div class="stat-label">LeetCode Problems Solved</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value" id="hackathon-count">5+</div>
                    <div class="stat-label">Hackathons Participated</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value" id="contributions">500+</div>
                    <div class="stat-label">GitHub Contributions</div>
                </div>
            </div>
        </section>
        
        <section class="section">
            <h2>🛠️ Tech Stack</h2>
            <div class="tech-stack">
                <div class="tech-item">
                    <i class="fab fa-python"></i> Python
                </div>
                <div class="tech-item">
                    <i class="fab fa-js-square"></i> JavaScript
                </div>
                <div class="tech-item">
                    <i class="fab fa-react"></i> React
                </div>
                <div class="tech-item">
                    <i class="fab fa-node-js"></i> Node.js
                </div>
                <div class="tech-item">
                    <i class="fab fa-css3-alt"></i> CSS3
                </div>
                <div class="tech-item">
                    <i class="fab fa-git-alt"></i> Git
                </div>
                <div class="tech-item">
                    <i class="fas fa-database"></i> SQL
                </div>
                <div class="tech-item">
                    <i class="fas fa-brain"></i> TensorFlow
                </div>
            </div>
        </section>
        
        <section class="section">
            <h2>📊 GitHub Statistics</h2>
            <div class="stats-grid">
                <div class="stat-card">
                    <div class="stat-value" id="github-stars">120+</div>
                    <div class="stat-label">GitHub Stars</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value" id="github-forks">80+</div>
                    <div class="stat-label">Repository Forks</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value" id="github-commits">750+</div>
                    <div class="stat-label">Total Commits</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value" id="github-repos">30+</div>
                    <div class="stat-label">Public Repositories</div>
                </div>
            </div>
        </section>
        
        <section class="section">
            <h2>🏆 LeetCode Achievements</h2>
            <div class="stats-grid">
                <div class="stat-card">
                    <div class="stat-value" id="leet-easy">150+</div>
                    <div class="stat-label">Easy Problems</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value" id="leet-medium">80+</div>
                    <div class="stat-label">Medium Problems</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value" id="leet-hard">20+</div>
                    <div class="stat-label">Hard Problems</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value" id="leet-rank">Top 10%</div>
                    <div class="stat-label">Contest Rating</div>
                </div>
            </div>
            
            <div class="badge-container">
                <div class="badge">
                    <i class="fas fa-medal" style="color: gold;"></i>
                    <span>50 Days Badge</span>
                </div>
                <div class="badge">
                    <i class="fas fa-medal" style="color: silver;"></i>
                    <span>100 Days Badge</span>
                </div>
                <div class="badge">
                    <i class="fas fa-fire" style="color: orange;"></i>
                    <span>Streak Icon</span>
                </div>
            </div>
        </section>
        
        <section class="section">
            <h2>🚀 Hackathon Achievements</h2>
            <table class="hackathon-table">
                <thead>
                    <tr>
                        <th>Hackathon</th>
                        <th>Track</th>
                        <th>Achievement</th>
                        <th>Prize</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>Your First Hackathon</td>
                        <td>Web3/AI</td>
                        <td>Winner/Top 10</td>
                        <td>$XXX USD</td>
                    </tr>
                    <tr>
                        <td>Another Hackathon</td>
                        <td>Education/Web3</td>
                        <td>Community Selected</td>
                        <td>$XXX USD</td>
                    </tr>
                    <tr>
                        <td>Future Hackathon</td>
                        <td>Open Source</td>
                        <td>Best Project</td>
                        <td>TBD</td>
                    </tr>
                </tbody>
            </table>
        </section>
        </html>
