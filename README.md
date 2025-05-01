<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Dibyanjaya Panda - GitHub Profile</title>
  <style>
    :root {
      --primary: #00D1E8;
      --secondary: #9945FF;
      --dark: #0a1929;
      --light: #f8f9fa;
      --accent: #ff5252;
    }
    
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', 'Roboto', sans-serif;
    }
    
    body {
      background: linear-gradient(135deg, var(--dark), #142c44);
      color: var(--light);
      padding: 2rem;
      overflow-x: hidden;
    }
    
    .container {
      max-width: 900px;
      margin: 0 auto;
    }
    
    .header {
      text-align: center;
      margin-bottom: 2rem;
      position: relative;
      overflow: hidden;
      padding: 2rem 0;
    }
    
    .header:before {
      content: '';
      position: absolute;
      width: 100%;
      height: 5px;
      bottom: 0;
      left: 0;
      background: linear-gradient(90deg, var(--primary), var(--secondary), var(--accent));
      border-radius: 50px;
      animation: gradientSlide 3s infinite;
    }
    
    @keyframes gradientSlide {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }
    
    h1 {
      font-size: 3rem;
      margin-bottom: 0.5rem;
      background: linear-gradient(90deg, var(--primary), var(--secondary));
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      animation: colorFlow 5s infinite;
    }
    
    @keyframes colorFlow {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }
    
    h3 {
      font-size: 1.5rem;
      color: #ddd;
      margin-bottom: 1.5rem;
    }
    
    .typing-container {
      height: 80px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: 500;
      overflow: hidden;
      margin-bottom: 1rem;
    }
    
    .typewriter {
      color: var(--primary);
      font-size: 1.4rem;
      position: relative;
      font-family: 'Fira Code', monospace;
      overflow: hidden;
      white-space: nowrap;
      letter-spacing: 0.15em;
      animation: typing 5s steps(40, end) infinite;
    }
    
    @keyframes typing {
      0%, 100% {
        width: 0;
      }
      50%, 90% {
        width: 100%;
      }
    }
    
    .section {
      background: rgba(255, 255, 255, 0.05);
      border-radius: 12px;
      padding: 2rem;
      margin-bottom: 2rem;
      border: 1px solid rgba(255, 255, 255, 0.1);
      box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
      backdrop-filter: blur(8px);
      transform: translateY(20px);
      opacity: 0;
      animation: fadeUp 0.6s forwards;
      position: relative;
      overflow: hidden;
    }
    
    .section:before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 4px;
      height: 100%;
      background: linear-gradient(to bottom, var(--primary), var(--secondary));
      border-radius: 4px;
    }
    
    @keyframes fadeUp {
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
    
    .section:nth-child(2) { animation-delay: 0.2s; }
    .section:nth-child(3) { animation-delay: 0.4s; }
    .section:nth-child(4) { animation-delay: 0.6s; }
    .section:nth-child(5) { animation-delay: 0.8s; }
    
    .section-title {
      font-size: 1.5rem;
      margin-bottom: 1.5rem;
      display: flex;
      align-items: center;
      color: var(--primary);
    }
    
    .section-title svg {
      margin-right: 0.5rem;
    }
    
    .contact-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 1rem;
    }
    
    .contact-item {
      display: flex;
      align-items: center;
      margin-bottom: 1rem;
      padding: 0.8rem;
      background: rgba(255, 255, 255, 0.05);
      border-radius: 8px;
      transition: all 0.3s ease;
    }
    
    .contact-item:hover {
      background: rgba(255, 255, 255, 0.1);
      transform: translateY(-3px);
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
    }
    
    .contact-icon {
      margin-right: 0.5rem;
      color: var(--primary);
    }
    
    .contact-link {
      color: var(--light);
      text-decoration: none;
      transition: color 0.3s ease;
    }
    
    .contact-link:hover {
      color: var(--primary);
    }
    
    .tech-stack {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      justify-content: center;
    }
    
    .tech-item {
      display: flex;
      align-items: center;
      justify-content: center;
      width: 70px;
      height: 70px;
      background: rgba(255, 255, 255, 0.05);
      border-radius: 12px;
      transition: all 0.3s ease;
      position: relative;
      overflow: hidden;
    }
    
    .tech-item:hover {
      transform: translateY(-5px);
      background: rgba(255, 255, 255, 0.1);
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
    }
    
    .tech-item:hover:before {
      transform: scale(1.2);
    }
    
    .tech-item svg {
      width: 40px;
      height: 40px;
      z-index: 1;
    }
    
    .tech-item:before {
      content: '';
      position: absolute;
      width: 100%;
      height: 100%;
      background: radial-gradient(circle, rgba(255, 255, 255, 0.1) 0%, rgba(255, 255, 255, 0) 70%);
      transition: transform 0.5s ease;
    }
    
    .projects {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 1.5rem;
    }
    
    .project-card {
      background: rgba(255, 255, 255, 0.05);
      border-radius: 12px;
      overflow: hidden;
      transition: all 0.3s ease;
      border: 1px solid rgba(255, 255, 255, 0.1);
    }
    
    .project-card:hover {
      transform: translateY(-10px);
      box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
      border-color: var(--primary);
    }
    
    .project-img {
      height: 150px;
      width: 100%;
      background-color: #1e3a5a;
      position: relative;
      overflow: hidden;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    
    .project-img svg {
      width: 60px;
      height: 60px;
      opacity: 0.7;
    }
    
    .project-content {
      padding: 1.2rem;
    }
    
    .project-title {
      font-size: 1.2rem;
      font-weight: 600;
      margin-bottom: 0.5rem;
      color: var(--primary);
    }
    
    .project-desc {
      font-size: 0.9rem;
      margin-bottom: 1rem;
      color: #ddd;
    }
    
    .project-link {
      display: inline-block;
      padding: 0.5rem 1rem;
      background: linear-gradient(90deg, var(--primary), var(--secondary));
      border-radius: 30px;
      color: white;
      text-decoration: none;
      font-size: 0.9rem;
      font-weight: 500;
      transition: all 0.3s ease;
    }
    
    .project-link:hover {
      transform: scale(1.05);
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
    }
    
    .stats {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 1.5rem;
    }
    
    .stat-card {
      background: rgba(255, 255, 255, 0.05);
      border-radius: 12px;
      overflow: hidden;
      transition: all 0.3s ease;
      height: 150px;
      display: flex;
      align-items: center;
      justify-content: center;
      position: relative;
    }
    
    .stat-card img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
    
    .fun-fact {
      text-align: center;
      padding: 2rem;
      font-style: italic;
      position: relative;
    }
    
    .quote {
      font-size: 1.2rem;
      margin-bottom: 1rem;
      position: relative;
      padding: 0 1.5rem;
    }
    
    .quote:before, .quote:after {
      content: '"';
      font-size: 2rem;
      position: absolute;
      color: var(--primary);
      opacity: 0.5;
    }
    
    .quote:before {
      left: 0;
      top: -10px;
    }
    
    .quote:after {
      right: 0;
      bottom: -10px;
    }
    
    .footer {
      text-align: center;
      margin-top: 2rem;
      padding: 1rem 0;
      font-size: 0.9rem;
      color: #aaa;
    }
    
    .floating {
      animation: floating 3s ease-in-out infinite;
    }
    
    @keyframes floating {
      0% { transform: translateY(0px); }
      50% { transform: translateY(-10px); }
      100% { transform: translateY(0px); }
    }
    
    .heart {
      color: var(--accent);
      display: inline-block;
      animation: heartbeat 1.5s ease-in-out infinite;
    }
    
    @keyframes heartbeat {
      0% { transform: scale(1); }
      25% { transform: scale(1.3); }
      50% { transform: scale(1); }
      75% { transform: scale(1.3); }
      100% { transform: scale(1); }
    }
    
    .spotlight {
      position: absolute;
      width: 100%;
      height: 100%;
      top: 0;
      left: 0;
      background: radial-gradient(circle, rgba(0, 209, 232, 0.1) 0%, rgba(0, 0, 0, 0) 70%);
      opacity: 0;
      transition: opacity 0.5s ease;
      pointer-events: none;
    }
    
    .section:hover .spotlight {
      opacity: 1;
    }
    
    .animate-border {
      position: relative;
      overflow: hidden;
    }
    
    .animate-border:after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      width: 0;
      height: 2px;
      background-color: var(--primary);
      transition: width 0.3s ease;
    }
    
    .animate-border:hover:after {
      width: 100%;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="header">
      <h1>Hi 👋, I'm Dibyanjaya Panda</h1>
      <h3>🚀 Full-stack Developer | 🎓 MCA @ KIIT | Career-Tech Enthusiast</h3>
      
      <div class="typing-container">
        <div class="typewriter" id="typewriter"></div>
      </div>
    </div>
    
    <div class="section">
      <div class="spotlight"></div>
      <h2 class="section-title">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="floating">
          <path d="M18 6a4 4 0 0 0-4 4 4 4 0 0 0 4 4 4 4 0 0 0 4-4 4 4 0 0 0-4-4z"></path>
          <path d="M6 18a4 4 0 0 0 4-4 4 4 0 0 0-4-4 4 4 0 0 0-4 4 4 4 0 0 0 4 4z"></path>
          <path d="m14 9-2 2"></path>
          <path d="m10 15-2 2"></path>
        </svg>
        Portfolio & Contact
      </h2>
      <div class="contact-grid">
        <div class="contact-item">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="contact-icon">
            <rect x="2" y="3" width="20" height="14" rx="2" ry="2"></rect>
            <line x1="8" y1="21" x2="16" y2="21"></line>
            <line x1="12" y1="17" x2="12" y2="21"></line>
          </svg>
          <a href="https://dibyanjaya-portfolio.onrender.com" target="_blank" class="contact-link animate-border">Portfolio</a>
        </div>
        <div class="contact-item">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="contact-icon">
            <path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"></path>
            <rect x="2" y="9" width="4" height="12"></rect>
            <circle cx="4" cy="4" r="2"></circle>
          </svg>
          <a href="https://linkedin.com/in/dibyanjaya" target="_blank" class="contact-link animate-border">LinkedIn</a>
        </div>
        <div class="contact-item">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="contact-icon">
            <path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path>
            <polyline points="22,6 12,13 2,6"></polyline>
          </svg>
          <a href="mailto:dibyanjayapanda2580@gmail.com" class="contact-link animate-border">Email</a>
        </div>
        <div class="contact-item">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="contact-icon">
            <path d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z"></path>
            <polyline points="3.27 6.96 12 12.01 20.73 6.96"></polyline>
            <line x1="12" y1="22.08" x2="12" y2="12"></line>
          </svg>
          <a href="mailto:dibyanjayapanda2580@gmail.com" class="contact-link animate-border">Hire Me</a>
        </div>
      </div>
    </div>
    
    <div class="section">
      <div class="spotlight"></div>
      <h2 class="section-title">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="floating">
          <rect x="2" y="3" width="20" height="14" rx="2" ry="2"></rect>
          <line x1="8" y1="21" x2="16" y2="21"></line>
          <line x1="12" y1="17" x2="12" y2="21"></line>
        </svg>
        Tech Stack
      </h2>
      <div class="tech-stack">
        <div class="tech-item">
          <svg viewBox="0 0 128 128" xmlns="http://www.w3.org/2000/svg">
            <g fill="#61DAFB"><circle cx="64" cy="64" r="11.4"/><path d="M107.3 45.2c-2.2-.8-4.5-1.6-6.9-2.3.6-2.4 1.1-4.8 1.5-7.1 2.1-13.2-.2-22.5-6.6-26.1-1.9-1.1-4-1.6-6.4-1.6-7 0-15.9 5.2-24.9 13.9-9-8.7-17.9-13.9-24.9-13.9-2.4 0-4.5.5-6.4 1.6-6.4 3.7-8.7 13-6.6 26.1.4 2.3.9 4.7 1.5 7.1-2.4.7-4.7 1.4-6.9 2.3C8.2 50 1.4 56.6 1.4 64s6.9 14 19.3 18.8c2.2.8 4.5 1.6 6.9 2.3-.6 2.4-1.1 4.8-1.5 7.1-2.1 13.2.2 22.5 6.6 26.1 1.9 1.1 4 1.6 6.4 1.6 7.1 0 16-5.2 24.9-13.9 9 8.7 17.9 13.9 24.9 13.9 2.4 0 4.5-.5 6.4-1.6 6.4-3.7 8.7-13 6.6-26.1-.4-2.3-.9-4.7-1.5-7.1 2.4-.7 4.7-1.4 6.9-2.3 12.5-4.8 19.3-11.4 19.3-18.8s-6.8-14-19.3-18.8zM92.5 14.7c4.1 2.4 5.5 9.8 3.8 20.3-.3 2.1-.8 4.3-1.4 6.6-5.2-1.2-10.7-2-16.5-2.5-3.4-4.8-6.9-9.1-10.4-13 7.4-7.3 14.9-12.3 21-12.3 1.3 0 2.5.3 3.5.9zM81.3 74c-1.8 3.2-3.9 6.4-6.1 9.6-3.7.3-7.4.4-11.2.4-3.9 0-7.6-.1-11.2-.4-2.2-3.2-4.2-6.4-6-9.6-1.9-3.3-3.7-6.7-5.3-10 1.6-3.3 3.4-6.7 5.3-10 1.8-3.2 3.9-6.4 6.1-9.6 3.7-.3 7.4-.4 11.2-.4 3.9 0 7.6.1 11.2.4 2.2 3.2 4.2 6.4 6 9.6 1.9 3.3 3.7 6.7 5.3 10-1.7 3.3-3.4 6.6-5.3 10zm8.3-3.3c1.5 3.5 2.7 6.9 3.8 10.3-3.4.8-7 1.4-10.8 1.9 1.2-1.9 2.5-3.9 3.6-6 1.2-2.1 2.3-4.2 3.4-6.2zM64 97.8c-2.4-2.6-4.7-5.4-6.9-8.3 2.3.1 4.6.2 6.9.2 2.3 0 4.6-.1 6.9-.2-2.2 2.9-4.5 5.7-6.9 8.3zm-18.6-15c-3.8-.5-7.4-1.1-10.8-1.9 1.1-3.3 2.3-6.8 3.8-10.3 1.1 2 2.2 4.1 3.4 6.1 1.2 2.2 2.4 4.1 3.6 6.1zm-7-25.5c-1.5-3.5-2.7-6.9-3.8-10.3 3.4-.8 7-1.4 10.8-1.9-1.2 1.9-2.5 3.9-3.6 6-1.2 2.1-2.3 4.2-3.4 6.2zM64 30.2c2.4 2.6 4.7 5.4 6.9 8.3-2.3-.1-4.6-.2-6.9-.2-2.3 0-4.6.1-6.9.2 2.2-2.9 4.5-5.7 6.9-8.3zm22.2 21l-3.6-6c3.8.5 7.4 1.1 10.8 1.9-1.1 3.3-2.3 6.8-3.8 10.3-1.1-2.1-2.2-4.2-3.4-6.2zM31.7 35c-1.7-10.5-.3-17.9 3.8-20.3 1-.6 2.2-.9 3.5-.9 6 0 13.5 4.9 21 12.3-3.5 3.8-7 8.2-10.4 13-5.8.5-11.3 1.4-16.5 2.5-.6-2.3-1-4.5-1.4-6.6zM7 64c0-4.7 5.7-9.7 15.7-13.4 2-.8 4.2-1.5 6.4-2.1 1.6 5 3.6 10.3 6 15.6-2.4 5.3-4.5 10.5-6 15.5C15.3 75.6 7 69.6 7 64zm28.5 49.3c-4.1-2.4-5.5-9.8-3.8-20.3.3-2.1.8-4.3 1.4-6.6 5.2 1.2 10.7 2 16.5 2.5 3.4 4.8 6.9 9.1 10.4 13-7.4 7.3-14.9 12.3-21 12.3-1.3 0-2.5-.3-3.5-.9zM96.3 93c1.7 10.5.3 17.9-3.8 20.3-1 .6-2.2.9-3.5.9-6 0-13.5-4.9-21-12.3 3.5-3.8 7-8.2 10.4-13 5.8-.5 11.3-1.4 16.5-2.5.6 2.3 1 4.5 1.4 6.6zm9-15.6c-1.6 5-3.6 10.3-6 15.6-2.4-5.3-4.5-10.5-6-15.5 13.8-4 22.1-10 22.1-15.6 0-4.7-5.7-9.7-15.7-13.4-2-.8-4.2-1.5-6.4-2.1 1.6 5 3.6 10.3 6 15.6 2.4 5.4 4.5 10.6 6 15.4z"/></g>
          </svg>
        </div>
        <div class="tech-item">
          <svg viewBox="0 0 128 128" xmlns="http://www.w3.org/2000/svg">
            <path d="M64 0C28.7 0 0 28.7 0 64s28.7 64 64 64c11.2 0 21.7-2.9 30.8-7.9L48.4 55.3v36.6h-6.8V41.8h6.8l50.5 75.8C116.4 106.2 128 86.5 128 64c0-35.3-28.7-64-64-64zm22.1 84.6l-7.5-11.3V41.8h7.5v42.8z" fill="#000"/><path d="M64 0C28.7 0 0 28.7 0 64s28.7 64 64 64c11.2 0 21.7-2.9 30.8-7.9L48.4 55.3v36.6h-6.8V41.8h6.8l50.5 75.8C116.4 106.2 128 86.5 128 64c0-35.3-28.7-64-64-64zm22.1 84.6l-7.5-11.3V41.8h7.5v42.8z" fill="#fff"/>
          </svg>
        </div>
        <div class="tech-item">
          <svg viewBox="0 0 128 128" xmlns="http://www.w3.org/2000/svg">
            <path fill="#83CD29" d="M112.771 30.334L68.674 4.729c-2.781-1.584-6.402-1.584-9.205 0L14.901 30.334C12.031 31.985 10 35.088 10 38.407v51.142c0 3.319 2.084 6.423 4.954 8.083l11.775 6.688c5.628 2.772 7.617 2.772 10.178 2.772 8.333 0 13.093-5.039 13.093-13.828v-50.49c0-.713-.371-1.774-1.071-1.774h-5.623C42.594 41 41 42.061 41 42.773v50.49c0 3.896-3.
