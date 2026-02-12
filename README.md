
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Valentine? 💝</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }

        .container {
            text-align: center;
            background: white;
            padding: 60px 40px;
            border-radius: 30px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            max-width: 500px;
            position: relative;
        }

        h1 {
            font-size: 2.5em;
            color: #e91e63;
            margin-bottom: 20px;
            animation: pulse 2s infinite;
        }

        .heart {
            font-size: 4em;
            margin: 20px 0;
            animation: heartbeat 1.5s infinite;
        }

        p {
            font-size: 1.3em;
            color: #555;
            margin-bottom: 40px;
            line-height: 1.6;
        }

        .buttons-container {
            position: relative;
            height: 150px;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 20px;
        }

        button {
            padding: 15px 40px;
            font-size: 1.2em;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            font-weight: bold;
            transition: transform 0.2s, box-shadow 0.2s;
            position: relative;
        }

        #yesBtn {
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            color: white;
            box-shadow: 0 4px 15px rgba(245, 87, 108, 0.4);
        }

        #yesBtn:hover {
            transform: scale(1.1);
            box-shadow: 0 6px 20px rgba(245, 87, 108, 0.6);
        }

        #noBtn {
            background: linear-gradient(135deg, #a8a8a8 0%, #7a7a7a 100%);
            color: white;
            box-shadow: 0 4px 15px rgba(122, 122, 122, 0.4);
            position: absolute;
        }

        .celebration {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            justify-content: center;
            align-items: center;
            flex-direction: column;
            z-index: 1000;
        }

        .meme-screen {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, #2c3e50 0%, #34495e 100%);
            justify-content: center;
            align-items: center;
            flex-direction: column;
            z-index: 2000;
            animation: fadeIn 0.5s ease-in;
        }

        .meme-container {
            text-align: center;
            padding: 40px;
            max-width: 600px;
        }

        .meme-image {
            margin: 20px 0;
            animation: shake 0.5s ease-in-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes shake {
            0%, 100% { transform: translateX(0); }
            10%, 30%, 50%, 70%, 90% { transform: translateX(-10px); }
            20%, 40%, 60%, 80% { transform: translateX(10px); }
        }

        .celebration h1 {
            font-size: 4em;
            color: white;
            margin-bottom: 30px;
        }

        .celebration p {
            font-size: 1.8em;
            color: white;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        @keyframes heartbeat {
            0%, 100% { transform: scale(1); }
            10%, 30% { transform: scale(1.1); }
            20%, 40% { transform: scale(1); }
        }

        @keyframes confetti {
            0% { transform: translateY(-100vh) rotate(0deg); }
            100% { transform: translateY(100vh) rotate(360deg); }
        }

        .confetti {
            position: fixed;
            width: 10px;
            height: 10px;
            background: #f0f;
            animation: confetti 3s linear infinite;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Will You Be My Valentine?</h1>
        <div class="heart">💖</div>
        <p>I've been thinking about this for a while now... Will you make me the happiest person and be my Valentine?</p>
        
        <div class="buttons-container">
            <button id="yesBtn">Yes! 💕</button>
            <button id="noBtn">No</button>
        </div>
    </div>

    <div class="celebration" id="celebration">
        <h1>Yay! 🎉💖✨</h1>
        <p>You just made my day! I'm so happy! 😊</p>
        <div class="heart" style="font-size: 6em; margin-top: 30px;">💝</div>
    </div>

    <div class="meme-screen" id="memeScreen">
        <div class="meme-container">
            <h1 style="color: #ff4757; font-size: 3em; margin-bottom: 20px;">WRONG CHOICE! 🚫</h1>
            <div class="meme-image">
                <img src="https://media.giphy.com/media/STfLOU6iRBRunMciZv/giphy.gif" alt="Disappointed" style="width: 100%; max-width: 400px; border-radius: 20px;">
            </div>
            <p style="font-size: 1.5em; margin: 30px 0; color: white;">You really thought you could escape? 😏</p>
            <p style="font-size: 1.2em; margin-bottom: 30px; color: white;">There's only ONE right answer here! 💕</p>
            <button id="tryAgainBtn" style="padding: 15px 40px; font-size: 1.3em; background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%); color: white; border: none; border-radius: 50px; cursor: pointer; font-weight: bold; box-shadow: 0 4px 15px rgba(245, 87, 108, 0.4);">
                Try Again 💖
            </button>
        </div>
    </div>

    <script>
        const noBtn = document.getElementById('noBtn');
        const yesBtn = document.getElementById('yesBtn');
        const celebration = document.getElementById('celebration');
        const memeScreen = document.getElementById('memeScreen');
        const tryAgainBtn = document.getElementById('tryAgainBtn');
        
        let noAttempts = 0;
        let startTime = null;
        let persistenceTimer = null;

        function moveButton() {
            const container = document.querySelector('.buttons-container');
            const containerRect = container.getBoundingClientRect();
            
            // Get random position within the container
            const maxX = containerRect.width - noBtn.offsetWidth;
            const maxY = containerRect.height - noBtn.offsetHeight;
            
            const randomX = Math.random() * maxX;
            const randomY = Math.random() * maxY;
            
            noBtn.style.left = randomX + 'px';
            noBtn.style.top = randomY + 'px';
            
            // Track attempts
            noAttempts++;
            
            // Start timer on first attempt
            if (startTime === null) {
                startTime = Date.now();
                checkPersistence();
            }
        }

        function checkPersistence() {
            persistenceTimer = setInterval(() => {
                if (startTime && (Date.now() - startTime) >= 5000) {
                    // 5 seconds have passed
                    showMeme();
                    clearInterval(persistenceTimer);
                }
            }, 100);
        }

        function showMeme() {
            memeScreen.style.display = 'flex';
        }

        function resetGame() {
            memeScreen.style.display = 'none';
            noAttempts = 0;
            startTime = null;
            if (persistenceTimer) {
                clearInterval(persistenceTimer);
                persistenceTimer = null;
            }
        }

        // Move button on hover
        noBtn.addEventListener('mouseenter', moveButton);

        // Move button on touch devices
        noBtn.addEventListener('touchstart', (e) => {
            e.preventDefault();
            moveButton();
        });

        // Try to click but it moves away
        noBtn.addEventListener('click', (e) => {
            e.preventDefault();
            moveButton();
        });

        // Try again button
        tryAgainBtn.addEventListener('click', resetGame);

        // Yes button celebration
        yesBtn.addEventListener('click', () => {
            // Clear any timers
            if (persistenceTimer) {
                clearInterval(persistenceTimer);
            }
            
            celebration.style.display = 'flex';
            
            // Create confetti
            for (let i = 0; i < 50; i++) {
                setTimeout(() => {
                    const confetti = document.createElement('div');
                    confetti.className = 'confetti';
                    confetti.style.left = Math.random() * 100 + '%';
                    confetti.style.background = ['#f093fb', '#f5576c', '#ffd700', '#00ff00', '#00ffff'][Math.floor(Math.random() * 5)];
                    confetti.style.animationDuration = (Math.random() * 2 + 2) + 's';
                    confetti.style.animationDelay = (Math.random() * 2) + 's';
                    celebration.appendChild(confetti);
                }, i * 50);
            }
        });
    </script>
</body>
</html>
