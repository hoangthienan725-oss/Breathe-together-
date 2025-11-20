<!doctype html>
<html lang="en">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Breathing Together - Yoga &amp; Meditation</title>
  <script src="/_sdk/element_sdk.js"></script>
  <style>
        body {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Inter', -webkit-system-font, system-ui, sans-serif;
            background: linear-gradient(135deg, #fef5e7 0%, #e8f4f8 50%, #f3e5f5 100%);
            color: #4a5568;
            line-height: 1.6;
            min-height: 100%;
            position: relative;
            overflow-x: hidden;
        }

        html {
            height: 100%;
        }

        /* Floating Particles */
        .particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }

        .particle {
            position: absolute;
            border-radius: 50%;
            animation: float 20s infinite ease-in-out;
        }

        .particle:nth-child(1) {
            width: 60px;
            height: 60px;
            left: 10%;
            background: radial-gradient(circle, rgba(255, 183, 77, 0.3), transparent);
            animation-delay: 0s;
            animation-duration: 25s;
        }

        .particle:nth-child(2) {
            width: 40px;
            height: 40px;
            left: 25%;
            background: radial-gradient(circle, rgba(135, 206, 235, 0.4), transparent);
            animation-delay: 3s;
            animation-duration: 22s;
        }

        .particle:nth-child(3) {
            width: 80px;
            height: 80px;
            left: 50%;
            background: radial-gradient(circle, rgba(183, 148, 244, 0.3), transparent);
            animation-delay: 6s;
            animation-duration: 28s;
        }

        .particle:nth-child(4) {
            width: 50px;
            height: 50px;
            left: 70%;
            background: radial-gradient(circle, rgba(129, 230, 217, 0.4), transparent);
            animation-delay: 2s;
            animation-duration: 24s;
        }

        .particle:nth-child(5) {
            width: 35px;
            height: 35px;
            left: 85%;
            background: radial-gradient(circle, rgba(255, 183, 77, 0.35), transparent);
            animation-delay: 5s;
            animation-duration: 26s;
        }

        .particle:nth-child(6) {
            width: 45px;
            height: 45px;
            left: 40%;
            background: radial-gradient(circle, rgba(135, 206, 235, 0.35), transparent);
            animation-delay: 8s;
            animation-duration: 23s;
        }

        @keyframes float {
            0%, 100% {
                transform: translateY(100%) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 0.6;
            }
            50% {
                transform: translateY(-50%) rotate(180deg);
                opacity: 0.8;
            }
            90% {
                opacity: 0.6;
            }
        }

        /* Breathing Circle Animation */
        .breathing-circle {
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 150px;
            height: 150px;
            pointer-events: none;
            z-index: 0;
            opacity: 0.1;
        }

        .breathing-circle::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border-radius: 50%;
            background: radial-gradient(circle, rgba(183, 148, 244, 0.4), transparent 70%);
            animation: breathe 8s infinite ease-in-out;
        }

        @keyframes breathe {
            0%, 100% {
                transform: scale(1);
                opacity: 0.3;
            }
            50% {
                transform: scale(2.5);
                opacity: 0.1;
            }
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            position: relative;
            z-index: 2;
        }

        /* Header */
        .header {
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(10px);
            padding: 20px 0;
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.05);
            position: relative;
            z-index: 10;
            animation: fadeInDown 1s ease-out;
            border-bottom: 2px solid transparent;
            border-image: linear-gradient(90deg, #ffb74d, #87ceeb, #b794f4, #81e6d9);
            border-image-slice: 1;
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .logo-icon {
            width: 40px;
            height: 40px;
            background: linear-gradient(135deg, #81e6d9, #4a90e2);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 20px;
            animation: pulse 3s infinite ease-in-out;
        }

        @keyframes pulse {
            0%, 100% {
                transform: scale(1);
                box-shadow: 0 0 0 0 rgba(129, 230, 217, 0.7);
            }
            50% {
                transform: scale(1.05);
                box-shadow: 0 0 0 10px rgba(129, 230, 217, 0);
            }
        }

        .logo h1 {
            margin: 0;
            font-size: 24px;
            font-weight: 600;
            background: linear-gradient(135deg, #4a90e2, #b794f4);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .tagline {
            font-size: 14px;
            color: #718096;
            margin: 0;
        }

        .nav-links {
            display: flex;
            gap: 30px;
            list-style: none;
            margin: 0;
            padding: 0;
        }

        .nav-links a {
            text-decoration: none;
            color: #4a5568;
            font-weight: 500;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: linear-gradient(90deg, #ffb74d, #87ceeb);
            transition: width 0.3s ease;
        }

        .nav-links a:hover {
            color: #4a90e2;
            transform: translateY(-2px);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        /* Main Content */
        .main {
            padding: 60px 0;
        }

        .hero {
            text-align: center;
            margin-bottom: 80px;
            animation: fadeInUp 1.2s ease-out;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(40px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero h2 {
            font-size: 48px;
            font-weight: 300;
            background: linear-gradient(135deg, #4a90e2, #b794f4, #ffb74d);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin: 0 0 20px 0;
            line-height: 1.2;
            animation: textGlow 4s ease-in-out infinite;
        }

        @keyframes textGlow {
            0%, 100% {
                filter: drop-shadow(0 0 10px rgba(183, 148, 244, 0.3));
            }
            50% {
                filter: drop-shadow(0 0 20px rgba(183, 148, 244, 0.6));
            }
        }

        .hero p {
            font-size: 20px;
            color: #718096;
            max-width: 600px;
            margin: 0 auto;
        }

        /* Video Section */
        .video-section {
            background: linear-gradient(135deg, rgba(255, 255, 255, 0.9), rgba(240, 248, 255, 0.7));
            border-radius: 20px;
            padding: 50px;
            margin-bottom: 80px;
            text-align: center;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.05);
            animation: fadeInUp 1.4s ease-out;
            transition: all 0.5s ease;
            border: 2px solid transparent;
            background-clip: padding-box;
            position: relative;
        }

        .video-section::before {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(135deg, #ffb74d, #87ceeb, #b794f4);
            border-radius: 20px;
            z-index: -1;
            opacity: 0;
            transition: opacity 0.5s ease;
        }

        .video-section:hover::before {
            opacity: 0.3;
        }

        .video-section:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.1);
        }

        .video-section h3 {
            font-size: 32px;
            font-weight: 400;
            background: linear-gradient(135deg, #4a90e2, #b794f4);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin: 0 0 20px 0;
        }

        .video-section p {
            font-size: 18px;
            color: #718096;
            margin-bottom: 40px;
            max-width: 500px;
            margin-left: auto;
            margin-right: auto;
        }

        .video-embed {
            background: linear-gradient(135deg, #f7fafc, #fef5e7);
            border: 2px dashed #cbd5e0;
            border-radius: 15px;
            padding: 60px 40px;
            margin: 30px 0;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .video-embed::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(183, 148, 244, 0.1), transparent 50%);
            animation: rotate 20s linear infinite;
        }

        @keyframes rotate {
            from {
                transform: rotate(0deg);
            }
            to {
                transform: rotate(360deg);
            }
        }

        .video-embed:hover {
            border-color: #b794f4;
            background: linear-gradient(135deg, #edf2f7, #fff8e1);
        }

        .video-placeholder {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 20px;
            position: relative;
            z-index: 1;
        }

        .video-icon {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, #81e6d9, #4a90e2);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 36px;
            animation: pulseVideo 2s infinite ease-in-out;
        }

        @keyframes pulseVideo {
            0%, 100% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.1);
            }
        }

        .video-placeholder h4 {
            font-size: 24px;
            color: #4a5568;
            margin: 0;
            font-weight: 500;
        }

        .video-placeholder p {
            color: #718096;
            margin: 0;
            font-size: 16px;
        }

        .embed-instructions {
            background: linear-gradient(135deg, #e6fffa, #fff8e1);
            border: 1px solid #81e6d9;
            border-radius: 10px;
            padding: 20px;
            margin-top: 20px;
            text-align: left;
            position: relative;
            z-index: 1;
        }

        .embed-instructions h5 {
            color: #234e52;
            margin: 0 0 10px 0;
            font-size: 16px;
            font-weight: 600;
        }

        .embed-instructions p {
            color: #285e61;
            margin: 0;
            font-size: 14px;
            line-height: 1.5;
        }

        /* Features Grid */
        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
            margin-bottom: 60px;
        }

        .features h3 {
            text-align: center;
            font-size: 32px;
            font-weight: 400;
            background: linear-gradient(135deg, #4a90e2, #b794f4, #ffb74d);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin: 0 0 50px 0;
            grid-column: 1 / -1;
            animation: fadeInUp 1.6s ease-out;
        }

        .feature-card {
            background: linear-gradient(135deg, rgba(255, 255, 255, 0.9), rgba(248, 249, 250, 0.8));
            border-radius: 15px;
            padding: 40px 30px;
            text-align: center;
            transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1);
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.05);
            animation: fadeInUp 1.8s ease-out;
            border: 2px solid transparent;
            position: relative;
        }

        .feature-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            border-radius: 15px;
            padding: 2px;
                background: linear-gradient(135deg, #ffb74d, #87ceeb, #b794f4);
                /* Use explicit mask properties for better cross-browser support
                    and to avoid @warnings from the shorthand syntax. This creates
                    an inner cutout (content-box) so the gradient appears as a frame. */
                -webkit-mask-image: linear-gradient(#fff 0 0), linear-gradient(#fff 0 0);
                -webkit-mask-clip: content-box, border-box;
                -webkit-mask-repeat: no-repeat;
                -webkit-mask-composite: xor;
                mask-image: linear-gradient(#fff 0 0), linear-gradient(#fff 0 0);
                mask-clip: content-box, border-box;
                mask-repeat: no-repeat;
                mask-composite: exclude;
            opacity: 0;
            transition: opacity 0.5s ease;
        }

        .feature-card:hover::before {
            opacity: 1;
        }

        .feature-card:nth-child(2) {
            animation-delay: 0.1s;
        }

        .feature-card:nth-child(3) {
            animation-delay: 0.2s;
        }

        .feature-card:nth-child(4) {
            animation-delay: 0.3s;
        }

        .feature-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.15);
        }

        .feature-icon {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px auto;
            color: white;
            font-size: 24px;
            transition: all 0.4s ease;
        }

        .feature-card:nth-child(2) .feature-icon {
            background: linear-gradient(135deg, #ffb74d, #ff9800);
        }

        .feature-card:nth-child(3) .feature-icon {
            background: linear-gradient(135deg, #87ceeb, #4a90e2);
        }

        .feature-card:nth-child(4) .feature-icon {
            background: linear-gradient(135deg, #81e6d9, #38b2ac);
        }

        .feature-card:hover .feature-icon {
            transform: rotate(360deg) scale(1.2);
            box-shadow: 0 10px 30px rgba(74, 144, 226, 0.4);
        }

        .feature-card h4 {
            font-size: 20px;
            color: #2d3748;
            margin: 0 0 15px 0;
            font-weight: 500;
        }

        .feature-card p {
            color: #718096;
            margin: 0;
            font-size: 16px;
        }

        /* Quote Pop-up */
        .quote-popup {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: linear-gradient(135deg, rgba(255, 255, 255, 0.95), rgba(243, 229, 245, 0.95));
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 30px;
            max-width: 400px;
            box-shadow: 0 20px 60px rgba(183, 148, 244, 0.3);
            z-index: 1000;
            opacity: 0;
            transform: translateY(100px) scale(0.8);
            transition: all 0.6s cubic-bezier(0.34, 1.56, 0.64, 1);
            pointer-events: none;
            border: 2px solid rgba(183, 148, 244, 0.2);
        }

        .quote-popup.show {
            opacity: 1;
            transform: translateY(0) scale(1);
            pointer-events: all;
        }

        .quote-popup.hide {
            animation: slideOut 0.5s ease-out forwards;
        }

        @keyframes slideOut {
            to {
                opacity: 0;
                transform: translateY(100px) scale(0.8);
            }
        }

        .quote-header {
            display: flex;
            align-items: center;
            gap: 15px;
            margin-bottom: 20px;
        }

        .quote-icon {
            width: 50px;
            height: 50px;
            background: linear-gradient(135deg, #b794f4, #9f7aea);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            animation: pulse 2s infinite ease-in-out;
        }

        .quote-label {
            font-size: 14px;
            color: #805ad5;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .quote-text {
            font-size: 18px;
            color: #2d3748;
            line-height: 1.6;
            margin: 0 0 15px 0;
            font-style: italic;
            font-weight: 400;
        }

        .quote-author {
            font-size: 14px;
            color: #718096;
            text-align: right;
            margin: 0 0 20px 0;
            font-weight: 500;
        }

        .quote-actions {
            display: flex;
            gap: 10px;
            justify-content: space-between;
        }

        .quote-btn {
            flex: 1;
            padding: 10px 20px;
            border: none;
            border-radius: 10px;
            font-size: 14px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .quote-btn-next {
            background: linear-gradient(135deg, #b794f4, #9f7aea);
            color: white;
        }

        .quote-btn-next:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(128, 90, 213, 0.4);
        }

        .quote-btn-close {
            background: rgba(226, 232, 240, 0.8);
            color: #4a5568;
        }

        .quote-btn-close:hover {
            background: rgba(203, 213, 224, 0.9);
        }

        .quote-trigger {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, #b794f4, #9f7aea);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 28px;
            cursor: pointer;
            box-shadow: 0 10px 30px rgba(128, 90, 213, 0.4);
            z-index: 999;
            transition: all 0.3s ease;
            animation: float-button 3s ease-in-out infinite;
        }

        @keyframes float-button {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-10px);
            }
        }

        .quote-trigger:hover {
            transform: scale(1.1);
            box-shadow: 0 15px 40px rgba(128, 90, 213, 0.6);
        }

        .quote-trigger.hidden {
            display: none;
        }

        /* Zen Waves */
        .zen-waves {
            position: fixed;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 200px;
            pointer-events: none;
            z-index: 0;
            opacity: 0.15;
        }

        .wave {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 200%;
            height: 100%;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none"><path d="M0,0V46.29c47.79,22.2,103.59,32.17,158,28,70.36-5.37,136.33-33.31,206.8-37.5C438.64,32.43,512.34,53.67,583,72.05c69.27,18,138.3,24.88,209.4,13.08,36.15-6,69.85-17.84,104.45-29.34C989.49,25,1113-14.29,1200,52.47V0Z" opacity=".25" fill="%2381e6d9"/><path d="M0,0V15.81C13,36.92,27.64,56.86,47.69,72.05,99.41,111.27,165,111,224.58,91.58c31.15-10.15,60.09-26.07,89.67-39.8,40.92-19,84.73-46,130.83-49.67,36.26-2.85,70.9,9.42,98.6,31.56,31.77,25.39,62.32,62,103.63,73,40.44,10.79,81.35-6.69,119.13-24.28s75.16-39,116.92-43.05c59.73-5.85,113.28,22.88,168.9,38.84,30.2,8.66,59,6.17,87.09-7.5,22.43-10.89,48-26.93,60.65-49.24V0Z" opacity=".5" fill="%2381e6d9"/><path d="M0,0V5.63C149.93,59,314.09,71.32,475.83,42.57c43-7.64,84.23-20.12,127.61-26.46,59-8.63,112.48,12.24,165.56,35.4C827.93,77.22,886,95.24,951.2,90c86.53-7,172.46-45.71,248.8-84.81V0Z" fill="%2381e6d9"/></svg>') repeat-x;
            background-size: 1200px 120px;
            animation: wave 25s cubic-bezier(0.36, 0.45, 0.63, 0.53) infinite;
        }

        .wave:nth-child(2) {
            animation: wave 20s cubic-bezier(0.36, 0.45, 0.63, 0.53) -.125s infinite, swell 7s ease -1.25s infinite;
            opacity: 0.8;
        }

        .wave:nth-child(3) {
            animation: wave 15s cubic-bezier(0.36, 0.45, 0.63, 0.53) -.125s infinite, swell 7s ease -1.25s infinite;
            opacity: 0.5;
        }

        @keyframes wave {
            0% {
                transform: translateX(0);
            }
            50% {
                transform: translateX(-25%);
            }
            100% {
                transform: translateX(-50%);
            }
        }

        @keyframes swell {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-15px);
            }
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .nav {
                flex-direction: column;
                gap: 20px;
            }

            .nav-links {
                gap: 20px;
            }

            .hero h2 {
                font-size: 36px;
            }

            .hero p {
                font-size: 18px;
            }

            .video-section {
                padding: 30px 20px;
            }

            .video-embed {
                padding: 40px 20px;
            }

            .features {
                grid-template-columns: 1fr;
                gap: 30px;
            }

            .feature-card {
                padding: 30px 20px;
            }

            .particle {
                display: none;
            }

            .quote-popup {
                bottom: 20px;
                right: 20px;
                left: 20px;
                max-width: none;
                padding: 25px;
            }

            .quote-trigger {
                bottom: 20px;
                right: 20px;
                width: 50px;
                height: 50px;
                font-size: 24px;
            }
        }
    </style>
  <style>@view-transition { navigation: auto; }</style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
  <script src="https://cdn.tailwindcss.com" type="text/javascript"></script>
 </head>
 <body><!-- Floating Particles -->
  <div class="particles">
   <div class="particle"></div>
   <div class="particle"></div>
   <div class="particle"></div>
   <div class="particle"></div>
   <div class="particle"></div>
   <div class="particle"></div>
  </div><!-- Breathing Circle -->
  <div class="breathing-circle"></div><!-- Zen Waves -->
  <div class="zen-waves">
   <div class="wave"></div>
   <div class="wave"></div>
   <div class="wave"></div>
  </div><!-- Quote Trigger Button -->
  <div class="quote-trigger" id="quoteTrigger">
   💭
  </div><!-- Quote Pop-up -->
  <div class="quote-popup" id="quotePopup">
   <div class="quote-header">
    <div class="quote-icon">
     ✨
    </div>
    <div class="quote-label">
     Moment of Calm
    </div>
   </div>
   <p class="quote-text" id="quoteText"></p>
   <p class="quote-author" id="quoteAuthor"></p>
   <div class="quote-actions"><button class="quote-btn quote-btn-next" id="nextQuote">Next Quote</button> <button class="quote-btn quote-btn-close" id="closeQuote">Close</button>
   </div>
  </div>
  <header class="header">
   <nav class="container">
    <div class="nav">
     <div class="logo">
      <div class="logo-icon">
       🧘
      </div>
      <div>
       <h1 id="site-title">Breathing Together</h1>
       <p class="tagline" id="tagline">Find your inner peace</p>
      </div>
     </div>
     <ul class="nav-links">
      <li><a href="#home">🏠 Home</a></li>
      <li><a href="#videos">📹 Videos</a></li>
      <li><a href="#practice">🧘 Practice</a></li>
      <li><a href="#about">ℹ️ About</a></li>
     </ul>
    </div>
   </nav>
  </header>
  <main class="main">
   <div class="container">
    <section class="hero" id="home">
     <h2 id="welcome-title">Welcome to Your Journey</h2>
     <p id="welcome-text">Discover the transformative power of yoga and meditation in a peaceful, supportive environment designed for your well-being.</p>
    </section>
    <section class="video-section" id="videos">
     <h3 id="video-section-title">Guided Sessions</h3>
     <p id="video-description">Immerse yourself in our carefully curated video content designed to guide you through your practice.</p>
     <div class="video-embed">
      <div class="video-placeholder">
       <div class="video-icon">
        ▶️
       </div>
       <h4>Video Embed Area
       <iframe width="560" height="315" src="https://www.youtube.com/embed/jPff5Yj-T_I?si=MKXy_v7Q1PCyNOWa" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe> 
       </h4>
       <p>This space is ready for your yoga and meditation videos</p>
      </div>
      <div class="embed-instructions">
       <h5>How to embed your videos:</h5>
       <p>You can easily replace this placeholder with your video content by pasting YouTube, Vimeo, or other video embed codes directly into this section. The responsive design will automatically adjust to fit your content beautifully.</p>
      </div>
     </div>
    </section>
    <section class="features">
     <h3 id="features-title">Why Choose Breathing Together</h3>
     <div class="feature-card">
      <div class="feature-icon">
       🌱
      </div>
      <h4>Mindful Practice</h4>
      <p>Cultivate awareness and presence through guided meditation and gentle yoga flows designed for all levels.</p>
     </div>
     <div class="feature-card">
      <div class="feature-icon">
       🎯
      </div>
      <h4>Focused Sessions</h4>
      <p>Structured programs that help you build consistency and deepen your practice over time.</p>
     </div>
     <div class="feature-card">
      <div class="feature-icon">
       🤝
      </div>
      <h4>Community Support</h4>
      <p>Join a welcoming community of practitioners on the same journey toward inner peace and wellness.</p>
     </div>
    </section>
   </div>
  </main>
  <script>
        const quotes = [
            {
                text: "The mind is everything. What you think you become.",
                author: "Buddha"
            },
            {
                text: "Peace comes from within. Do not seek it without.",
                author: "Buddha"
            },
            {
                text: "The present moment is filled with joy and happiness. If you are attentive, you will see it.",
                author: "Thich Nhat Hanh"
            },
            {
                text: "Meditation is not evasion; it is a serene encounter with reality.",
                author: "Thich Nhat Hanh"
            },
            {
                text: "The goal of meditation isn't to control your thoughts, it's to stop letting them control you.",
                author: "Unknown"
            },
            {
                text: "In the midst of movement and chaos, keep stillness inside of you.",
                author: "Deepak Chopra"
            },
            {
                text: "Quiet the mind and the soul will speak.",
                author: "Ma Jaya Sati Bhagavati"
            },
            {
                text: "Do not dwell in the past, do not dream of the future, concentrate the mind on the present moment.",
                author: "Buddha"
            },
            {
                text: "The soul always knows what to do to heal itself. The challenge is to silence the mind.",
                author: "Caroline Myss"
            },
            {
                text: "Feelings come and go like clouds in a windy sky. Conscious breathing is my anchor.",
                author: "Thich Nhat Hanh"
            },
            {
                text: "Wherever you are, be there totally.",
                author: "Eckhart Tolle"
            },
            {
                text: "The quieter you become, the more you can hear.",
                author: "Ram Dass"
            }
        ];

        let currentQuoteIndex = 0;

        const defaultConfig = {
            site_title: "Breathing Together",
            tagline: "Find your inner peace",
            welcome_title: "Welcome to Your Journey",
            welcome_text: "Discover the transformative power of yoga and meditation in a peaceful, supportive environment designed for your well-being.",
            video_section_title: "Guided Sessions",
            video_description: "Immerse yourself in our carefully curated video content designed to guide you through your practice.",
            features_title: "Why Choose Breathing Together",
            background_color: "#fef5e7",
            surface_color: "#ffffff",
            text_color: "#4a5568",
            primary_color: "#4a90e2",
            accent_color: "#b794f4",
            font_family: "Inter",
            font_size: 16
        };

        async function onConfigChange(config) {
            // Update text content
            document.getElementById('site-title').textContent = config.site_title || defaultConfig.site_title;
            document.getElementById('tagline').textContent = config.tagline || defaultConfig.tagline;
            document.getElementById('welcome-title').textContent = config.welcome_title || defaultConfig.welcome_title;
            document.getElementById('welcome-text').textContent = config.welcome_text || defaultConfig.welcome_text;
            document.getElementById('video-section-title').textContent = config.video_section_title || defaultConfig.video_section_title;
            document.getElementById('video-description').textContent = config.video_description || defaultConfig.video_description;
            document.getElementById('features-title').textContent = config.features_title || defaultConfig.features_title;

            // Update colors
            const backgroundColor = config.background_color || defaultConfig.background_color;
            const surfaceColor = config.surface_color || defaultConfig.surface_color;
            const textColor = config.text_color || defaultConfig.text_color;
            const primaryColor = config.primary_color || defaultConfig.primary_color;
            const accentColor = config.accent_color || defaultConfig.accent_color;

            document.body.style.background = `linear-gradient(135deg, ${backgroundColor} 0%, #e8f4f8 50%, #f3e5f5 100%)`;
            
            // Update text colors
            const headings = document.querySelectorAll('h1, h2, h3, h4');
            headings.forEach(heading => {
                heading.style.color = textColor;
            });

            // Update primary color elements
            const logoIcon = document.querySelector('.logo-icon');
            if (logoIcon) logoIcon.style.background = `linear-gradient(135deg, #81e6d9, ${primaryColor})`;

            const videoIcon = document.querySelector('.video-icon');
            if (videoIcon) videoIcon.style.background = `linear-gradient(135deg, #81e6d9, ${primaryColor})`;

            // Update font
            const fontFamily = config.font_family || defaultConfig.font_family;
            document.body.style.fontFamily = `${fontFamily}, -webkit-system-font, system-ui, sans-serif`;

            // Update font sizes
            const baseFontSize = config.font_size || defaultConfig.font_size;
            document.body.style.fontSize = `${baseFontSize}px`;

            const h1Elements = document.querySelectorAll('h1');
            h1Elements.forEach(el => el.style.fontSize = `${baseFontSize * 1.5}px`);

            const h2Elements = document.querySelectorAll('h2');
            h2Elements.forEach(el => el.style.fontSize = `${baseFontSize * 3}px`);

            const h3Elements = document.querySelectorAll('h3');
            h3Elements.forEach(el => el.style.fontSize = `${baseFontSize * 2}px`);

            const h4Elements = document.querySelectorAll('h4');
            h4Elements.forEach(el => el.style.fontSize = `${baseFontSize * 1.5}px`);

            const pElements = document.querySelectorAll('p');
            pElements.forEach(el => {
                if (el.classList.contains('tagline')) {
                    el.style.fontSize = `${baseFontSize * 0.875}px`;
                } else if (el.closest('.hero')) {
                    el.style.fontSize = `${baseFontSize * 1.25}px`;
                } else if (el.closest('.video-section')) {
                    el.style.fontSize = `${baseFontSize * 1.125}px`;
                } else if (el.classList.contains('quote-text')) {
                    el.style.fontSize = `${baseFontSize * 1.125}px`;
                } else {
                    el.style.fontSize = `${baseFontSize}px`;
                }
            });
        }

        function mapToCapabilities(config) {
            return {
                recolorables: [
                    {
                        get: () => config.background_color || defaultConfig.background_color,
                        set: (value) => {
                            if (window.elementSdk) {
                                window.elementSdk.setConfig({ background_color: value });
                            }
                        }
                    },
                    {
                        get: () => config.surface_color || defaultConfig.surface_color,
                        set: (value) => {
                            if (window.elementSdk) {
                                window.elementSdk.setConfig({ surface_color: value });
                            }
                        }
                    },
                    {
                        get: () => config.text_color || defaultConfig.text_color,
                        set: (value) => {
                            if (window.elementSdk) {
                                window.elementSdk.setConfig({ text_color: value });
                            }
                        }
                    },
                    {
                        get: () => config.primary_color || defaultConfig.primary_color,
                        set: (value) => {
                            if (window.elementSdk) {
                                window.elementSdk.setConfig({ primary_color: value });
                            }
                        }
                    },
                    {
                        get: () => config.accent_color || defaultConfig.accent_color,
                        set: (value) => {
                            if (window.elementSdk) {
                                window.elementSdk.setConfig({ accent_color: value });
                            }
                        }
                    }
                ],
                borderables: [],
                fontEditable: {
                    get: () => config.font_family || defaultConfig.font_family,
                    set: (value) => {
                        if (window.elementSdk) {
                            window.elementSdk.setConfig({ font_family: value });
                        }
                    }
                },
                fontSizeable: {
                    get: () => config.font_size || defaultConfig.font_size,
                    set: (value) => {
                        if (window.elementSdk) {
                            window.elementSdk.setConfig({ font_size: value });
                        }
                    }
                }
            };
        }

        function mapToEditPanelValues(config) {
            return new Map([
                ["site_title", config.site_title || defaultConfig.site_title],
                ["tagline", config.tagline || defaultConfig.tagline],
                ["welcome_title", config.welcome_title || defaultConfig.welcome_title],
                ["welcome_text", config.welcome_text || defaultConfig.welcome_text],
                ["video_section_title", config.video_section_title || defaultConfig.video_section_title],
                ["video_description", config.video_description || defaultConfig.video_description],
                ["features_title", config.features_title || defaultConfig.features_title]
            ]);
        }

        // Initialize the Element SDK
        if (window.elementSdk) {
            window.elementSdk.init({
                defaultConfig,
                onConfigChange,
                mapToCapabilities,
                mapToEditPanelValues
            });
        }

        // Quote functionality
        function showQuote(index) {
            const quote = quotes[index];
            if (!quote) return;
            const textEl = document.getElementById('quoteText');
            const authorEl = document.getElementById('quoteAuthor');
            if (textEl) textEl.textContent = quote.text || '';
            if (authorEl) authorEl.textContent = quote.author ? '— ' + quote.author : '';

            const popup = document.getElementById('quotePopup');
            const trigger = document.getElementById('quoteTrigger');

            if (popup) {
                popup.classList.remove('hide');
                popup.classList.add('show');
            }
            if (trigger) trigger.classList.add('hidden');
        }

        function hideQuote() {
            const popup = document.getElementById('quotePopup');
            const trigger = document.getElementById('quoteTrigger');
            
            popup.classList.remove('show');
            popup.classList.add('hide');
            
            setTimeout(() => {
                popup.classList.remove('hide');
                trigger.classList.remove('hidden');
            }, 500);
        }

        function nextQuote() {
            currentQuoteIndex = (currentQuoteIndex + 1) % quotes.length;
            showQuote(currentQuoteIndex);
        }

        // Event listeners
        document.getElementById('quoteTrigger').addEventListener('click', () => {
            showQuote(currentQuoteIndex);
        });

        document.getElementById('nextQuote').addEventListener('click', nextQuote);
        document.getElementById('closeQuote').addEventListener('click', hideQuote);

        // Show first quote after 5 seconds
        setTimeout(() => {
            showQuote(0);
        }, 5000);

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });
    </script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9a178a75a319558c',t:'MTc2MzYzNzQ0Ni4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
