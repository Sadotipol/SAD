<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Minecraft Server</title>
    <!-- Favicon -->
    <link rel="icon" href="favicon.ico" type="image/x-icon">
    <!-- Alternate Favicon (PNG) -->
    <link rel="icon" href="favicom.png" type="image/png">
    <style>
        /* General Styles */
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            background: #000000; /* Pure black background for high contrast */
            color: #ffffff; /* White text for readability */
            text-align: center;
            height: 100vh;
        }
    
        header {
            background: linear-gradient(90deg, #008000, #00ff00); /* Dark green to bright green gradient */
            padding: 20px 10px;
        }
    
        header h1 {
            color: #ffffff;
            font-size: 3em;
            text-shadow: 2px 2px 6px rgba(0, 0, 0, 0.5);
            margin: 0;
        }

        /* Social Media Buttons */
        .social-buttons {
            text-align: center;
            margin: 20px auto;
        }

        .social-buttons a {
            display: inline-block;
            margin: 0 10px;
            padding: 12px 20px;
            font-size: 16px;
            font-weight: bold;
            color: white;
            text-decoration: none;
            border-radius: 50px;
            transition: transform 0.3s, background-color 0.3s;
        }

        .social-buttons a:hover {
            transform: scale(1.1);
        }

        .youtube { background-color: #FF0000; }
        .youtube:hover { background-color: #CC0000; }
        .instagram { background-color: #E1306C; }
        .instagram:hover { background-color: #C2185B; }
        .telegram { background-color: #0088CC; }
        .telegram:hover { background-color: #006699; }
        .tiktok { background-color: #000000; }
        .tiktok:hover { background-color: #1C1C1C; }
    
        .container {
            padding: 20px;
            margin: 0 auto;
            max-width: 1200px;
        }
    
        /* Cards */
        .server-info, .player-stats, .news, .shop-info {
            margin: 20px auto;
            background: #121212; /* Soft black for contrast */
            border-radius: 15px;
            padding: 20px;
            max-width: 700px;
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.5);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
    
        .server-info:hover, .player-stats:hover, .news:hover, .shop-info:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 20px rgba(0, 255, 0, 0.3); /* Green glow on hover */
        }
    
        .server-info h2, .player-stats h2, .news h2, .shop-info h2 {
            color: #00ff00; /* Bright green for headers */
            font-size: 2em;
            margin-bottom: 10px;
        }
    
        .ip {
            font-size: 1.5em;
            font-weight: bold;
            color: #00ff00; /* Bright green for emphasis */
            margin-bottom: 10px;
        }
    
        .port {
            font-size: 1.2em;
            font-weight: bold;
            color: #32cd32; /* Medium green for port */
        }
    
        .status {
            color: #32cd32; /* Medium green for online status */
            font-weight: bold;
        }
    
        /* Buttons and Links */
        .button, .link {
            background: #00ff00; /* Bright green background for buttons */
            color: #000000; /* Black text for contrast on buttons */
            text-decoration: none;
            padding: 12px 24px;
            border-radius: 8px;
            font-size: 1.2em;
            display: inline-block;
            margin: 10px;
            transition: background-color 0.3s ease, transform 0.2s ease, box-shadow 0.3s ease;
        }
    
        .button:hover, .link:hover {
            background: #008000; /* Dark green hover effect */
            transform: translateY(-3px);
            box-shadow: 0 4px 10px rgba(0, 255, 0, 0.4); /* Glow effect on hover */
        }

        /* Cube Container */
        .cube-container {
            perspective: 1000px;
        }

        /* Cube */
        .cube {
            width: 150px;
            height: 150px;
            position: relative;
            transform-style: preserve-3d;
            animation: rotateCube 5s infinite linear;
        }

        /* Cube Faces */
        .cube-face {
            position: absolute;
            width: 150px;
            height: 150px;
            background: rgba(0, 255, 0, 0.7); /* Transparent green */
            border: 2px solid #ffffff; /* White borders */
        }

        .front  { transform: translateZ(75px); }
        .back   { transform: rotateY(180deg) translateZ(75px); }
        .left   { transform: rotateY(-90deg) translateZ(75px); }
        .right  { transform: rotateY(90deg) translateZ(75px); }
        .top    { transform: rotateX(90deg) translateZ(75px); }
        .bottom { transform: rotateX(-90deg) translateZ(75px); }

        /* Animation */
        @keyframes rotateCube {
            from {
                transform: rotateX(0) rotateY(0);
            }
            to {
                transform: rotateX(360deg) rotateY(360deg);
            }
        }

        /* Footer */
        footer {
            margin-top: 40px;
            background: #008000; /* Matches header for consistency */
            padding: 15px 10px;
            color: #ffffff;
            font-size: 0.9em;
            box-shadow: 0 -5px 10px rgba(0, 0, 0, 0.3);
        }
    
        footer p {
            margin: 0;
        }
    
        /* Responsive Design */
        @media (max-width: 768px) {
            .server-info, .player-stats, .news, .shop-info {
                padding: 15px;
            }
    
            header h1 {
                font-size: 2em;
            }
    
            .button, .link {
                padding: 10px 20px;
                font-size: 1em;
            }
        }
    </style>
    
</head>
<body>
    <header>
        <h1>Welcome to My Minecraft Server!</h1>
    </header>
    <div class="container">
        <!-- Server Info Section -->
        <div class="server-info">
            <h2>Server Details</h2>
            <p class="ip">Server IP: <span>pmr9t00ati.scalacube.pro</span></p>
            <p class="port">Port: <span>2445</span></p>
            <p>Status: <strong class="status">Online</strong></p>
            <a href="http://t.me/sadotipol_bot" class="button" aria-label="Join our Discord">Join Telegram</a>
            <a href="https://minecraftrating.ru/vote/201868/" class="button" aria-label="Vote for our server">Vote for Server</a>
        </div>

        <!-- Shop Info Section -->
        <div class="shop-info">
            <h2>Server Shop</h2>
            <p>Support the server by visiting our shop! Purchase exclusive ranks, special items, and perks that enhance your gameplay experience.</p>
            <ul style="list-style-type: none; padding: 0; text-align: left;">
                <li>- <strong>Ranks:</strong> Gain special privileges and stand out from the crowd.</li>
                <li>- <strong>Items:</strong> Get unique tools, armor, and more!</li>
                <li>- <strong>Perks:</strong> Unlock abilities like fly mode, set homes, and more.</li>
            </ul>
            <a href="https://sadxeri.easydonate.ru/" class="button" aria-label="Visit the server shop">Visit Shop</a>
        </div>

        <!-- Social Media Buttons -->
        <div class="social-buttons" id="social">
            <a href="https://www.youtube.com/@sadotipol" target="_blank" class="youtube">YouTube</a>
            <a href="https://instagram.com" target="_blank" class="instagram">Instagram</a>
            <a href="http://t.me/sadotipol_bot" target="_blank" class="telegram">Telegram</a>
            <a href="https://tiktok.com" target="_blank" class="tiktok">TikTok</a>
        </div>

        <div class="cube-container">
            <div class="cube">
                <div class="cube-face front">Front</div>
                <div class="cube-face back">Back</div>
                <div class="cube-face left">Left</div>
                <div class="cube-face right">Right</div>
                <div class="cube-face top">Top</div>
                <div class="cube-face bottom">Bottom</div>
            </div>
        </div>

        <!-- Player Stats Section -->
        <div class="player-stats">
            <h2>Player Stats</h2>
            <p>Players Online: <strong style="color: #00e0e0;">47</strong></p>
            <p>Max Players: <strong style="color: #ffcc00;">100</strong></p>
            <p>Server Uptime: <strong style="color: #00e676;">99.9%</strong></p>
            <a href="https://minecraftrating.ru/server/201868/" class="link" aria-label="View detailed server statistics">View Server Statistics</a>
        </div>

        <!-- News Section -->
        <div class="news">
            <h2>Latest Updates</h2>
            <p>- New survival world added!</p>
            <p>- Holiday event starts next week.</p>
            <p>- Bug fixes and performance improvements.</p>
        </div>
    </div>
    <footer>
        <p>© 2024 My Minecraft Server | Crafted with ❤️ by Sadotipol</p>
    </footer>
</body>
</html>
