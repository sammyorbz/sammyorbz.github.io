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
        position: relative;
    }

    /* Homepage Background Image */
    .homepage-body::before {
        content: '';
        position: fixed;
        top: 0;
        right: 0;
        width: 50%;
        height: 100%;
        background-image: url('/assets/images/Gemini_Generated_Image_kb5agvkb5agvkb5a.png);
        background-size: contain;
        background-position: right center;
        background-repeat: no-repeat;
        z-index: 1;
        opacity: 1;
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
        max-width: 50%;
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

        .hero-content {
            max-width: 100%;
        }

        /* Hide background image on mobile */
        .homepage-body::before {
            display: none;
        }
    }
</style>

<script>
    // Add homepage class to body
    document.addEventListener('DOMContentLoaded', function() {
        document.body.classList.add('homepage-body');
        
        // Simple animation on load
        const greeting = document.querySelector('.greeting');
        if (greeting) {
            greeting.style.opacity = '0';
            greeting.style.transform = 'translateY(20px)';
            
            setTimeout(() => {
                greeting.style.transition = 'opacity 0.8s ease, transform 0.8s ease';
                greeting.style.opacity = '1';
                greeting.style.transform = 'translateY(0)';
            }, 300);
        }
    });
</script>

<div class="container">
    <header>
        <nav>
            <div class="nav-links">
                <a href="/about">About Me</a>
                <a href="/experience">Experience</a>
                <a href="/projects">Projects</a>
                <a href="/contact">Contact</a>
            </div>
        </nav>
    </header>

    <section class="hero">
        <div class="hero-content">
            <span class="greeting">Hello</span>
            <div class="name">Samuel Nkrumah</div>
            <div class="title">Data Analyst | Physician Assistant</div>
        </div>
    </section>

    <div class="scroll-indicator">
        Scroll down
        <i class="fas fa-chevron-down"></i>
    </div>
</div>
