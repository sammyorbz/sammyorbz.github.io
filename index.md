<style>
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    :root {
        --primary: #000000;
        --secondary: #666666;
        --accent: #000000;
        --light-bg: #ffffff;
    }

    body {
        background-color: var(--light-bg);
        color: var(--primary);
        line-height: 1.6;
        overflow-x: hidden;
        font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
        min-height: 100vh;
        position: relative;
    }

    .container {
        max-width: 1200px;
        margin: 0 auto;
        padding: 0 40px;
        position: relative;
        min-height: 100vh;
        display: flex;
        flex-direction: column;
    }

    /* Header Styles */
    header {
        padding: 40px 0 0 0;
    }

    nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .logo {
        font-size: 18px;
        font-weight: 600;
        color: var(--primary);
    }

    .nav-links {
        display: flex;
        gap: 40px;
        margin-left: auto;
        margin-right: 60px;
    }

    .nav-links a {
        text-decoration: none;
        color: var(--primary);
        font-weight: 400;
        font-size: 16px;
        transition: color 0.3s;
    }

    .nav-links a:hover {
        color: var(--secondary);
    }

    .header-right {
        display: flex;
        align-items: center;
        gap: 40px;
    }

    .stats {
        display: flex;
        gap: 30px;
    }

    .stat-item {
        text-align: center;
    }

    .stat-number {
        font-size: 20px;
        font-weight: 600;
        color: var(--primary);
        line-height: 1.2;
    }

    .stat-label {
        font-size: 12px;
        color: var(--secondary);
        margin-top: 2px;
        font-weight: 400;
    }

    .cta-button {
        background-color: var(--primary);
        color: white;
        border: none;
        padding: 12px 24px;
        border-radius: 25px;
        font-weight: 500;
        font-size: 14px;
        cursor: pointer;
        transition: all 0.3s;
    }

    .cta-button:hover {
        background-color: var(--secondary);
    }

    /* Main Content */
    .main-content {
        flex: 1;
        display: flex;
        align-items: center;
        position: relative;
        padding: 60px 0 100px 0;
    }

    .text-content {
        flex: 1;
        max-width: 50%;
    }

    .image-content {
        flex: 1;
        max-width: 50%;
        display: flex;
        justify-content: flex-end;
        align-items: center;
    }

    .profile-image {
        width: 400px;
        height: 500px;
        background: linear-gradient(135deg, #f5f5f5 0%, #e0e0e0 100%);
        border-radius: 10px;
        display: flex;
        align-items: center;
        justify-content: center;
        position: relative;
        overflow: hidden;
    }

    .profile-image img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        display: none;
    }

    .profile-image::after {
        content: 'Your Photo Here';
        color: var(--secondary);
        font-size: 16px;
        text-align: center;
    }

    .profile-image.has-image::after {
        display: none;
    }

    .profile-image.has-image img {
        display: block;
    }

    .greeting {
        font-size: 16px;
        color: var(--secondary);
        margin-bottom: 20px;
        display: block;
        font-weight: 400;
    }

    .main-title {
        font-size: 64px;
        font-weight: 700;
        line-height: 1.1;
        margin-bottom: 20px;
        letter-spacing: -1.5px;
    }

    .dash {
        font-size: 64px;
        font-weight: 300;
        margin-right: 5px;
    }

    .year {
        font-size: 16px;
        color: var(--secondary);
        margin-top: 40px;
        display: block;
        font-weight: 400;
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

    /* File Upload Section */
    .upload-section {
        position: fixed;
        top: 20px;
        left: 20px;
        background: white;
        padding: 15px;
        border-radius: 8px;
        box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        z-index: 1000;
        max-width: 300px;
    }

    .upload-section h4 {
        margin-bottom: 10px;
        font-size: 14px;
        color: var(--primary);
    }

    .upload-btn {
        background-color: var(--primary);
        color: white;
        border: none;
        padding: 8px 16px;
        border-radius: 5px;
        font-size: 12px;
        cursor: pointer;
        margin-right: 10px;
    }

    .remove-btn {
        background-color: #ff4444;
        color: white;
        border: none;
        padding: 8px 16px;
        border-radius: 5px;
        font-size: 12px;
        cursor: pointer;
    }

    /* Mobile Responsive */
    @media (max-width: 968px) {
        .container {
            padding: 0 20px;
        }

        .nav-links {
            display: none;
        }

        .stats {
            gap: 20px;
        }

        .main-content {
            flex-direction: column;
            text-align: center;
        }

        .text-content, .image-content {
            max-width: 100%;
        }

        .image-content {
            justify-content: center;
            margin-top: 40px;
        }

        .profile-image {
            width: 300px;
            height: 400px;
        }

        .main-title {
            font-size: 48px;
        }

        .upload-section {
            position: relative;
            top: auto;
            left: auto;
            margin: 20px auto;
            max-width: 100%;
        }
    }
</style>

<!-- Upload Section -->
<div class="upload-section">
    <h4>Add Your Profile Picture</h4>
    <input type="file" id="imageUpload" accept="image/*" style="display: none;">
    <button class="upload-btn" onclick="document.getElementById('imageUpload').click()">Choose Image</button>
    <button class="remove-btn" onclick="removeImage()">Remove Image</button>
    <p style="font-size: 11px; color: #666; margin-top: 8px; line-height: 1.3;">For best results, use a portrait photo with similar composition to the reference image.</p>
</div>

<div class="container">
    <header>
        <nav>
            <div class="logo">Samuel Nkrumah</div>
            <div class="nav-links">
                <a href="#about">About Me</a>
                <a href="#experience">Experience</a>
                <a href="#projects">Projects</a>
                <a href="#contact">Contact</a>
            </div>
            <div class="header-right">
                <div class="stats">
                    <div class="stat-item">
                        <div class="stat-number">+200</div>
                        <div class="stat-label">Project completed</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-number">+50</div>
                        <div class="stat-label">Startup raised</div>
                    </div>
                </div>
                <button class="cta-button">Book A Call</button>
            </div>
        </nav>
    </header>

    <section class="main-content">
        <div class="text-content">
            <span class="greeting">Hello</span>
            <h1 class="main-title">
                <span class="dash">—</span> It's Samuel Nkrumah<br>
                Data Analyst | Physician Assistant
            </h1>
            <span class="year">2024</span>
        </div>
        <div class="image-content">
            <div class="profile-image" id="profileImage">
                <img src="" alt="Samuel Nkrumah" id="profileImg">
            </div>
        </div>
    </section>

    <div class="scroll-indicator">
        Scroll down
        <i class="fas fa-chevron-down"></i>
    </div>
</div>

<script>
    // Image upload functionality
    document.getElementById('imageUpload').addEventListener('change', function(event) {
        const file = event.target.files[0];
        if (file) {
            const reader = new FileReader();
            reader.onload = function(e) {
                const profileImage = document.getElementById('profileImage');
                const profileImg = document.getElementById('profileImg');
                
                profileImg.src = e.target.result;
                profileImage.classList.add('has-image');
                
                // Save to localStorage
                localStorage.setItem('profileImage', e.target.result);
            };
            reader.readAsDataURL(file);
        }
    });

    // Remove image functionality
    function removeImage() {
        const profileImage = document.getElementById('profileImage');
        const profileImg = document.getElementById('profileImg');
        
        profileImg.src = '';
        profileImage.classList.remove('has-image');
        localStorage.removeItem('profileImage');
        document.getElementById('imageUpload').value = '';
    }

    // Load saved image on page load
    document.addEventListener('DOMContentLoaded', function() {
        const savedImage = localStorage.getItem('profileImage');
        if (savedImage) {
            const profileImage = document.getElementById('profileImage');
            const profileImg = document.getElementById('profileImg');
            
            profileImg.src = savedImage;
            profileImage.classList.add('has-image');
        }

        // Animation for main title
        const mainTitle = document.querySelector('.main-title');
        mainTitle.style.opacity = '0';
        mainTitle.style.transform = 'translateY(20px)';
        
        setTimeout(() => {
            mainTitle.style.transition = 'opacity 0.8s ease, transform 0.8s ease';
            mainTitle.style.opacity = '1';
            mainTitle.style.transform = 'translateY(0)';
        }, 300);
    });
</script>
