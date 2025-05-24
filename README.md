<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>হাসান মাহমুদ আহাদ | পোর্টফোলিও</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Hind+Siliguri:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #3498db;
            --secondary-color: #2ecc71;
            --dark-color: #2c3e50;
            --light-color: #ecf0f1;
            --text-color: #333;
            --bg-color: #fff;
            --card-bg: #f8f9fa;
        }

        .dark-mode {
            --primary-color: #2980b9;
            --secondary-color: #27ae60;
            --dark-color: #ecf0f1;
            --light-color: #2c3e50;
            --text-color: #f8f9fa;
            --bg-color: #1a1a2e;
            --card-bg: #16213e;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            transition: all 0.3s ease;
        }

        body {
            font-family: 'Hind Siliguri', sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Header Styles */
        header {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            padding: 60px 0;
            clip-path: polygon(0 0, 100% 0, 100% 85%, 0 100%);
            margin-bottom: 50px;
        }

        .hero-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
        }

        .hero-text {
            flex: 1;
            min-width: 300px;
            padding-right: 30px;
        }

        .hero-text h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            animation: fadeInUp 1s ease;
        }

        .hero-text h2 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            animation: fadeInUp 1.2s ease;
        }

        .hero-text p {
            font-size: 1.1rem;
            margin-bottom: 30px;
            animation: fadeInUp 1.4s ease;
        }

        .hero-image {
            flex: 1;
            min-width: 300px;
            text-align: center;
            animation: fadeIn 1.6s ease;
        }

        .hero-image img {
            width: 300px;
            height: 300px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid white;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        }

        .social-links {
            display: flex;
            gap: 15px;
            animation: fadeInUp 1.6s ease;
        }

        .social-links a {
            color: white;
            font-size: 1.5rem;
            transition: transform 0.3s ease;
        }

        .social-links a:hover {
            transform: translateY(-5px);
        }

        /* Theme Toggle */
        .theme-toggle {
            position: fixed;
            top: 20px;
            right: 20px;
            background: var(--primary-color);
            color: white;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
        }

        /* Section Styles */
        section {
            padding: 60px 0;
        }

        .section-title {
            text-align: center;
            font-size: 2.2rem;
            margin-bottom: 40px;
            color: var(--primary-color);
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background: var(--secondary-color);
        }

        /* About Section */
        .about-content {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
        }

        .about-text {
            flex: 1;
            min-width: 300px;
        }

        .about-text p {
            margin-bottom: 20px;
            font-size: 1.1rem;
        }

        .personal-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }

        .personal-info div {
            background: var(--card-bg);
            padding: 15px;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .personal-info span {
            font-weight: bold;
            color: var(--primary-color);
            display: block;
            margin-bottom: 5px;
        }

        /* Skills Section */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .skill-category {
            background: var(--card-bg);
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .skill-category h3 {
            margin-bottom: 15px;
            color: var(--primary-color);
        }

        .skill-item {
            margin-bottom: 10px;
        }

        .skill-name {
            display: flex;
            justify-content: space-between;
            margin-bottom: 5px;
        }

        .skill-bar {
            height: 10px;
            background: #ddd;
            border-radius: 5px;
            overflow: hidden;
        }

        .skill-progress {
            height: 100%;
            background: var(--primary-color);
            border-radius: 5px;
        }

        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }

        .project-card {
            background: var(--card-bg);
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-10px);
        }

        .project-image {
            height: 200px;
            overflow: hidden;
        }

        .project-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .project-card:hover .project-image img {
            transform: scale(1.1);
        }

        .project-info {
            padding: 20px;
        }

        .project-info h3 {
            margin-bottom: 10px;
            color: var(--primary-color);
        }

        .project-info p {
            margin-bottom: 15px;
        }

        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 15px;
        }

        .tech-tag {
            background: var(--primary-color);
            color: white;
            padding: 3px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
        }

        .project-links {
            display: flex;
            gap: 10px;
        }

        .project-links a {
            display: inline-block;
            padding: 8px 15px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s ease;
        }

        .demo-link {
            background: var(--primary-color);
            color: white;
        }

        .code-link {
            background: var(--secondary-color);
            color: white;
        }

        .project-links a:hover {
            opacity: 0.9;
            transform: translateY(-2px);
        }

        /* Contact Section */
        .contact-container {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
        }

        .contact-info {
            flex: 1;
            min-width: 300px;
        }

        .contact-info h3 {
            margin-bottom: 20px;
            color: var(--primary-color);
        }

        .contact-details {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .contact-item i {
            font-size: 1.2rem;
            color: var(--primary-color);
        }

        .contact-form {
            flex: 1;
            min-width: 300px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            background: var(--card-bg);
            color: var(--text-color);
        }

        .form-group textarea {
            height: 150px;
            resize: vertical;
        }

        .submit-btn {
            background: var(--primary-color);
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.3s ease;
        }

        .submit-btn:hover {
            background: var(--secondary-color);
            transform: translateY(-2px);
        }

        /* Footer */
        footer {
            background: var(--dark-color);
            color: white;
            text-align: center;
            padding: 20px 0;
            margin-top: 50px;
        }

        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes fadeInUp {
            from { 
                opacity: 0;
                transform: translateY(20px);
            }
            to { 
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Responsive Styles */
        @media (max-width: 768px) {
            .hero-content {
                flex-direction: column;
                text-align: center;
            }
            
            .hero-text {
                padding-right: 0;
                margin-bottom: 30px;
            }
            
            .social-links {
                justify-content: center;
            }
        }
    </style>
</head>
<body>
    <div class="theme-toggle">
        <i class="fas fa-moon"></i>
    </div>
    
    <header class="header">
        <div class="container">
            <div class="hero-content">
                <div class="hero-text">
                    <h1>হাসান মাহমুদ আহাদ</h1>
                    <h2>শিক্ষার্থী</h2>
                    <p>আমি হাসান মাহমুদ আহাদ। আমি একজন শিক্ষার্থী এবং বর্তমানে সরকারি বাংলা কলেজে দ্বাদশ শ্রেণিতে পড়াশোনা করছি। আমি আমার শিক্ষা ও জ্ঞানের পরিসর বাড়ানোর জন্য নিয়মিত অধ্যয়ন ও চর্চায় মনোযোগী থাকার চেষ্টা করি।</p>
                    <div class="social-links">
                        <a href="https://www.linkedin.com/in/hassan-mahmudd?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app" target="_blank"><i class="fab fa-linkedin"></i></a>
                        <a href="https://www.facebook.com/hachana.mahamuda.109421" target="_blank"><i class="fab fa-facebook"></i></a>
                        <a href="mailto:hassanmahmudahad847@gmail.com"><i class="fas fa-envelope"></i></a>
                    </div>
                </div>
                <div class="hero-image">
                    <img src="images/profile.jpg" alt="হাসান মাহমুদ আহাদ">
                </div>
            </div>
        </div>
    </header>

    <section class="about">
        <div class="container">
            <h2 class="section-title">আমার সম্পর্কে</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>আমি একজন মেধাবী ও পরিশ্রমী শিক্ষার্থী হিসেবে নিজেকে গড়ে তুলছি। জ্ঞান অর্জন ও দক্ষতা উন্নয়নে আমি সবসময় আগ্রহী। নতুন নতুন বিষয় শিখতে এবং সেগুলো বাস্তব জীবনে প্রয়োগ করতে আমি ভালোবাসি।</p>
                    <div class="personal-info">
                        <div>
                            <span>নাম:</span>
                            <p>হাসান মাহমুদ আহাদ</p>
                        </div>
                        <div>
                            <span>ইমেইল:</span>
                            <p>hassanmahmudahad847@gmail.com</p>
                        </div>
                        <div>
                            <span>ফোন:</span>
                            <p>01961082029</p>
                        </div>
                        <div>
                            <span>অবস্থান:</span>
                            <p>ঢাকা, বাংলাদেশ</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="skills">
        <div class="container">
            <h2 class="section-title">আমার দক্ষতা</h2>
            <div class="skills-container">
                <div class="skill-category">
                    <h3>প্রযুক্তিগত দক্ষতা</h3>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>HTML</span>
                            <span>90%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 90%;"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>CSS</span>
                            <span>85%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 85%;"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>JavaScript</span>
                            <span>75%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 75%;"></div>
                        </div>
                    </div>
                </div>
                <div class="skill-category">
                    <h3>ভাষা দক্ষতা</h3>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>বাংলা</span>
                            <span>100%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 100%;"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>ইংরেজি</span>
                            <span>80%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 80%;"></div>
                        </div>
                    </div>
                </div>
                <div class="skill-category">
                    <h3>অন্যান্য দক্ষতা</h3>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>গবেষণা</span>
                            <span>85%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 85%;"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>টিমওয়ার্ক</span>
                            <span>90%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 90%;"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="projects">
        <div class="container">
            <h2 class="section-title">আমার প্রকল্পসমূহ</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-image">
                        <img src="projects/project1.jpg" alt="প্রকল্প ১">
                    </div>
                    <div class="project-info">
                        <h3>ব্যক্তিগত ব্লগ ওয়েবসাইট</h3>
                        <p>একটি সম্পূর্ণ রেস্পন্সিভ ব্লগ ওয়েবসাইট যেখানে আমি আমার লেখা প্রকাশ করতে পারি।</p>
                        <div class="project-tech">
                            <span class="tech-tag">HTML</span>
                            <span class="tech-tag">CSS</span>
                            <span class="tech-tag">JavaScript</span>
                        </div>
                        <div class="project-links">
                            <a href="#" class="demo-link">ডেমো দেখুন</a>
                            <a href="#" class="code-link">কোড দেখুন</a>
                        </div>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-image">
                        <img src="projects/project2.jpg" alt="প্রকল্প ২">
                    </div>
                    <div class="project-info">
                        <h3>স্টুডেন্ট ম্যানেজমেন্ট সিস্টেম</h3>
                        <p>একটি ওয়েব অ্যাপ্লিকেশন যা শিক্ষার্থীদের তথ্য ব্যবস্থাপনা করতে সাহায্য করে।</p>
                        <div class="project-tech">
                            <span class="tech-tag">HTML</span>
                            <span class="tech-tag">CSS</span>
                            <span class="tech-tag">JavaScript</span>
                        </div>
                        <div class="project-links">
                            <a href="#" class="demo-link">ডেমো দেখুন</a>
                            <a href="#" class="code-link">কোড দেখুন</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="contact">
        <div class="container">
            <h2 class="section-title">যোগাযোগ করুন</h2>
            <div class="contact-container">
                <div class="contact-info">
                    <h3>আমার সাথে যোগাযোগ করুন</h3>
                    <div class="contact-details">
                        <div class="contact-item">
                            <i class="fas fa-envelope"></i>
                            <span>hassanmahmudahad847@gmail.com</span>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-phone"></i>
                            <span>01961082029</span>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-map-marker-alt"></i>
          
