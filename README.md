<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Nauman's Resume</title>
  <link rel="stylesheet" href="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.css">
  <script type="module" src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.esm.js"></script>
  <script nomodule src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.js"></script>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(to right, #e6e9f0, #eef1f5);
      margin: 0;
      padding: 30px;
    }
    .resume {
      display: flex;
      max-width: 1100px;
      background: #fff;
      margin: auto;
      padding: 0;
      border-radius: 20px;
      box-shadow: 0 10px 40px rgba(44, 62, 80, 0.15);
      overflow: hidden;
      animation: fadeInUp 1.2s cubic-bezier(.23,1.01,.32,1) 0.1s both;
    }
    @keyframes fadeInUp {
      0% { opacity: 0; transform: translateY(40px); }
      100% { opacity: 1; transform: translateY(0); }
    }
    .left-column {
      background: linear-gradient(135deg, #f7f9fa 80%, #e3eafc 100%);
      width: 320px;
      padding: 56px 32px 48px 32px;
      border-right: 1.5px solid #e0e6ed;
      display: flex;
      flex-direction: column;
      align-items: center;
      min-height: 100%;
      box-shadow: 2px 0 16px 0 rgba(52, 152, 219, 0.06);
      position: relative;
      z-index: 1;
    }
    .profile-photo {
      width: 120px;
      height: 120px;
      border-radius: 50%;
      object-fit: cover;
      border: 5px solid #3498db;
      margin-bottom: 22px;
      box-shadow: 0 4px 18px rgba(52, 152, 219, 0.15);
      background: #fff;
      transition: transform 0.5s cubic-bezier(.23,1.01,.32,1), box-shadow 0.4s;
      animation: photoPop 1.2s cubic-bezier(.23,1.01,.32,1) 0.2s both;
    }
    .profile-photo:hover {
      transform: scale(1.08) rotate(-3deg);
      box-shadow: 0 8px 32px rgba(52, 152, 219, 0.25);
    }
    @keyframes photoPop {
      0% { opacity: 0; transform: scale(0.7) rotate(-10deg); }
      100% { opacity: 1; transform: scale(1) rotate(0); }
    }
    .name {
      font-family: 'Montserrat', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      font-size: 2.1rem;
      font-weight: 700;
      color: #2c3e50;
      margin-bottom: 7px;
      text-align: center;
      letter-spacing: 1.2px;
      animation: fadeIn 1.2s 0.3s both;
    }
    .title {
      font-family: 'Montserrat', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      font-size: 1.1rem;
      color: #2980b9;
      font-weight: 500;
      margin-bottom: 18px;
      text-align: center;
      letter-spacing: 0.5px;
    }
    @keyframes fadeIn {
      0% { opacity: 0; }
      100% { opacity: 1; }
    }
    .contact-info {
      font-size: 15px;
      color: #555;
      margin-bottom: 36px;
      display: flex;
      flex-direction: column;
      gap: 12px;
      width: 100%;
      animation: fadeIn 1.2s 0.4s both;
    }
    .contact-info ion-icon {
      color: #3498db;
      margin-right: 8px;
      font-size: 18px;
      vertical-align: middle;
      transition: color 0.3s;
    }
    .contact-info a {
      position: relative;
      display: inline-block;
      transition: color 0.3s;
    }
    .contact-info a::after {
      content: '';
      display: block;
      width: 0;
      height: 2px;
      background: #3498db;
      transition: width 0.3s;
      position: absolute;
      left: 0;
      bottom: -2px;
    }
    .contact-info a:hover {
      color: #1a5276;
    }
    .contact-info a:hover::after {
      width: 100%;
    }
    .section {
      margin-bottom: 36px;
      width: 100%;
      opacity: 0;
      transform: translateY(30px);
      animation: sectionFadeIn 1.1s cubic-bezier(.23,1.01,.32,1) forwards;
      background: #fafdff;
      border-radius: 14px;
      box-shadow: 0 2px 12px rgba(52, 152, 219, 0.07);
      border: 1.5px solid #e3eafc;
      padding: 24px 22px 18px 22px;
      transition: box-shadow 0.3s, border 0.3s;
    }
    .section:hover {
      box-shadow: 0 6px 24px rgba(52, 152, 219, 0.13);
      border: 1.5px solid #3498db;
    }
    .section:not(:last-child)::after {
      content: '';
      display: block;
      margin: 24px auto 0 auto;
      width: 60%;
      height: 1.5px;
      background: linear-gradient(90deg, #e3eafc 0%, #3498db 100%);
      border-radius: 1px;
      opacity: 0.5;
    }
    .section:nth-child(1) { animation-delay: 0.5s; }
    .section:nth-child(2) { animation-delay: 0.7s; }
    .section:nth-child(3) { animation-delay: 0.9s; }
    .section:nth-child(4) { animation-delay: 1.1s; }
    .section:nth-child(5) { animation-delay: 1.3s; }
    .section:nth-child(6) { animation-delay: 1.5s; }
    .section:nth-child(7) { animation-delay: 1.7s; }
    @keyframes sectionFadeIn {
      0% { opacity: 0; transform: translateY(30px); }
      100% { opacity: 1; transform: translateY(0); }
    }
    h2 {
      font-family: 'Montserrat', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      font-size: 1.25rem;
      border-left: 5px solid #3498db;
      padding-left: 12px;
      margin-bottom: 15px;
      color: #1a5276;
      display: flex;
      align-items: center;
      gap: 10px;
      position: relative;
      overflow: hidden;
      transition: color 0.3s;
      cursor: pointer;
      font-weight: 700;
      letter-spacing: 0.5px;
    }
    h2 ion-icon {
      transition: transform 0.4s cubic-bezier(.23,1.01,.32,1), color 0.3s;
    }
    h2:hover ion-icon {
      transform: scale(1.2) rotate(-8deg);
      color: #2980b9;
    }
    h2::after {
      content: '';
      display: block;
      position: absolute;
      left: 0;
      bottom: 0;
      width: 0;
      height: 3px;
      background: linear-gradient(90deg, #3498db 60%, #6dd5ed 100%);
      transition: width 0.4s cubic-bezier(.23,1.01,.32,1);
    }
    h2:hover::after {
      width: 100%;
    }
    p, li {
      line-height: 1.8;
      color: #2c3e50;
      font-size: 1.05rem;
      letter-spacing: 0.01em;
    }
    ul {
      padding-left: 22px;
      margin-bottom: 0;
    }
    a {
      color: #2980b9;
      text-decoration: none;
      transition: color 0.3s;
      font-weight: 500;
    }
    a:hover {
      color: #1a5276;
      text-decoration: underline;
    }
    .highlight {
      font-weight: bold;
      color: #3498db;
    }
    .badges {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-top: 8px;
    }
    .badge {
      background-color: #ecf0f1;
      border-radius: 20px;
      padding: 7px 18px;
      font-size: 15px;
      color: #2c3e50;
      transition: background 0.2s, color 0.2s, box-shadow 0.2s, transform 0.3s;
      box-shadow: 0 1px 4px rgba(52, 152, 219, 0.07);
      cursor: pointer;
      opacity: 0;
      transform: translateY(20px) scale(0.95);
      animation: badgeFadeIn 0.7s cubic-bezier(.23,1.01,.32,1) forwards;
      font-family: 'Montserrat', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      font-weight: 500;
      letter-spacing: 0.03em;
    }
    .badges .badge:nth-child(1) { animation-delay: 1.1s; }
    .badges .badge:nth-child(2) { animation-delay: 1.2s; }
    .badges .badge:nth-child(3) { animation-delay: 1.3s; }
    .badges .badge:nth-child(4) { animation-delay: 1.4s; }
    .badges .badge:nth-child(5) { animation-delay: 1.5s; }
    .badge:hover {
      background-color: #3498db;
      color: #fff;
      box-shadow: 0 2px 8px rgba(52, 152, 219, 0.18);
      transform: scale(1.08) translateY(-2px);
    }
    @keyframes badgeFadeIn {
      0% { opacity: 0; transform: translateY(20px) scale(0.95); }
      100% { opacity: 1; transform: translateY(0) scale(1); }
    }
    .right-column {
      flex: 1;
      padding: 56px 60px 48px 60px;
      background: linear-gradient(120deg, #fafdff 80%, #eaf6fb 100%);
      position: relative;
      z-index: 0;
    }
    @media (max-width: 900px) {
      .resume {
        flex-direction: column;
      }
      .left-column, .right-column {
        width: 100%;
        padding: 32px 12px;
        border: none;
      }
      .left-column {
        align-items: flex-start;
      }
      .right-column {
        padding: 32px 12px;
      }
    }
  </style>
</head>
<body>
  <div class="resume">
    <div class="left-column">
      <img class="profile-photo" src="../nauman-anwar.png" alt="Profile Photo" />
      <div class="name">Nauman Anwar</div>
      <div class="contact-info">
        <span><ion-icon name="mail-outline"></ion-icon> <a href="mailto:nabhatti@gmail.com">nabhatti@gmail.com</a></span>
        <span><ion-icon name="call-outline"></ion-icon> +923148805857</span>
        <span><ion-icon name="location-outline"></ion-icon> Pindi Bhattian, Pakistan</span>
        <span><ion-icon name="logo-linkedin"></ion-icon> <a href="https://www.linkedin.com/in/nauman-anwar-98aba8248/" target="_blank">LinkedIn</a></span>
      </div>
      <div class="section">
        <h2><ion-icon name="school-outline"></ion-icon>Education</h2>
        <p><strong>Matriculation</strong> — Government High School No.1, Pindi Bhattain (2019 – 2021)</p>
        <p><strong>Intermediate Computer Science</strong> — Punjab Collage, Pindi Bhattain (2021 – 2023)</p>
        <p><strong>BSc Computer Science</strong> — University of Central Punjab (2023 – 2025)</p>
      </div>
            <div class="section">
        <h2><ion-icon name="language-outline"></ion-icon>Languages</h2>
        <div class="badges">
          <div class="badge">English - Fluent</div>
          <div class="badge">Urdu - Native</div>
        </div>
      </div>
      <div class="section">
        <h2><ion-icon name="construct-outline"></ion-icon>Skills</h2>
        <div class="badges">
          <div class="badge">Front-End Development</div>
          <div class="badge">C Language</div>
          <div class="badge">C++</div>
          <div class="badge">Andriod Studio</div>
          <div class="badge">Kotlin</div>
          <div class="badge">Wordpress</div>
          <div class="badge">Content Writing</div>
          <div class="badge">SEO</div>
        </div>
      </div>
    </div>
    <div class="right-column">
      <div class="section">
        <h2><ion-icon name="person-outline"></ion-icon> Summary</h2>
    <p>
      I'm a passionate and results-driven Computer Science student with a strong foundation in programming, front-end development, and digital marketing. My academic journey began with 
      <strong>1008/1100</strong> in Matriculation from Govt. High School No.1, Pindi Bhattian, and <strong>747/1100</strong> in ICS from Punjab College, Pindi Bhattian.
    </p>

    <h2> What I Do</h2>
    <p>
      As a <strong>professional SEO specialist</strong>, I help businesses grow their online presence through strategic optimization and performance analysis. I'm also skilled in developing clean and responsive front-end interfaces.
    </p>

    <h2>Technical Skills</h2>
    <ul>
      <li><strong>Programming:</strong> C, C++, Kotlin</li>
      <li><strong>Web Development:</strong> HTML, CSS, JavaScript</li>
      <li><strong>SEO:</strong> On-page, Off-page, Keyword Research, Analytics</li>
      <li><strong>Tools:</strong> Google Search Console, Google Analytics, Ahrefs</li>
    </ul>
</p>
      </div>
      <div class="section">
        <h2><ion-icon name="briefcase-outline"></ion-icon>Experience</h2>
        <p><strong>Content Writing</strong> — Freelance (October 2021 – Current)</p>
        <p><strong>Wordpress</strong> — Freelance (June 2024 – Current)</p>
        <p><strong>SEO</strong> — APEX Digital Marketers (July 2024 – April 2025)</p>
      </div>
      <div class="section">
        <h2><ion-icon name="happy-outline"></ion-icon> Hobbies</h2>
        <ul>
      <li><strong>Coding & App Development</strong> – Enjoy building small projects and exploring new programming languages like Kotlin and C++</li>
      <li><strong>Exploring SEO Trends</strong> – Passionate about learning the latest in digital marketing and search engine optimization</li>
      <li><strong>Web Design</strong> – Love experimenting with front-end technologies to create visually appealing interfaces</li>
      <li><strong>Tech Reading</strong> – Regularly read blogs, forums, and articles about software development and technology trends</li>
    </ul>
      </div>
    </div>
  </div>
</body>
</html> 
