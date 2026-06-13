<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tashobya Isaac | Network Engineer Portfolio</title>
    <style>
        /* CSS VARIABLE PALETTE (Premium Executive / Navy & Gold) */
        :root {
            --background: #F4F6F9;       /* Soft White/Light Grey - Clean background */
            --surface: #FFFFFF;          /* Pure White - Content modules */
            --primary: #0A192F;          /* Deep Navy - Headings, major structure */
            --secondary: #D4AF37;        /* Rich Gold - Professional accents, highlights */
            --accent-teal: #008080;      /* Muted Teal - Interactive states, tags */
            --text-main: #2C3E50;        /* Dark Slate - Crisp, highly readable body text */
            --text-muted: #5A6B7C;       /* Soft Slate - Subtitles, secondary info */
            --border-color: #E2E8F0;     /* Clean subtle dividers */
        }

        /* GLOBAL STYLES */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
        }

        body {
            background-color: var(--background);
            color: var(--text-main);
            line-height: 1.7;
            padding: 0;
        }

        .container {
            max-width: 1140px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        /* PREMIUM HERO HEADER WITH PROFILE IMAGE INTEGRATION */
        header {
            background-color: var(--primary);
            color: #FFFFFF;
            padding: 50px 40px;
            border-radius: 12px;
            position: relative;
            box-shadow: 0 10px 30px rgba(10, 25, 47, 0.1);
            margin-bottom: 40px;
            border-bottom: 4px solid var(--secondary);
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 30px;
        }

        @media (max-width: 768px) {
            header {
                flex-direction: column-reverse;
                text-align: center;
                padding: 40px 20px;
            }
        }

        .header-content {
            flex: 1;
        }

        .header-content h1 {
            font-size: 3rem;
            font-weight: 700;
            letter-spacing: -0.5px;
            margin-bottom: 8px;
            color: #FFFFFF;
        }

        .header-content .subtitle {
            font-size: 1.3rem;
            color: var(--secondary);
            font-weight: 500;
            margin-bottom: 12px;
        }

        .header-content .institution {
            font-size: 1.05rem;
            color: rgba(255, 255, 255, 0.7);
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* PROFILE IMAGE CONTAINER */
        .profile-image-container {
            flex-shrink: 0;
        }

        .profile-frame {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            overflow: hidden;
            border: 4px solid var(--secondary);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
            background-color: #112240;
        }

        .profile-frame img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: center 20%;
        }

        /* LIVE STATUS INDICATOR */
        .status-pill {
            display: inline-flex;
            align-items: center;
            background: rgba(255, 255, 255, 0.08);
            border: 1px solid rgba(255, 255, 255, 0.15);
            padding: 6px 14px;
            border-radius: 30px;
            font-size: 0.85rem;
            font-weight: 500;
            color: #FFFFFF;
            margin-top: 20px;
        }

        .status-dot {
            width: 8px;
            height: 8px;
            background-color: #2ECC71;
            border-radius: 50%;
            margin-right: 8px;
            box-shadow: 0 0 8px #2ECC71;
        }

        /* MODULAR LAYOUT GRID */
        .layout-grid {
            display: grid;
            grid-template-columns: 7fr 4fr;
            gap: 30px;
        }

        @media (max-width: 900px) {
            .layout-grid {
                grid-template-columns: 1fr;
            }
        }

        /* EXECUTIVE CARD STYLES */
        .profile-card {
            background: var(--surface);
            border-radius: 8px;
            padding: 35px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.02), 0 1px 3px rgba(0, 0, 0, 0.05);
            border: 1px solid var(--border-color);
            margin-bottom: 30px;
        }

        h2 {
            color: var(--primary);
            font-size: 1.5rem;
            font-weight: 600;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--background);
            position: relative;
        }

        h2::after {
            content: '';
            position: absolute;
            bottom: -2px;
            left: 0;
            width: 50px;
            height: 2px;
            background-color: var(--secondary);
        }

        h3 {
            color: var(--primary);
            font-size: 1.15rem;
            font-weight: 600;
            margin: 20px 0 10px 0;
        }

        p {
            margin-bottom: 20px;
            font-size: 1.05rem;
            color: var(--text-main);
            text-align: justify;
        }

        ul.content-list {
            margin-left: 20px;
            margin-bottom: 20px;
            color: var(--text-main);
        }

        ul.content-list li {
            margin-bottom: 8px;
            font-size: 1.05rem;
        }

        /* PROFESSIONAL COMPETENCY TAGS */
        .tags-wrapper {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 10px;
        }

        .badge {
            background: var(--background);
            color: var(--primary);
            border: 1px solid var(--border-color);
            padding: 6px 14px;
            border-radius: 6px;
            font-size: 0.9rem;
            font-weight: 500;
            transition: all 0.2s ease;
        }

        .badge:hover {
            border-color: var(--accent-teal);
            color: var(--accent-teal);
            transform: translateY(-1px);
        }

        .badge-alt {
            background: #FFFDF3;
            color: #B7950B;
            border: 1px solid rgba(212, 175, 55, 0.3);
        }

        /* NETWORKING CHANNELS (CONTACTS) */
        .network-channels {
            list-style: none;
        }

        .channel-row {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 12px 0;
            border-bottom: 1px solid var(--background);
        }

        .channel-row:last-child {
            border-bottom: none;
        }

        .channel-title {
            font-weight: 600;
            font-size: 0.95rem;
            color: var(--text-muted);
        }

        .channel-action a {
            color: var(--accent-teal);
            text-decoration: none;
            font-weight: 500;
            font-size: 0.95rem;
        }

        .channel-action a:hover {
            color: var(--primary);
            text-decoration: underline;
        }

        /* SIMULATED METRIC INFRASTRUCTURE */
        .infra-widget {
            background: #F8FAFC;
            border: 1px dashed var(--border-color);
            border-radius: 6px;
            padding: 15px;
            margin-top: 15px;
        }

        .metric-line {
            display: flex;
            justify-content: space-between;
            font-size: 0.85rem;
            margin-bottom: 6px;
            font-family: monospace;
        }

        .metric-line:last-child {
            margin-bottom: 0;
        }

        /* PROFESSIONAL FOOTER */
        footer {
            margin-top: 60px;
            text-align: center;
            padding: 30px 20px;
            border-top: 1px solid var(--border-color);
            color: var(--text-muted);
            font-size: 0.9rem;
        }
    </style>
</head>
<body>

    <div class="container">
        
        <header>
            <div class="header-content">
                <h1>Tashobya Isaac</h1>
                <div class="subtitle">Aspiring Networking Specialist & System Architect</div>
                <div class="institution">Uganda Christian University</div>
                
                <div>
                    <span class="status-pill">
                        <span class="status-dot"></span>
                        Enterprise Core Engine: Operations Nominal
                    </span>
                </div>
            </div>

            <div class="profile-image-container">
                <div class="profile-frame">
                    <img src="WhatsApp Image 2026-06-13 at 17.07.36.jpeg" alt="Tashobya Isaac Profile Picture">
                </div>
            </div>
        </header>

        <div class="layout-grid">
            
            <main>
                <section class="profile-card">
                    <h2>About Me</h2>
                    <p>I am an aspiring Networking Specialist and currently a student at Uganda Christian University. My academic and professional focus is centered on building strong expertise in computer networking, with a long-term goal of becoming a highly skilled and industry-ready network engineer.</p>
                    
                    <p>My interest in technology extends beyond routing and switching configurations alone. I actively explore the intersection of modern systems design and data analysis to understand network traffic patterns, predict system anomalies, and optimize overall infrastructure layouts.</p>
                    
                    <h3>Multi-Disciplinary Technical Focus</h3>
                    <p>Through my academic tenure, I have developed functional skills across key emerging domains:</p>
                    <ul class="content-list">
                        <li><strong>Cybersecurity Hardening:</strong> Implementing strict access control lists (ACLs), secure device administration (SSH), and core perimeter defenses.</li>
                        <li><strong>Artificial Intelligence & Analysis:</strong> Investigating smart data modeling methods to automate routing optimizations and system behavior evaluations.</li>
                        <li><strong>Systems Visualization:</strong> Leveraging engineering design utilities like <strong>SolidWorks</strong> to conceptualize physical equipment placements, data center racks, and structural technical modeling layouts.</li>
                    </ul>
                    
                    <p>Beyond my technical background, I am also actively involved in sports. This structured physical involvement has helped me build strong personal discipline, sharp situational focus, and continuous resilience—qualities that translate directly into troubleshooting complex network topologies and maintaining academic growth under challenging timelines.</p>
                </section>

                <section class="profile-card">
                    <h2>Future Direction & Innovation Goals</h2>
                    <p>Looking ahead, I am actively working on developing additional hands-on projects in the fields of automated networking, cybersecurity frameworks, and intelligent infrastructure systems. My goal is to contribute to innovative solutions that improve digital access, stable connectivity, and high-quality skill development opportunities for students and young professionals within East Africa and beyond.</p>
                    
                    <h3>Strategic Architecture Focus Areas</h3>
                    <p>I am particularly focused on building systems that combine traditional networking components with software-driven enhancements to address critical infrastructure dependencies:</p>
                    <ul class="content-list">
                        <li><strong>Network Automation:</strong> Transitioning away from manually intensive configurations by studying programmable network principles and API integration.</li>
                        <li><strong>Intelligent Routing:</strong> Using intelligent frameworks to dynamically reroute and optimize data packet pathways under high-congestion scenarios.</li>
                        <li><strong>Youth Empowerment Portals:</strong> Building platforms backed by scalable local area architectures that lower the barrier to entry for digital transformation training.</li>
                    </ul>

                    <p>My journey in technology is driven by persistent curiosity, continuous self-guided learning, and a strong desire to build impactful solutions. I am fully committed to growing into an industry-expert networking professional while contributing meaningfully to projects that support digital transformation, local network modernization, and youth empowerment initiatives.</p>
                </section>
            </main>

            <aside>
                <div class="profile-card">
                    <h2>Technical Matrix</h2>
                    <div class="tags-wrapper">
                        <span class="badge">Networking</span>
                        <span class="badge">Cybersecurity</span>
                        <span class="badge">Artificial Intelligence</span>
                        <span class="badge">Data Analysis</span>
                        <span class="badge">Systems Design</span>
                        <span class="badge">SolidWorks</span>
                        <span class="badge">VLAN & Routing</span>
                        <span class="badge badge-alt">Athletic Discipline</span>
                    </div>
                </div>

                <div class="profile-card">
                    <h2>System Telemetry</h2>
                    <div class="infra-widget">
                        <div class="metric-line">
                            <span style="color: var(--text-muted);">Session Routing:</span>
                            <span style="color: var(--accent-teal); font-weight: bold;">OSPF_Active</span>
                        </div>
                        <div class="metric-line">
                            <span style="color: var(--text-muted);">Automation Layer:</span>
                            <span style="color: var(--accent-teal); font-weight: bold;">Enabled</span>
                        </div>
                        <div class="metric-line">
                            <span style="color: var(--text-muted);">Security Policy:</span>
                            <span style="color: #2ECC71; font-weight: bold;">Hardened</span>
                        </div>
                        <div class="metric-line">
                            <span style="color: var(--text-muted);">Node Status:</span>
                            <span style="color: var(--primary); font-weight: bold;">UCU-STU_NODE</span>
                        </div>
                    </div>
                </div>

                <div class="profile-card">
                    <h2>Professional Gateways</h2>
                    <ul class="network-channels">
                        <li class="channel-row">
                            <span class="channel-title">Corporate Email</span>
                            <span class="channel-action">
                                <a href="mailto:isaactash2@gmail.com">isaactash2@gmail.com</a>
                            </span>
                        </li>
                        <li class="channel-row">
                            <span class="channel-title">LinkedIn Node</span>
                            <span class="channel-action">
                                <a href="https://ug.linkedin.com/in/tashobya-isaac-097579358" target="_blank">tashobya-isaac</a>
                            </span>
                        </li>
                    </ul>
                </div>
            </aside>

        </div>

        <footer>
            <p>&copy; 2026 Tashobya Isaac &bull; Uganda Christian University Portfolio Matrix</p>
            <p style="font-size: 0.8rem; margin-top: 5px; opacity: 0.7;">Engineered for scalability, innovation, and digital transformation.</p>
        </footer>

    </div>

</body>
</html>
