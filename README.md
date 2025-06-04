<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>SafeHaulX - Smart Trucking Support</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        header {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.2);
            padding: 2rem 0;
            text-align: center;
            color: white;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        header h1 {
            font-size: 3rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }

        .subtitle {
            font-size: 1.2rem;
            opacity: 0.9;
            font-weight: 300;
        }

        main {
            padding: 3rem 0;
        }

        section {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            margin: 2rem 0;
            padding: 2.5rem;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.3);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        section:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        }

        h2 {
            color: #4a5568;
            font-size: 2rem;
            margin-bottom: 1.5rem;
            position: relative;
            padding-left: 1rem;
        }

        h2::before {
            content: '';
            position: absolute;
            left: 0;
            top: 50%;
            transform: translateY(-50%);
            width: 4px;
            height: 2rem;
            background: linear-gradient(135deg, #667eea, #764ba2);
            border-radius: 2px;
        }

        p {
            margin-bottom: 1rem;
            color: #2d3748;
            font-size: 1.1rem;
        }

        ul {
            list-style: none;
            padding-left: 0;
        }

        li {
            margin: 1rem 0;
            padding: 1rem;
            background: rgba(102, 126, 234, 0.05);
            border-radius: 10px;
            border-left: 4px solid #667eea;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        li::before {
            content: '→';
            position: absolute;
            left: 15px;
            color: #667eea;
            font-weight: bold;
            opacity: 0;
            transform: translateX(-10px);
            transition: all 0.3s ease;
        }

        li:hover {
            background: rgba(102, 126, 234, 0.1);
            transform: translateX(10px);
            padding-left: 2rem;
        }

        li:hover::before {
            opacity: 1;
            transform: translateX(0);
        }

        .features li {
            padding-left: 2rem;
        }

        .features li::before {
            content: '✓';
            position: absolute;
            left: 15px;
            color: #48bb78;
            font-weight: bold;
            opacity: 1;
            transform: translateX(0);
        }

        .coming-soon {
            background: linear-gradient(135deg, #ffeaa7, #fab1a0);
            color: #2d3748;
            padding: 0.3rem 0.8rem;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
            margin-left: 0.5rem;
        }

        a {
            color: #667eea;
            text-decoration: none;
            font-weight: 600;
            transition: color 0.3s ease;
        }

        a:hover {
            color: #764ba2;
            text-decoration: underline;
        }

        .contact-item {
            display: flex;
            align-items: center;
            margin: 1rem 0;
            padding: 1rem;
            background: rgba(72, 187, 120, 0.05);
            border-radius: 10px;
            border-left: 4px solid #48bb78;
        }

        .contact-item strong {
            min-width: 80px;
            color: #2d3748;
        }

        footer {
            background: rgba(0, 0, 0, 0.8);
            color: white;
            text-align: center;
            padding: 2rem 0;
            margin-top: 3rem;
        }

        .intro p {
            font-size: 1.2rem;
            color: #4a5568;
            line-height: 1.8;
        }

        .privacy-policy ul li {
            background: rgba(237, 137, 54, 0.05);
            border-left-color: #ed8936;
        }

        .privacy-policy ul li:hover {
            background: rgba(237, 137, 54, 0.1);
        }

        @media (max-width: 768px) {
            header h1 {
                font-size: 2rem;
            }
            
            section {
                margin: 1rem 0;
                padding: 1.5rem;
            }
            
            h2 {
                font-size: 1.5rem;
            }
            
            .container {
                padding: 0 15px;
            }
        }

        /* Subtle animations */
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }

        section:nth-child(even) {
            animation: float 6s ease-in-out infinite;
            animation-delay: 0.5s;
        }

        section:nth-child(odd) {
            animation: float 6s ease-in-out infinite;
            animation-delay: 1s;
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>SafeHaulX</h1>
            <p class="subtitle">Smart Trucking Support</p>
        </div>
    </header>
    
    <main>
        <div class="container">
            <section class="intro">
                <h2>About SafeHaulX</h2>
                <p>
                    SafeHaulX is a smart trucking app designed to support drivers on the road with real-time weather updates, and an interactive 3D trucking interface—all in one easy-to-use platform.
                </p>
            </section>

            <section class="features">
                <h2>Features</h2>
                <ul>
                    <li>Stay informed on weather changes instantly</li>
                    <li>Hands free voice control for safer navigation <span class="coming-soon">Coming soon</span></li>
                    <li>Interactive and engaging user experience</li>
                    <li>Optimized for speed and stability</li>
                </ul>
            </section>

            <section class="support">
                <h2>Support & Feedback</h2>
                <p>We're here to help! If you experience any issues or have suggestions, reach out to us through:</p>
                <div class="contact-item">
                    <strong>Email:</strong> 
                    <a href="mailto:alsharafiyousef8@gmail.com">alsharafiyousef8@gmail.com</a>
                </div>
                <div class="contact-item">
                    <strong>Phone:</strong> 
                    <a href="tel:7213456723">721-345-6723</a>
                </div>
            </section>

            <section class="privacy-policy">
                <h2>Privacy Policy</h2>
                <p><strong>Effective Date:</strong> June 4, 2025</p>
                <p>SafeHaulX values your privacy. This policy explains what information we collect and how we use it:</p>
                <ul>
                    <li><strong>Location Data:</strong> We collect your real-time GPS location to support map and routing features.</li>
                    <li><strong>User Input:</strong> Truck details, search queries, and settings are stored locally for convenience.</li>
                    <li><strong>Device Info:</strong> Anonymous usage and crash data may be collected to improve app performance.</li>
                    <li><strong>Data Sharing:</strong> We do not sell or share your data with third parties.</li>
                    <li><strong>Security:</strong> We apply best practices to protect your information, but no method is fully secure.</li>
                    <li><strong>Children:</strong> The app is not intended for users under 13.</li>
                    <li><strong>Choices:</strong> You may revoke location access or request data deletion by contacting us.</li>
                </ul>
                <p>For questions or to request data deletion, email us at <a href="mailto:alsharafiyousef8@gmail.com">alsharafiyousef8@gmail.com</a>.</p>
            </section>
        </div>
    </main>

    <footer>
        <div class="container">
            <p>&copy; 2025 SafeHaulX. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
