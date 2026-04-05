---
layout: page
title: Resume
menu: true
order: 3
description: 
---

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> </title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #00838f;
            --text-dark: #2c3e50;
            --text-light: #546e7a;
            --bg-light: #f8f9fa;
            --border: #eceff1;
            --accent: #00838f;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Helvetica Neue', sans-serif;
            line-height: 1.6;
            color: var(--text-dark);
            background: white;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 450px 1fr;
            gap: 40px;
            padding: 50px 40px;
        }

        /* Header */
        .header {
            grid-column: 1 / -1;
            display: grid;
            grid-template-columns: 1fr auto;
            gap: 30px;
            align-items: start;
            padding-bottom: 30px;
            border-bottom: 2px solid var(--primary);
            margin-bottom: 20px;
        }

        .header-info h1 {
            font-size: 32px;
            font-weight: 700;
            color: var(--text-dark);
            margin-bottom: 6px;
            letter-spacing: -0.5px;
        }

        .header-info p {
            font-size: 14px;
            color: var(--text-light);
            font-weight: 500;
        }

        .contact-info {
            font-size: 13px;
            line-height: 1.8;
            color: var(--text-light);
            margin-top: 15px;
        }

        .contact-info a {
            color: var(--primary);
            text-decoration: none;
            font-weight: 500;
        }

        .contact-info a:hover {
            text-decoration: underline;
        }

        /* Sidebar */
        .sidebar {
            display: flex;
            flex-direction: column;
            gap: 32px;
        }

        .sidebar-section h3 {
            font-size: 13px;
            font-weight: 700;
            text-transform: uppercase;
            color: var(--primary);
            letter-spacing: 0.8px;
            margin-bottom: 14px;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--primary);
        }

        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

        .tech-tag {
            display: inline-block;
            background: var(--bg-light);
            color: var(--text-dark);
            padding: 6px 12px;
            border-radius: 4px;
            font-size: 12px;
            font-weight: 500;
            border: 1px solid var(--border);
        }

        .competencies ul {
            list-style: none;
            font-size: 13px;
            line-height: 2;
            color: var(--text-light);
        }

        .competencies li:before {
            content: "•";
            color: var(--primary);
            font-weight: bold;
            margin-right: 8px;
        }

        .languages {
            font-size: 13px;
            line-height: 2;
        }

        .language-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 4px;
        }

        .language-item strong {
            color: var(--text-dark);
        }

        .stars {
            display: flex;
            gap: 3px;
        }

        .star {
            width: 10px;
            height: 10px;
            border-radius: 50%;
            background: var(--primary);
        }

        /* Main content */
        .main-content {
            display: flex;
            flex-direction: column;
            gap: 32px;
        }

        .section {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .section-title {
            font-size: 16px;
            font-weight: 700;
            text-transform: uppercase;
            color: var(--primary);
            letter-spacing: 0.8px;
            padding-bottom: 12px;
            border-bottom: 2px solid var(--primary);
        }

        .job {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .job-header {
            display: flex;
            justify-content: space-between;
            align-items: baseline;
            gap: 15px;
        }

        .job-title {
            font-size: 14px;
            font-weight: 700;
            color: var(--text-dark);
        }

        .job-company {
            color: var(--primary);
            font-weight: 600;
            font-size: 14px;
        }

        .job-dates {
            font-size: 12px;
            color: var(--text-light);
            white-space: nowrap;
        }

        .job-location {
            font-size: 12px;
            color: var(--text-light);
        }

        .job-description {
            font-size: 13px;
            line-height: 1.7;
            color: var(--text-light);
        }

        .job-description ul {
            list-style: none;
            margin: 8px 0;
        }

        .job-description li {
            margin-bottom: 6px;
            padding-left: 16px;
            position: relative;
        }

        .job-description li:before {
            content: "•";
            position: absolute;
            left: 0;
            color: var(--primary);
            font-weight: bold;
        }

        .job-skills {
            font-size: 12px;
            color: var(--text-light);
            font-style: italic;
            margin-top: 6px;
            padding-top: 8px;
            border-top: 1px solid var(--border);
        }

        .job-skills strong {
            color: var(--text-dark);
        }

        .education-item {
            margin-bottom: 16px;
        }

        .education-degree {
            font-size: 13px;
            font-weight: 700;
            color: var(--text-dark);
            margin-bottom: 4px;
        }

        .education-school {
            font-size: 13px;
            color: var(--primary);
            font-weight: 600;
            margin-bottom: 4px;
        }

        .education-meta {
            font-size: 12px;
            color: var(--text-light);
        }

        /* Summary section */
        .summary-text {
            font-size: 13px;
            line-height: 1.8;
            color: var(--text-light);
            font-style: italic;
        }

        /* Responsive */
        @media (max-width: 900px) {
            .container {
                grid-template-columns: 1fr;
                gap: 30px;
                padding: 30px 25px;
            }

            .header {
                grid-column: 1;
            }

            .sidebar {
                order: 3;
                grid-column: 1;
            }

            .main-content {
                order: 2;
                grid-column: 1;
            }

            .profile-pic {
                width: 100px;
                height: 100px;
                font-size: 32px;
            }

            .header h1 {
                font-size: 28px;
            }

            .tech-tag {
                padding: 5px 10px;
                font-size: 11px;
            }
        }

        @media print {
            body {
                background: white;
            }

            .container {
                max-width: 100%;
                padding: 0;
                margin: 0;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <div class="header">
            <div class="header-info">
                <h1>DIOGO DUARTE</h1>
            </div>
            <div class="profile-pic"></div>
        </div>


        <!-- Main Content -->
        <main class="main-content">
            <section class="section">
                <h2 class="section-title">EXPERIENCE</h2>

                <div class="job">
                    <div class="job-header">
                        <div>
                            <div class="job-title">Lab Manager & Research Software Engineer</div>
                            <div class="job-company">NOVA SBE</div>
                        </div>
                        <div style="text-align: right;">
                            <div class="job-dates">2025–Current</div>
                            <div class="job-location">Cascais, Portugal</div>
                        </div>
                    </div>
                    <div class="job-description">
                        <ul>
                            <li>Managed IT and lab resources for experimentation and teaching</li>
                            <li>Developed and validated software for data collection and automation</li>
                            <li>Created end-user evaluation methods for clients in SaaS and AI solutions</li>
                        </ul>
                    </div>
                    <div class="job-skills"><strong>Skills:</strong> Data and software engineering, system administration</div>
                </div>

                <div class="job">
                    <div class="job-header">
                        <div>
                            <div class="job-title">Graduate Researcher</div>
                            <div class="job-company">Fundação Champalimaud</div>
                        </div>
                        <div style="text-align: right;">
                            <div class="job-dates">2018–2024</div>
                            <div class="job-location">Lisboa, Portugal</div>
                        </div>
                    </div>
                    <div class="job-description">
                        <ul>
                            <li>Designed and assembled neurobehavioral setups for mouse research</li>
                            <li>Engineered multi-stream data acquisition systems (NI DAQ + 430 fps video)</li>
                            <li>Computationally optimized estimation of firing rates from big data (30x faster)</li>
                            <li>Tracked animal movement (classical image processing + deep CNNs)</li>
                            <li>Predicted animal behavior from neural data (neural decoding by multilinear regression)</li>
                            <li>Deployed virtual containers for large scale neural simulations in remote servers</li>
                        </ul>
                    </div>
                    <div class="job-skills"><strong>Skills:</strong> DAQ electronics, multi-sensor integration, computer vision, GPU computing, artificial neural networks, Docker</div>
                </div>

                <div class="job">
                    <div class="job-header">
                        <div>
                            <div class="job-title">Software Engineer & Data Scientist</div>
                            <div class="job-company">Instituto de Biofísica e Engenharia Biomédica</div>
                        </div>
                        <div style="text-align: right;">
                            <div class="job-dates">2017</div>
                            <div class="job-location">Lisboa, Portugal</div>
                        </div>
                    </div>
                    <div class="job-description">
                        <ul>
                            <li>Created a medical imaging analysis pipeline for pre-surgical planning</li>
                            <li>Tuned blind source separation models for functional imaging in patients</li>
                            <li>Communicated closely with medicine and engineering teams</li>
                            <li>Automated the generation of functional imaging reports</li>
                        </ul>
                    </div>
                    <div class="job-skills"><strong>Skills:</strong> Matlab, Blind Source Separation, DICOM</div>
                </div>

                <div class="job">
                    <div class="job-header">
                        <div>
                            <div class="job-title">Game Software Developer</div>
                            <div class="job-company">Museu dos Valores Universais</div>
                        </div>
                        <div style="text-align: right;">
                            <div class="job-dates">2016</div>
                            <div class="job-location">Mafra, Portugal</div>
                        </div>
                    </div>
                    <div class="job-description">
                        <ul>
                            <li>Implemented a facial mimicry interactive game for children</li>
                        </ul>
                    </div>
                    <div class="job-skills"><strong>Skills:</strong> Unity, C#, Affectiva AI</div>
                </div>

                <div class="job">
                    <div class="job-header">
                        <div>
                            <div class="job-title">Researcher / MSc. Student</div>
                            <div class="job-company">Institute of Cognitive Neuroscience, UCL</div>
                        </div>
                        <div style="text-align: right;">
                            <div class="job-dates">2014–2015</div>
                            <div class="job-location">London, England</div>
                        </div>
                    </div>
                    <div class="job-description">
                        <ul>
                            <li>Developed hardware and software for human behavioral experiments</li>
                            <li>Quantified behavior through timeseries analysis</li>
                            <li>Estimated neural encoding schema via multivariate analysis</li>
                        </ul>
                    </div>
                    <div class="job-skills"><strong>Skills:</strong> Computer Aided Design, C++, Matlab</div>
                </div>
            </section>
        </main>
        
                <!-- Sidebar -->
        <aside class="aside">
            <div class="sidebar-section">
            </div>

            <div class="sidebar-section">
                <h3>TECH STACK</h3>
                <div class="tech-stack">
                    <span class="tech-tag">python</span>
                    <span class="tech-tag">C</span>
                    <span class="tech-tag">C++</span>
                    <span class="tech-tag">Matlab</span>
                    <span class="tech-tag">git</span>
                    <span class="tech-tag">ETL</span>
                    <span class="tech-tag">SQL</span>
                    <span class="tech-tag">scikit-learn</span>
                    <span class="tech-tag">Tensorflow</span>
                    <span class="tech-tag">Keras</span>
                    <span class="tech-tag">OpenCV</span>
                    <span class="tech-tag">Dash</span>
                    <span class="tech-tag">Plotly</span>
                    <span class="tech-tag">Power BI</span>
                    <span class="tech-tag">DAQ</span>
                    <span class="tech-tag">CAD</span>
                </div>
            </div>

            <div class="sidebar-section">
                <h3>CORE COMPETENCIES</h3>
                <div class="competencies">
                    <ul>
                        <li>ETL and Data Engineering</li>
                        <li>ML Modeling</li>
                        <li>Time series and image analysis</li>
                        <li>Computer Vision</li>
                    </ul>
                </div>
            </div>

            <div class="sidebar-section">
                <h3>LANGUAGES</h3>
                <div class="languages">
                    <div class="language-item">
                        <strong>Portuguese</strong>
                        <div class="stars">
                            <div class="star"></div>
                            <div class="star"></div>
                            <div class="star"></div>
                            <div class="star"></div>
                            <div class="star"></div>
                        </div>
                    </div>
                    <div class="language-item">
                        <strong>English</strong>
                        <div class="stars">
                            <div class="star"></div>
                            <div class="star"></div>
                            <div class="star"></div>
                            <div class="star"></div>
                            <div class="star"></div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="sidebar-section">
                <h3>EDUCATION</h3>
                <div class="education-item">
                    <div class="education-degree">PhD in Neuroscience</div>
                    <div class="education-school">International Neuroscience Doctoral Programme, ITQB-NOVA / Fundação Champalimaud</div>
                    <div class="education-meta">Mar 2018 – Dec 2024 • Lisboa, Portugal</div>
                </div>
                <div class="education-item">
                    <div class="education-degree">MSc in Biomedical Engineering</div>
                    <div class="education-school">Faculdade de Ciências, Universidade de Lisboa</div>
                    <div class="education-meta">Sep 2013 – May 2016 • Lisboa, Portugal</div>
                </div>
                <div class="education-item">
                    <div class="education-degree">BSc in Biomedical Engineering</div>
                    <div class="education-school">Faculdade de Ciências, Universidade de Lisboa</div>
                    <div class="education-meta">Sep 2010 – Jul 2013 • Lisboa, Portugal</div>
                </div>
            </div>
        </aside>
        
        
    </div>
</body>
