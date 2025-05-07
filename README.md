<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nick Neo - Finance Systems Expert</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        /* Reset and Base Styles */
        html {
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        *,
        *:before,
        *:after {
            box-sizing: inherit;
        }

        body {
            margin: 0;
            padding: 0;
            font-family: 'Montserrat', sans-serif;
            line-height: 1.6;
            background: #f9f9f9;
            color: #333;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
        }

        img {
            max-width: 100%;
            height: auto;
        }

        a {
            text-decoration: none;
        }

        /* Typography */
        h1,
        h2,
        h3 {
            color: #1a202c;
            /* Darker grey */
            font-weight: 700;
            line-height: 1.2;
            margin-bottom: 0.75em;
        }

        h1 {
            font-size: 2.5rem;
        }

        h2 {
            font-size: 2rem;
        }

        h3 {
            font-size: 1.5rem;
        }

        p {
            margin-bottom: 1.25em;
            color: #4a5568;
            /* Medium grey */
        }

        /* Colors */
        :root {
            --primary-color: #434190;
            /* Deep Indigo */
            --primary-light: #6d6cb3;
            /* Light Indigo */
            --accent-color: #f7fafc;
            /* Off-White */
            --text-light: #718096;
            /* Light Text */
        }

        /* Layout */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }

        .grid {
            display: grid;
            grid-gap: 2rem;
        }

        /* Header */
        header {
            background: white;
            box-shadow: 0 0.25rem 0.5rem rgba(0, 0, 0, 0.05);
            position: sticky;
            top: 0;
            z-index: 10;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary-color);
        }

        nav ul {
            display: flex;
            list-style: none;
            padding: 0;
        }

        nav li {
            margin-left: 1.5rem;
        }

        nav a {
            color: var(--text-light);
            transition: color 0.3s ease;
        }

        nav a:hover {
            color: var(--primary-color);
        }

        /* Hero Section */
        #hero {
            background: linear-gradient(to right, var(--primary-color), var(--primary-light));
            color: var(--accent-color);
            padding: 4rem 0;
            text-align: center;
        }

        #hero h1 {
            color: var(--accent-color);
            font-size: 3rem;
            margin-bottom: 0.5rem;
        }

        #hero p {
            color: var(--accent-color);
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }

        .profile-image {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            margin-bottom: 1rem;
            box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.2);
        }

        .btn {
            display: inline-block;
            padding: 0.75rem 1.5rem;
            border-radius: 0.25rem;
            background-color: var(--accent-color);
            color: var(--primary-color);
            font-weight: 600;
            transition: background-color 0.3s ease, color 0.3s ease;
        }

        .btn:hover {
            background-color: var(--primary-light);
            color: var(--accent-color);
        }

        /* About Section */
        #about {
            background: var(--accent-color);
            padding: 4rem 0;
        }

        #about h2 {
            text-align: center;
            margin-bottom: 2rem;
        }

        /* Experience Section */
        #experience {
            background: #f0f0f5;
            padding: 4rem 0;
        }

        #experience h2 {
            text-align: center;
            margin-bottom: 2rem;
        }

        .experience-item {
            background: white;
            padding: 2rem;
            border-radius: 0.5rem;
            box-shadow: 0 0.25rem 0.5rem rgba(0, 0, 0, 0.05);
            border-left: 0.5rem solid var(--primary-color);
        }

        .experience-item h3 {
            margin-top: 0;
            color: var(--primary-color);
        }

        .experience-item p.company {
            font-style: italic;
            color: var(--text-light);
            margin-bottom: 0.5rem;
        }

        .experience-item p.duration {
            color: #a0aec0;
            font-size: 0.9rem;
        }

        .experience-item ul {
            list-style: disc;
            margin-left: 1.5rem;
            margin-top: 1rem;
        }

        .experience-item ul li {
            margin-bottom: 0.5rem;
        }

        /* Skills Section */
        #skills {
            background: var(--accent-color);
            padding: 4rem 0;
        }

        #skills h2 {
            text-align: center;
            margin-bottom: 2rem;
        }

        .skills-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            grid-gap: 2rem;
        }

        .skill-category {
            background: white;
            padding: 1.5rem;
            border-radius: 0.5rem;
            box-shadow: 0 0.25rem 0.5rem rgba(0, 0, 0, 0.05);
        }

        .skill-category h3 {
            margin-top: 0;
            margin-bottom: 1rem;
            color: var(--primary-color);
            border-bottom: 2px solid #edf2f7;
            padding-bottom: 0.5rem;
        }

        .skill-category ul {
            list-style: none;
            padding: 0;
        }

        .skill-category li {
            margin-bottom: 0.5rem;
            color: var(--text-light);
        }

        /* Contact Section */
        #contact {
            background: linear-gradient(to right, var(--primary-light), var(--primary-color));
            color: var(--accent-color);
            padding: 4rem 0;
            text-align: center;
        }

        #contact h2 {
            margin-bottom: 1.5rem;
            color: var(--accent-color);
        }

        #contact p {
            font-size: 1.1rem;
            margin-bottom: 2rem;
        }

        .contact-details {
            margin-top: 1rem;
        }

        .contact-details p {
            margin-bottom: 0.75rem;
        }

        .contact-details a {
            color: var(--accent-color);
            font-weight: 500;
        }

        .contact-details i {
            margin-right: 0.5rem;
        }

        /* Footer */
        footer {
            background: #2d3748;
            /* Darker Grey */
            color: var(--text-light);
            text-align: center;
            padding: 1.5rem 0;
            font-size: 0.9rem;
        }

        /* Utility Classes */
        .text-center {
            text-align: center;
        }

        .mt-4 {
            margin-top: 1rem;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .container {
                padding: 1rem;
            }

            nav {
                flex-direction: column;
                align-items: flex-start;
            }

            nav ul {
                margin-top: 1rem;
            }

            nav li {
                margin-left: 0;
                margin-right: 1rem;
            }

            #hero {
                padding: 3rem 0;
            }

            #hero h1 {
                font-size: 2.2rem;
            }

            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>

<body>
    <header>
        <nav class="container">
            <a href="#" class="logo">Nick Neo</a>
            <ul>
                <li><a href="#about">About</a></li>
                <li><a href="#experience">Experience</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#contact">Contact</a></li>
                <li><a href="Nick Neo CV - Apr25.docx" download="Nick Neo CV">Download CV <i class="fas fa-download"></i></a></li>
            </ul>
        </nav>
    </header>

    <section id="hero">
        <div class="container text-center">
            <img src="profile.jpg" alt="Nick Neo" class="profile-image">
            <h1>Nick Neo</h1>
            <p class="lead">Finance Systems Expert | Dynamics 365, Oracle, Business Analysis</p>
            <p>Driving efficiency and delivering impactful solutions with 25+ years of experience.</p>
            <a href="#contact" class="btn">Get In Touch</a>
        </div>
    </section>

    <section id="about">
        <div class="container">
            <h2>About Me</h2>
            <p>With over 25 years of experience in finance and systems, I bring a wealth of expertise in finance systems projects, business analysis, and financial modeling. My ACCA qualification underpins a career dedicated to optimizing financial processes and implementing innovative solutions across both private and public sectors.</p>
            <p>I have a proven track record of successfully implementing Cloud/SaaS platforms such as Dynamics 365 F&O/Business Central/NAV, Oracle, and others, thriving in Agile environments. My focus is on understanding core business needs and leveraging technology to drive efficiency, improve controls, and provide valuable insights.</p>
            <p>References highlight my ability to quickly grasp complex situations, provide valuable support and analysis, and deliver effective solutions. My calm demeanor and commitment to excellence ensure a positive and productive engagement.</p>
        </div>
    </section>

    <section id="experience">
        <div class="container">
            <h2>Experience</h2>
            <div class="experience-item">
                <h3>Finance Systems Consultant</h3>
                <p class="company">Various Clients</p>
                <p class="duration">Last 5 Years (Examples)</p>
                <ul>
                    <li>Provided support and analysis for Dynamics Business Central implementations.</li>
                    <li>Identified inefficiencies and recommended system enhancements.</li>
                    <li>Collaborated with stakeholders to optimize system integration.</li>
                    <li>Delivered end-user training and support.</li>
                </ul>
            </div>
            <div class="experience-item">
                <h3>Interim Systems Accountant</h3>
                <p class="company">Electoral Commission</p>
                <p class="duration">2023 - 2024</p>
                <ul>
                    <li>Supported the rectification of a failed system implementation.</li>
                    <li>Developed Excel-based solutions for Non-Current Asset management.</li>
                    <li>Demonstrated calm and effective problem-solving.</li>
                </ul>
            </div>
            <div class="experience-item">
                <h3>Finance Lead/Project Manager</h3>
                <p class="company">Various Clients (Pre-2019)</p>
                <ul>
                    <li>Led Oracle Fusion finance system implementations.</li>
                    <li>Managed project timelines, budgets, and resources.</li>
                    <li>Ensured successful delivery of finance system solutions.</li>
                </ul>
            </div>
            <div class="experience-item">
                <h3>Finance and Business Systems Analyst</h3>
                <p class="company">Various Clients (Pre-2019)</p>
                <ul>
                    <li>Analyzed business requirements for Dynamics F&O/NAV.</li>
                    <li>Configured and customized Dynamics systems.</li>
                    <li>Provided user training and support.</li>
                </ul>
            </div>
        </div>
    </section>

    <section id="skills">
        <div class="container">
            <h2>Skills & Certifications</h2>
            <div class="skills-list">
                <div class="skill-category">
                    <h3>Finance Systems</h3>
                    <ul>
                        <li>Dynamics 365 (F&O)</li>
                        <li>Dynamics 365 Business Central</li>
                        <li>Dynamics NAV</li>
                        <li>Power BI</li>
                        <li>Salesforce</li>
                        <li>Oracle Fusion</li>
                        <li>Unit4 Agresso</li>
                        <li>Workday</li>
                        <li>Infor SunSystems</li>
                        <li>JET Reporting</li>
                    </ul>
                </div>
                <div class="skill-category">
                    <h3>Functional Skills</h3>
                    <ul>
                        <li>Financial Reporting (UK/US GAAP, IFRS)</li>
                        <li>Managerial Finance</li>
                        <li>Strategic Financial Planning</li>
                        <li>Business Analysis</li>
                        <li>Business Process Improvement</li>
                        <li>Internal Audit</li>
                        <li>Financial Modelling</li>
                    </ul>
                </div>
                <div class="skill-category">
                    <h3>Soft Skills</h3>
                    <ul>
                        <li>Project Management</li>
                        <li>Stakeholder Management</li>
                        <li>Communication</li>
                        <li>Problem Solving</li>
                        <li>Analytical Skills</li>
                        <li>Teamwork</li>
                    </ul>
                </div>
                <div class="skill-category">
                    <h3>Certifications</h3>
                    <ul>
                        <li>ACCA Qualified</li>
                        <li>Dynamics Business Central Finance Essentials</li>
                        <li>Microsoft Dynamics Consultant</li>
                        <li>Microsoft Dynamics 365 Finance and Operations Functional Consultant</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <section id="contact">
        <div class="container text-center">
            <h2>Contact Me</h2>
            <p>I am available for interim and contract opportunities. Please reach out to discuss how my expertise can benefit your organization.</p>
            <div class="contact-details">
                <p><i class="fas fa-envelope"></i> <a href="mailto:nickneouk@gmail.com">nickneouk@gmail.com</a></p>
                <p><i class="fab fa-linkedin"></i> <a href="linkedin.com/in/neonick" target="_blank">linkedin.com/in/neonick</a></p>
            </div>
        </div>
    </section>

    <footer>
        <div class="container text-center">
            <p>&copy; 2025 Nick Neo. All rights reserved.</p>
        </div>
    </footer>

    <script>
        //  Optional JavaScript (example for smooth scrolling)
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                document.querySelector(this.getAttribute
