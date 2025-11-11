---
layout: default
title: Samuel Nkrumah - Data Analyst | Physician Assistant
---

<style>
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    :root {
        --primary: #111111;
        --secondary: #555555;
        --accent: #ff3366;
        --light-bg: #ffffff;
    }

    body {
        background-color: var(--light-bg);
        color: var(--primary);
        line-height: 1.6;
        overflow-x: hidden;
        font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
    }

    .container {
        max-width: 1200px;
        margin: 0 auto;
        padding: 0 20px;
        position: relative;
        z-index: 2;
    }

    /* Header Styles */
    header {
        padding: 30px 0;
        position: relative;
    }

    nav {
        display: flex;
        justify-content: flex-end;
        align-items: center;
    }

    .nav-links {
        display: flex;
        gap: 40px;
    }

    .nav-links a {
        text-decoration: none;
        color: var(--primary);
        font-weight: 500;
        transition: color 0.3s;
    }

    .nav-links a:hover {
        color: var(--accent);
    }

    /* Hero Section */
    .hero {
        display: flex;
        align-items: center;
        min-height: 100vh;
        padding: 60px 0;
        position: relative;
    }

    .hero-content {
        flex: 1;
        max-width: 60%;
    }

    .hero-image {
        position: absolute;
        right: 0;
        top: 50%;
        transform: translateY(-50%);
        width: 45%;
        height: 80%;
        display: flex;
        justify-content: center;
        align-items: center;
        z-index: 1;
    }

    .hero-image img {
        max-width: 100%;
        max-height: 100%;
        object-fit: contain;
        filter: none;
        opacity: 1;
    }

    .greeting {
        font-family: 'Inter', sans-serif;
        font-size: 11.25rem; /* 180px */
        font-weight: 700;
        line-height: 1.1;
        letter-spacing: -0.02em;
        color: #111111;
        margin-bottom: 20px;
        display: block;
    }

    .name {
        font-family: 'Inter', sans-serif;
        font-size: 1.375rem; /* 22px */
        font-weight: 400;
        line-height: 1.4;
        letter-spacing: 0em;
        color: #555555;
        margin-bottom: 5px;
    }

    .title {
        font-family: 'Inter', sans-serif;
        font-size: 1.375rem; /* 22px */
        font-weight: 400;
        line-height: 1.4;
        letter-spacing: 0em;
        color: #555555;
    }

    .scroll-indicator {
        position: absolute;
        bottom: 40px;
        left: 50%;
        transform: translateX(-50%);
        display: flex;
        flex-direction: column;
        align-items: center;
        color: var(--secondary);
        font-size: 14px;
        z-index: 3;
    }

    .scroll-indicator i {
        margin-top: 5px;
        animation: bounce 2s infinite;
    }

    @keyframes bounce {
        0%, 20%, 50%, 80%, 100% {
            transform: translateY(0);
        }
        40% {
            transform: translateY(-10px);
        }
        60% {
            transform: translateY(-5px);
        }
    }

    /* Mobile Responsive */
    @media (max-width: 768px) {
        .nav-links {
            gap: 20px;
        }

        .greeting {
            font-size: 5rem;
        }
        
        .name, .title {
            font-size: 1.125rem;
        }

        .hero {
            flex-direction: column;
        }

        .hero-content {
            max-width: 100%;
            margin-bottom: 40px;
        }

        .hero-image {
            position: relative;
            width: 100%;
            height: auto;
            top: auto;
            transform: none;
            margin-top: 40px;
        }
    }
</style>

<div class="container">
    <header>
        <nav>
            <div class="nav-links">
                <a href="#about">About Me</a>
                <a href="#experience">Experience</a>
                <a href="#projects">Projects</a>
                <a href="#contact">Contact</a>
            </div>
        </nav>
    </header>

    <section class="hero">
        <div class="hero-content">
            <span class="greeting">Hello</span>
            <div class="name">Samuel Nkrumah</div>
            <div class="title">Data Analyst | Physician Assistant</div>
        </div>
        <div class="hero-image">
            <img src="https://i.ibb.co/0QfL9v3/Gemini-Generated-Image-kb5agvkb5agvkb5a.png" alt="CANNOTCHING GAME MADE IN CHINA">
        </div>
    </section>

    <div class="scroll-indicator">
        Scroll down
        <i class="fas fa-chevron-down"></i>
    </div>
</div>

<script>
    // Simple animation on load
    document.addEventListener('DOMContentLoaded', function() {
        const greeting = document.querySelector('.greeting');
        greeting.style.opacity = '0';
        greeting.style.transform = 'translateY(20px)';
        
        setTimeout(() => {
            greeting.style.transition = 'opacity 0.8s ease, transform 0.8s ease';
            greeting.style.opacity = '1';
            greeting.style.transform = 'translateY(0)';
        }, 300);
    });
</script>

<!-- Add Font Awesome CDN in _includes/head.html or directly in config -->
