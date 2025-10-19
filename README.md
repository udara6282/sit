<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Amila Wickramaarachchi - Science Class</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Global Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        :root {
            --primary: #8A2BE2;
            --primary-light: #9B4DFF;
            --primary-dark: #6A1B9A;
            --secondary: #FF4081;
            --accent: #00E5FF;
            --background: #1A0033;
            --card-bg: #2D004D;
            --text: #FFFFFF;
            --text-secondary: #E0E0E0;
        }
        
        body {
            background: linear-gradient(135deg, var(--background), #2D004D);
            color: var(--text);
            line-height: 1.6;
            min-height: 100vh;
            overflow-x: hidden;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        /* Animated Background Elements */
        .floating-elements {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            overflow: hidden;
        }
        
        .floating-element {
            position: absolute;
            border-radius: 50%;
            background: rgba(138, 43, 226, 0.1);
            animation: float 15s infinite linear;
        }
        
        .floating-element:nth-child(1) {
            width: 80px;
            height: 80px;
            top: 10%;
            left: 10%;
            animation-delay: 0s;
        }
        
        .floating-element:nth-child(2) {
            width: 120px;
            height: 120px;
            top: 60%;
            left: 80%;
            animation-delay: -5s;
        }
        
        .floating-element:nth-child(3) {
            width: 60px;
            height: 60px;
            top: 80%;
            left: 20%;
            animation-delay: -10s;
        }
        
        .floating-element:nth-child(4) {
            width: 100px;
            height: 100px;
            top: 30%;
            left: 70%;
            animation-delay: -7s;
        }
        
        @keyframes float {
            0% {
                transform: translateY(0) rotate(0deg);
                opacity: 0.7;
            }
            50% {
                transform: translateY(-20px) rotate(180deg);
                opacity: 0.3;
            }
            100% {
                transform: translateY(0) rotate(360deg);
                opacity: 0.7;
            }
        }
        
        /* Header Styles */
        header {
            background: rgba(45, 0, 77, 0.8);
            backdrop-filter: blur(10px);
            color: white;
            padding: 20px 0;
            box-shadow: 0 4px 20px rgba(138, 43, 226, 0.3);
            position: relative;
            overflow: hidden;
        }
        
        header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(90deg, var(--primary), var(--secondary), var(--accent), var(--primary));
            animation: rainbow 3s linear infinite;
        }
        
        @keyframes rainbow {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        .logo-container {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo-icon {
            width: 70px;
            height: 70px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            box-shadow: 0 0 20px rgba(138, 43, 226, 0.5);
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { box-shadow: 0 0 20px rgba(138, 43, 226, 0.5); }
            50% { box-shadow: 0 0 30px rgba(138, 43, 226, 0.8); }
            100% { box-shadow: 0 0 20px rgba(138, 43, 226, 0.5); }
        }
        
        .logo-icon i {
            font-size: 30px;
            color: white;
        }
        
        .logo-text h1 {
            font-size: 28px;
            margin-bottom: 5px;
            background: linear-gradient(90deg, var(--primary), var(--secondary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .logo-text p {
            font-size: 14px;
            opacity: 0.9;
            color: var(--text-secondary);
        }
        
        /* Login Form Styles */
        .login-container {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 80vh;
            padding: 40px 0;
        }
        
        .login-form {
            background: rgba(45, 0, 77, 0.7);
            backdrop-filter: blur(10px);
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            width: 100%;
            max-width: 400px;
            border: 1px solid rgba(138, 43, 226, 0.3);
            position: relative;
            overflow: hidden;
        }
        
        .login-form::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(138, 43, 226, 0.1), transparent);
            transform: rotate(45deg);
            animation: shine 3s infinite;
        }
        
        @keyframes shine {
            0% { transform: translateX(-100%) translateY(-100%) rotate(45deg); }
            100% { transform: translateX(100%) translateY(100%) rotate(45deg); }
        }
        
        .login-form h2 {
            text-align: center;
            margin-bottom: 30px;
            color: var(--text);
            font-size: 28px;
            position: relative;
        }
        
        .login-form h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            border-radius: 3px;
        }
        
        .form-group {
            margin-bottom: 25px;
            position: relative;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
            color: var(--text-secondary);
        }
        
        .form-group input {
            width: 100%;
            padding: 15px;
            background: rgba(26, 0, 51, 0.5);
            border: 1px solid rgba(138, 43, 226, 0.3);
            border-radius: 10px;
            font-size: 16px;
            color: var(--text);
            transition: all 0.3s;
        }
        
        .form-group input:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 10px rgba(138, 43, 226, 0.5);
        }
        
        .login-btn {
            width: 100%;
            padding: 15px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            border: none;
            border-radius: 10px;
            font-size: 18px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
        }
        
        .login-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(138, 43, 226, 0.4);
        }
        
        .login-btn:active {
            transform: translateY(0);
        }
        
        .login-btn::after {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: 0.5s;
        }
        
        .login-btn:hover::after {
            left: 100%;
        }
        
        .error-message {
            color: #FF4081;
            margin-top: 10px;
            text-align: center;
            display: none;
            padding: 10px;
            background: rgba(255, 64, 129, 0.1);
            border-radius: 5px;
            border-left: 3px solid #FF4081;
        }
        
        /* Dashboard Styles */
        .dashboard {
            display: none;
        }
        
        .dashboard-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 30px;
            padding: 20px;
            background: rgba(45, 0, 77, 0.7);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            border: 1px solid rgba(138, 43, 226, 0.3);
        }
        
        .welcome-message h2 {
            color: var(--text);
            font-size: 24px;
            margin-bottom: 5px;
        }
        
        .welcome-message p {
            color: var(--text-secondary);
        }
        
        .logout-btn {
            background: linear-gradient(135deg, #FF4081, #F50057);
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.3s;
            font-weight: 600;
        }
        
        .logout-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(255, 64, 129, 0.4);
        }
        
        /* Grade Selection */
        .grade-selection {
            margin-bottom: 30px;
        }
        
        .grade-selection h3 {
            margin-bottom: 20px;
            color: var(--text);
            font-size: 22px;
            text-align: center;
            position: relative;
            padding-bottom: 10px;
        }
        
        .grade-selection h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 3px;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            border-radius: 3px;
        }
        
        .grade-buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
        }
        
        .grade-btn {
            background: linear-gradient(135deg, var(--primary), var(--primary-light));
            color: white;
            border: none;
            padding: 15px 25px;
            border-radius: 12px;
            cursor: pointer;
            transition: all 0.3s;
            font-size: 18px;
            font-weight: 600;
            min-width: 120px;
            box-shadow: 0 5px 15px rgba(138, 43, 226, 0.3);
            position: relative;
            overflow: hidden;
        }
        
        .grade-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(138, 43, 226, 0.5);
        }
        
        .grade-btn:active {
            transform: translateY(0);
        }
        
        .grade-btn::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transform: translateX(-100%);
        }
        
        .grade-btn:hover::after {
            transform: translateX(100%);
            transition: transform 0.6s;
        }
        
        /* Video Lessons */
        .video-lessons {
            display: none;
        }
        
        .video-lessons h3 {
            margin-bottom: 20px;
            color: var(--text);
            font-size: 24px;
            text-align: center;
        }
        
        .back-btn {
            background: linear-gradient(135deg, #6A1B9A, #8A2BE2);
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 10px;
            cursor: pointer;
            margin-bottom: 20px;
            transition: all 0.3s;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .back-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(138, 43, 226, 0.4);
        }
        
        .videos-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 25px;
        }
        
        .video-card {
            background: rgba(45, 0, 77, 0.7);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
            transition: all 0.3s;
            border: 1px solid rgba(138, 43, 226, 0.3);
            position: relative;
        }
        
        .video-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(138, 43, 226, 0.3);
        }
        
        .video-thumbnail {
            height: 180px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 50px;
            position: relative;
            overflow: hidden;
            cursor: pointer;
        }
        
        .video-thumbnail::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, transparent, rgba(255, 255, 255, 0.1), transparent);
            transform: translateX(-100%);
        }
        
        .video-card:hover .video-thumbnail::before {
            transform: translateX(100%);
            transition: transform 0.6s;
        }
        
        .video-thumbnail img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .play-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            transition: opacity 0.3s;
        }
        
        .video-thumbnail:hover .play-overlay {
            opacity: 1;
        }
        
        .video-info {
            padding: 20px;
        }
        
        .video-info h4 {
            margin-bottom: 10px;
            color: var(--text);
            font-size: 18px;
        }
        
        .video-info p {
            font-size: 14px;
            color: var(--text-secondary);
            margin-bottom: 15px;
        }
        
        .watch-btn {
            background: linear-gradient(135deg, var(--primary), var(--primary-light));
            color: white;
            border: none;
            padding: 10px 15px;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s;
            width: 100%;
            font-weight: 600;
        }
        
        .watch-btn:hover {
            background: linear-gradient(135deg, var(--primary-light), var(--secondary));
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(138, 43, 226, 0.4);
        }
        
        /* Video Player Modal */
        .video-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.9);
            z-index: 1000;
            align-items: center;
            justify-content: center;
        }
        
        .video-modal-content {
            background: var(--card-bg);
            border-radius: 15px;
            width: 90%;
            max-width: 900px;
            overflow: hidden;
            box-shadow: 0 15px 40px rgba(138, 43, 226, 0.3);
            border: 1px solid rgba(138, 43, 226, 0.5);
        }
        
        .video-modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 20px;
            background: linear-gradient(90deg, var(--primary), var(--primary-dark));
            color: white;
        }
        
        .video-modal-header h3 {
            margin: 0;
            font-size: 20px;
        }
        
        .close-modal {
            background: none;
            border: none;
            color: white;
            font-size: 24px;
            cursor: pointer;
            transition: transform 0.3s;
        }
        
        .close-modal:hover {
            transform: rotate(90deg);
        }
        
        .video-player-container {
            position: relative;
            padding-bottom: 56.25%; /* 16:9 aspect ratio */
            height: 0;
            overflow: hidden;
        }
        
        .video-player-container iframe,
        .video-player-container video {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: none;
        }
        
        .video-description {
            padding: 20px;
            color: var(--text-secondary);
        }
        
        .loading-message {
            text-align: center;
            padding: 20px;
            color: var(--text-secondary);
        }
        
        /* Footer */
        footer {
            background: rgba(26, 0, 51, 0.8);
            color: white;
            text-align: center;
            padding: 30px 0;
            margin-top: 50px;
            border-top: 1px solid rgba(138, 43, 226, 0.3);
        }
        
        footer p {
            margin-bottom: 10px;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 15px;
        }
        
        .social-links a {
            color: var(--text-secondary);
            font-size: 20px;
            transition: all 0.3s;
        }
        
        .social-links a:hover {
            color: var(--primary);
            transform: translateY(-3px);
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .logo-container {
                flex-direction: column;
                text-align: center;
            }
            
            .logo {
                justify-content: center;
                margin-bottom: 10px;
            }
            
            .dashboard-header {
                flex-direction: column;
                align-items: flex-start;
            }
            
            .logout-btn {
                margin-top: 15px;
            }
            
            .videos-container {
                grid-template-columns: 1fr;
            }
            
            .grade-buttons {
                gap: 10px;
            }
            
            .grade-btn {
                min-width: 100px;
                padding: 12px 20px;
            }
        }
    </style>
</head>
<body>
    <!-- Animated Background Elements -->
    <div class="floating-elements">
        <div class="floating-element"></div>
        <div class="floating-element"></div>
        <div class="floating-element"></div>
        <div class="floating-element"></div>
    </div>

    <!-- Header Section -->
    <header>
        <div class="container">
            <div class="logo-container">
                <div class="logo">
                    <div class="logo-icon">
                        <i class="fas fa-atom"></i>
                    </div>
                    <div class="logo-text">
                        <h1>Niuro Science</h1>
                        <p>Online learning platforme</p>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <!-- Login Section -->
    <section class="login-container" id="loginSection">
        <div class="login-form">
            <h2>NIURO SCIENCE</h2>
            <h3>Login to Access Lessons</h3>
            <form id="loginForm">
                <div class="form-group">
                    <label for="username">Username</label>
                    <input type="text" id="username" placeholder="Enter your username" required>
                </div>
                <div class="form-group">
                    <label for="password">Password</label>
                    <input type="password" id="password" placeholder="Enter your password" required>
                </div>
                <button type="submit" class="login-btn">Login</button>
                <div class="error-message" id="errorMessage">Invalid username or password. Please try again.</div>
            </form>
        </div>
    </section>

    <!-- Dashboard Section (Initially Hidden) -->
    <section class="dashboard container" id="dashboard">
        <div class="dashboard-header">
            <div class="welcome-message">
                <h2>Welcome to Niuro Science!</h2>
                <p>Select your grade to access video lessons</p>
            </div>
            <button class="logout-btn" id="logoutBtn">Logout</button>
        </div>

        <div class="grade-selection">
            <h3>Select Your Grade</h3>
            <div class="grade-buttons">
                <button class="grade-btn" data-grade="6">Grade 6</button>
                <button class="grade-btn" data-grade="7">Grade 7</button>
                <button class="grade-btn" data-grade="8">Grade 8</button>
                <button class="grade-btn" data-grade="9">Grade 9</button>
                <button class="grade-btn" data-grade="10">Grade 10</button>
                <button class="grade-btn" data-grade="11">Grade 11</button>
            </div>
        </div>

        <!-- Video Lessons for Each Grade (Initially Hidden) -->
        <div class="video-lessons" id="videoLessons">
            <button class="back-btn" id="backBtn"><i class="fas fa-arrow-left"></i> Back to Grade Selection</button>
            <h3 id="gradeTitle">Grade 6 Science Lessons</h3>
            <div class="videos-container" id="videosContainer">
                <!-- Video cards will be dynamically inserted here -->
            </div>
        </div>
    </section>

    <!-- Video Player Modal -->
    <div class="video-modal" id="videoModal">
        <div class="video-modal-content">
            <div class="video-modal-header">
                <h3 id="modalTitle">Video Title</h3>
                <button class="close-modal" id="closeModal">&times;</button>
            </div>
            <div class="video-player-container" id="videoPlayer">
                <div class="loading-message">
                    <i class="fas fa-spinner fa-spin"></i> Loading video...
                </div>
            </div>
            <div class="video-description">
                <p id="modalDescription">Video description will appear here.</p>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>&copy; 2025 Niuro Science. All rights reserved.</p>
            <p>Amila Wickramaarachchi</p>
            <div class="social-links">
                <a href="#"><i class="fab fa-facebook"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
                <a href="#"><i class="fab fa-youtube"></i></a>
            </div>
        </div>
    </footer>

    <script>
        // Sample user credentials
        const validUsers = [
            { username: "student", password: "science123" },
            { username: "teacher", password: "teach456" },
            { username: "admin", password: "admin789" },
            { username: "Udara", password: "Udara6282" }
        ];

        // Function to convert Google Drive shareable link to embed URL
        function getGoogleDriveEmbedUrl(shareableLink) {
            // Extract file ID from Google Drive URL
            const fileIdMatch = shareableLink.match(/[-\w]{25,}/);
            if (fileIdMatch) {
                return `https://drive.google.com/file/d/${fileIdMatch[0]}/preview`;
            }
            return shareableLink;
        }

        // Function to get Google Drive thumbnail URL
        function getGoogleDriveThumbnailUrl(shareableLink) {
            const fileIdMatch = shareableLink.match(/[-\w]{25,}/);
            if (fileIdMatch) {
                return `https://drive.google.com/thumbnail?id=${fileIdMatch[0]}&sz=w300-h180`;
            }
            return "https://via.placeholder.com/300x180/8A2BE2/ffffff?text=Science+Lesson";
        }

        // Sample video lessons data with Google Drive links
        const videoLessons = {
            6: [
                { 
                    title: "Introduction to Science", 
                    description: "Learn the basics of scientific methods and inquiry. This lesson covers observation, hypothesis formation, and the scientific process.", 
                    duration: "15:30",
                    // Replace with your actual Google Drive shareable link
                    videoUrl: "https://drive.google.com/file/d/1ltXrlmit9isYZSKYbwF6mMFG1HaKVkG7/view?usp=sharing",
                    // You can use the same Google Drive link for thumbnail or provide a custom one
                    thumbnail: "https://drive.google.com/thumbnail?id=YOUR_FILE_ID_1&sz=w300-h180"
                },
                { 
                    title: "Living Organisms", 
                    description: "Understanding the characteristics of living things. Explore what makes something alive and the different classifications of organisms.", 
                    duration: "22:45",
                    videoUrl: "https://drive.google.com/file/d/YOUR_FILE_ID_2/view?usp=sharing",
                    thumbnail: "https://drive.google.com/thumbnail?id=YOUR_FILE_ID_2&sz=w300-h180"
                },
                { 
                    title: "States of Matter", 
                    description: "Solid, liquid and gas - properties and changes. Learn about matter and how it transforms between different states.", 
                    duration: "18:20",
                    videoUrl: "https://drive.google.com/file/d/YOUR_FILE_ID_3/view?usp=sharing",
                    thumbnail: "https://drive.google.com/thumbnail?id=YOUR_FILE_ID_3&sz=w300-h180"
                }
            ],
            7: [
                { 
                    title: "Cell Structure", 
                    description: "Exploring plant and animal cells. Discover the basic building blocks of life and their functions.", 
                    duration: "20:15",
                    videoUrl: "https://drive.google.com/file/d/YOUR_FILE_ID_4/view?usp=sharing",
                    thumbnail: "https://drive.google.com/thumbnail?id=YOUR_FILE_ID_4&sz=w300-h180"
                },
                { 
                    title: "Chemical Reactions", 
                    description: "Introduction to chemical changes. Understand what happens during chemical reactions.", 
                    duration: "24:30",
                    videoUrl: "https://drive.google.com/file/d/YOUR_FILE_ID_5/view?usp=sharing",
                    thumbnail: "https://drive.google.com/thumbnail?id=YOUR_FILE_ID_5&sz=w300-h180"
                }
            ],
            8: [
                { 
                    title: "Microorganisms", 
                    description: "Bacteria, viruses, and their impact. Discover the microscopic world and its importance.", 
                    duration: "23:40",
                    videoUrl: "https://drive.google.com/file/d/YOUR_FILE_ID_6/view?usp=sharing",
                    thumbnail: "https://drive.google.com/thumbnail?id=YOUR_FILE_ID_6&sz=w300-h180"
                }
            ],
            9: [
                { 
                    title: "Genetics and Heredity", 
                    description: "DNA, genes, and inheritance patterns. Explore how traits are passed from parents to offspring.", 
                    duration: "32:10",
                    videoUrl: "https://drive.google.com/file/d/YOUR_FILE_ID_7/view?usp=sharing",
                    thumbnail: "https://drive.google.com/thumbnail?id=YOUR_FILE_ID_7&sz=w300-h180"
                }
            ],
            10: [
                { 
                    title: "Human Physiology", 
                    description: "Detailed study of body systems. Take an in-depth look at human anatomy and physiology.", 
                    duration: "38:15",
                    videoUrl: "https://drive.google.com/file/d/YOUR_FILE_ID_8/view?usp=sharing",
                    thumbnail: "https://drive.google.com/thumbnail?id=YOUR_FILE_ID_8&sz=w300-h180"
                }
            ],
            11: [
                { 
                    title: "Advanced Genetics", 
                    description: "Molecular biology and biotechnology. Explore advanced genetic concepts and applications.", 
                    duration: "45:20",
                    videoUrl: "https://drive.google.com/file/d/YOUR_FILE_ID_9/view?usp=sharing",
                    thumbnail: "https://drive.google.com/thumbnail?id=YOUR_FILE_ID_9&sz=w300-h180"
                }
            ]
        };

        // DOM Elements
        const loginSection = document.getElementById('loginSection');
        const loginForm = document.getElementById('loginForm');
        const errorMessage = document.getElementById('errorMessage');
        const dashboard = document.getElementById('dashboard');
        const logoutBtn = document.getElementById('logoutBtn');
        const gradeButtons = document.querySelectorAll('.grade-btn');
        const videoLessonsSection = document.getElementById('videoLessons');
        const backBtn = document.getElementById('backBtn');
        const gradeTitle = document.getElementById('gradeTitle');
        const videosContainer = document.getElementById('videosContainer');
        const videoModal = document.getElementById('videoModal');
        const closeModal = document.getElementById('closeModal');
        const modalTitle = document.getElementById('modalTitle');
        const modalDescription = document.getElementById('modalDescription');
        const videoPlayer = document.getElementById('videoPlayer');

        // Login Form Submission
        loginForm.addEventListener('submit', function(e) {
            e.preventDefault();
            
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            
            // Check if credentials are valid
            const isValidUser = validUsers.some(user => 
                user.username === username && user.password === password
            );
            
            if (isValidUser) {
                // Successful login
                loginSection.style.display = 'none';
                dashboard.style.display = 'block';
                errorMessage.style.display = 'none';
                
                // Add a subtle entrance animation
                dashboard.style.opacity = '0';
                dashboard.style.transform = 'translateY(20px)';
                
                setTimeout(() => {
                    dashboard.style.transition = 'all 0.5s ease';
                    dashboard.style.opacity = '1';
                    dashboard.style.transform = 'translateY(0)';
                }, 100);
            } else {
                // Failed login
                errorMessage.style.display = 'block';
                
                // Shake animation for error
                loginForm.style.animation = 'shake 0.5s';
                setTimeout(() => {
                    loginForm.style.animation = '';
                }, 500);
            }
        });

        // Logout Functionality
        logoutBtn.addEventListener('click', function() {
            dashboard.style.display = 'none';
            loginSection.style.display = 'flex';
            loginForm.reset();
            
            // Add a subtle exit animation
            dashboard.style.opacity = '0';
            dashboard.style.transform = 'translateY(20px)';
        });

        // Grade Selection
        gradeButtons.forEach(button => {
            button.addEventListener('click', function() {
                const grade = this.getAttribute('data-grade');
                showVideoLessons(grade);
            });
        });

        // Back Button
        backBtn.addEventListener('click', function() {
            videoLessonsSection.style.display = 'none';
            document.querySelector('.grade-selection').style.display = 'block';
        });

        // Close Modal
        closeModal.addEventListener('click', function() {
            videoModal.style.display = 'none';
            // Clear the video player when modal is closed
            videoPlayer.innerHTML = '<div class="loading-message"><i class="fas fa-spinner fa-spin"></i> Loading video...</div>';
        });

        // Close modal when clicking outside
        videoModal.addEventListener('click', function(e) {
            if (e.target === videoModal) {
                videoModal.style.display = 'none';
                videoPlayer.innerHTML = '<div class="loading-message"><i class="fas fa-spinner fa-spin"></i> Loading video...</div>';
            }
        });

        // Function to display video lessons for selected grade
        function showVideoLessons(grade) {
            document.querySelector('.grade-selection').style.display = 'none';
            videoLessonsSection.style.display = 'block';
            gradeTitle.textContent = `Grade ${grade} Science Lessons`;
            
            // Add entrance animation
            videoLessonsSection.style.opacity = '0';
            videoLessonsSection.style.transform = 'translateY(20px)';
            
            setTimeout(() => {
                videoLessonsSection.style.transition = 'all 0.5s ease';
                videoLessonsSection.style.opacity = '1';
                videoLessonsSection.style.transform = 'translateY(0)';
            }, 100);
            
            // Clear previous videos
            videosContainer.innerHTML = '';
            
            // Check if grade has videos
            if (!videoLessons[grade] || videoLessons[grade].length === 0) {
                videosContainer.innerHTML = '<p>No videos available for this grade yet.</p>';
                return;
            }
            
            // Add videos for selected grade
            videoLessons[grade].forEach((video, index) => {
                const videoCard = document.createElement('div');
                videoCard.className = 'video-card';
                
                // Add staggered animation delay
                videoCard.style.animationDelay = `${index * 0.1}s`;
                
                // Get thumbnail URL - use Google Drive thumbnail or placeholder
                const thumbnailUrl = video.thumbnail || 
                    getGoogleDriveThumbnailUrl(video.videoUrl) || 
                    "https://via.placeholder.com/300x180/8A2BE2/ffffff?text=Science+Lesson";
                
                videoCard.innerHTML = `
                    <div class="video-thumbnail" data-video-url="${video.videoUrl}">
                        <img src="${thumbnailUrl}" alt="${video.title}" 
                             onerror="this.src='https://via.placeholder.com/300x180/8A2BE2/ffffff?text=Science+Lesson'">
                        <div class="play-overlay">
                            <i class="fas fa-play-circle fa-3x"></i>
                        </div>
                    </div>
                    <div class="video-info">
                        <h4>${video.title}</h4>
                        <p>${video.description}</p>
                        <p><strong>Duration:</strong> ${video.duration}</p>
                        <button class="watch-btn" data-video-url="${video.videoUrl}" data-title="${video.title}" data-description="${video.description}">Watch Lesson</button>
                    </div>
                `;
                videosContainer.appendChild(videoCard);
            });
            
            // Add event listeners to watch buttons
            document.querySelectorAll('.watch-btn').forEach(button => {
                button.addEventListener('click', function() {
                    const videoUrl = this.getAttribute('data-video-url');
                    const title = this.getAttribute('data-title');
                    const description = this.getAttribute('data-description');
                    playVideo(videoUrl, title, description);
                });
            });
            
            // Add event listeners to thumbnails
            document.querySelectorAll('.video-thumbnail').forEach(thumbnail => {
                thumbnail.addEventListener('click', function() {
                    const videoUrl = this.getAttribute('data-video-url');
                    const title = this.parentElement.querySelector('h4').textContent;
                    const description = this.parentElement.querySelector('p').textContent;
                    playVideo(videoUrl, title, description);
                });
            });
        }

        // Function to play video in modal
        function playVideo(videoUrl, title, description) {
            modalTitle.textContent = title;
            modalDescription.textContent = description;
            
            // Convert Google Drive URL to embed URL
            const embedUrl = getGoogleDriveEmbedUrl(videoUrl);
            
            // Create iframe for Google Drive embed
            videoPlayer.innerHTML = `
                <iframe src="${embedUrl}" 
                        frameborder="0" 
                        allow="autoplay; encrypted-media" 
                        allowfullscreen>
                </iframe>
            `;
            
            // Show modal with animation
            videoModal.style.display = 'flex';
            videoModal.style.opacity = '0';
            
            setTimeout(() => {
                videoModal.style.transition = 'opacity 0.3s';
                videoModal.style.opacity = '1';
            }, 10);
        }

        // Add CSS for shake animation
        const style = document.createElement('style');
        style.textContent = `
            @keyframes shake {
                0%, 100% { transform: translateX(0); }
                10%, 30%, 50%, 70%, 90% { transform: translateX(-5px); }
                20%, 40%, 60%, 80% { transform: translateX(5px); }
            }
        `;
        document.head.appendChild(style);

        // Instructions for setting up Google Drive videos
        function showSetupInstructions() {
            console.log(`
            ===========================================
            GOOGLE DRIVE SETUP INSTRUCTIONS:
            ===========================================
            
            1. Upload your videos to Google Drive
            2. For each video:
               - Right-click the file and select "Share"
               - Click "Change to anyone with the link"
               - Copy the shareable link
               
            3. Replace the videoUrl in the videoLessons object:
               - Change "YOUR_FILE_ID_1" to your actual file ID
               - Example: 
                 videoUrl: "https://drive.google.com/file/d/ABC123def456/view?usp=sharing"
                 
            4. For thumbnails, you can:
               - Use the same Google Drive file ID for automatic thumbnails
               - Upload custom thumbnails and use their URLs
               
            Note: Make sure your videos are in a supported format (MP4 recommended)
            ===========================================
            `);
        }

        // Show setup instructions when page loads
        window.addEventListener('load', showSetupInstructions);
    </script>
</body>
</html>
