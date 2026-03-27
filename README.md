<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>🎉 SURPRISE! Happy Birthday Sister! 🎉</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;700&family=Poppins:wght@300;400;600;700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #ff9a9e 0%, #fecfef 50%, #fecfef 100%);
            min-height: 100vh;
            overflow-x: hidden;
            position: relative;
        }
        
        /* Animated Background */
        .stars {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 1;
        }
        
        .star {
            position: absolute;
            width: 4px;
            height: 4px;
            background: #fff;
            border-radius: 50%;
            animation: twinkle 2s infinite;
        }
        
        @keyframes twinkle {
            0%, 100% { opacity: 0.3; transform: scale(1); }
            50% { opacity: 1; transform: scale(1.5); }
        }
        
        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
            z-index: 10;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
        }
        
        .hack-text {
            font-size: 4rem;
            font-weight: 700;
            color: #ff4757;
            text-shadow: 0 0 20px rgba(255, 71, 87, 0.5);
            margin-bottom: 20px;
            animation: glitch 2s infinite;
            font-family: 'Courier New', monospace;
        }
        
        @keyframes glitch {
            0%, 100% { transform: translate(0); }
            20% { transform: translate(-2px, 2px); }
            40% { transform: translate(-2px, -2px); }
            60% { transform: translate(2px, 2px); }
            80% { transform: translate(2px, -2px); }
        }
        
        .surprise-btn {
            background: linear-gradient(45deg, #ff6b6b, #ff8e8e);
            color: white;
            border: none;
            padding: 15px 40px;
            font-size: 1.5rem;
            font-weight: 600;
            border-radius: 50px;
            cursor: pointer;
            box-shadow: 0 10px 30px rgba(255, 107, 107, 0.4);
            transition: all 0.3s ease;
            margin: 20px;
            text-transform: uppercase;
            letter-spacing: 2px;
        }
        
        .surprise-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(255, 107, 107, 0.6);
        }
        
        .surprise-btn:active {
            transform: translateY(-2px);
        }
        
        .message-box {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(20px);
            border-radius: 30px;
            padding: 50px;
            margin: 40px 0;
            box-shadow: 0 25px 50px rgba(0,0,0,0.1);
            max-width: 800px;
            display: none;
            font-size: 1.4rem;
            line-height: 1.8;
            position: relative;
            overflow: hidden;
        }
        
        .message-box h1 {
            font-family: 'Dancing Script', cursive;
            font-size: 3.5rem;
            color: #ff6b6b;
            margin-bottom: 30px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
        }
        
        .message-box p {
            color: #333;
            margin-bottom: 20px;
            font-weight: 300;
        }
        
        .typewriter {
            overflow: hidden;
            border-right: 3px solid #ff6b6b;
            white-space: nowrap;
            animation: typing 8s steps(40, end), blink-caret 0.75s step-end infinite;
        }
        
        @keyframes typing {
            from { width: 0; }
            to { width: 100%; }
        }
        
        @keyframes blink-caret {
            from, to { border-color: transparent; }
            50% { border-color: #ff6b6b; }
        }
        
        .cake {
            font-size: 4rem;
            margin: 30px 0;
            animation: bounce 2s infinite;
        }
        
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-20px); }
            60% { transform: translateY(-10px); }
        }
        
        .link-box {
            background: linear-gradient(45deg, #4ecdc4, #44a08d);
            color: white;
            padding: 20px 40px;
            border-radius: 25px;
            margin-top: 30px;
            box-shadow: 0 10px 30px rgba(78, 205, 196, 0.4);
            display: none;
        }
        
        .link-box a {
            color: white;
            text-decoration: none;
            font-size: 1.2rem;
            font-weight: 600;
        }
        
        @media (max-width: 768px) {
            .hack-text { font-size: 2.5rem; }
            .message-box { padding: 30px 20px; font-size: 1.2rem; }
            .message-box h1 { font-size: 2.5rem; }
            .surprise-btn { padding: 12px 30px; font-size: 1.2rem; }
        }
    </style>
</head>
<body>
    <div class="stars" id="stars"></div>
    
    <div class="container">
        <div class="hack-text" id="hackText">Now!!! You have been hacked 😈</div>
        <p style="font-size: 1.3rem; color: #666; margin-bottom: 40px;">
            There was a surprise for you... 😊
        </p>
        
        <button class="surprise-btn" onclick="revealSurprise()">
            Ready for your SURPRISE? 😍
        </button>
        <p style="font-size: 1rem; color: #888; margin-top: 20px;">
            Say NO if you want to say YES... Take your own risk! 😏
        </div>
        
        <div class="message-box" id="messageBox">
            <div class="cake">🎂✨🎉</div>
            <h1>Happy Birthday Sister! 💖</h1>
            <div class="typewriter" id="typewriter">
                <p>Happy Birthday! Thanks for being my unpaid therapist 😄</p>
                <p>Happy Birthday to my amazing sister! 🎉 You are not just my sibling, but also my best friend and biggest support.</p>
                <p>Thank you for always being there for me, understanding me, and filling my life with happiness and laughter.</p>
                <p>I'm so lucky to have you in my life.</p>
                <p>May your day be full of love, joy, and all the things that make you smile.</p>
                <p>Stay blessed and keep shining always! 💖</p>
            </div>
        </div>
        
        <div class="link-box" id="linkBox">
            <p>🎁 Special Gift for you!</p>
            <a href="https://share.google/hLY3axSteFf73s4Zc" target="_blank">Visit this site →</a>
        </div>
    </div>

    <script>
        // Create twinkling stars
        function createStars() {
            const starsContainer = document.getElementById('stars');
            for (let i = 0; i < 100; i++) {
                const star = document.createElement('div');
                star.className = 'star';
                star.style.left = Math.random() * 100 + '%';
                star.style.top = Math.random() * 100 + '%';
                star.style.animationDelay = Math.random() * 2 + 's';
                starsContainer.appendChild(star);
            }
        }
        
        function revealSurprise() {
            const hackText = document.getElementById('hackText');
            const container = document.querySelector('.container');
            const messageBox = document.getElementById('messageBox');
            const linkBox = document.getElementById('linkBox');
            
            hackText.style.display = 'none';
            container.querySelector('p').style.display = 'none';
            container.querySelector('.surprise-btn').style.display = 'none';
            
            setTimeout(() => {
                messageBox.style.display = 'block';
                linkBox.style.display = 'block';
            }, 500);
        }
        
        // Initialize
        createStars();
        
        // Glitch effect for hack text
        setInterval(() => {
            const hackText = document.getElementById('hackText');
            hackText.style.color = `hsl(${Math.random() * 360}, 70%, 60%)`;
        }, 100);
    </script>
</body>
</html>
 
