<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Speed Racer - Play Online</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Arial', sans-serif;
            background: #111;
            color: white;
            overflow: hidden;
        }
        
        /* Header */
        .header {
            background: #222;
            padding: 10px;
            text-align: center;
            border-bottom: 3px solid #FF5722;
        }
        
        .logo {
            font-size: 28px;
            font-weight: bold;
            color: #FF5722;
        }
        
        /* Ad Spaces with Unit ID Labels */
        .ad-container {
            width: 100%;
            margin: 5px auto;
            text-align: center;
        }
        
        .ad-label {
            color: #aaa;
            font-size: 12px;
            margin-bottom: 5px;
        }
        
        .ad-unit {
            background: #333;
            color: #999;
            padding: 10px;
            border: 1px dashed #555;
            margin: 0 auto;
        }
        
        /* Game Canvas */
        #gameCanvas {
            background: #000;
            display: block;
            margin: 0 auto;
            border: 2px solid #FF5722;
        }
        
        /* Game Info */
        .game-info {
            text-align: center;
            margin: 10px;
            font-size: 18px;
        }
        
        .score {
            color: #4CAF50;
            font-weight: bold;
        }
        
        /* Game Over Popup */
        .game-over {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 100;
            display: none;
        }
        
        .popup {
            background: #222;
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            border: 2px solid #FF5722;
        }
        
        .popup h2 {
            color: #FF5722;
        }
        
        .popup button {
            background: #4CAF50;
            color: white;
            border: none;
            padding: 10px 20px;
            margin: 10px;
            cursor: pointer;
            border-radius: 5px;
        }
        
        /* Footer */
        .footer {
            background: #222;
            text-align: center;
            padding: 10px;
            margin-top: 10px;
            border-top: 3px solid #FF5722;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <div class="header">
        <div class="logo">SPEED RACER</div>
    </div>
    
    <!-- Top Ad Unit with ID -->
    <div class="ad-container">
        <div class="ad-label">AD UNIT ID: TOP_BANNER_728x90</div>
        <div class="ad-unit" style="width: 728px; height: 90px;">
            <!-- Replace with actual AdSense code -->
            <!-- Example: 
            <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-YOUR_PUB_ID"
                crossorigin="anonymous"></script>
            <ins class="adsbygoogle"
                style="display:inline-block;width:728px;height:90px"
                data-ad-client="ca-pub-YOUR_PUB_ID"
                data-ad-slot="YOUR_AD_SLOT_TOP"></ins>
            <script>
                (adsbygoogle = window.adsbygoogle || []).push({});
            </script>
            -->
            ADVERTISEMENT PLACEHOLDER (728x90)
        </div>
    </div>
    
    <!-- Game Canvas -->
    <canvas id="gameCanvas" width="400" height="600"></canvas>
    
    <!-- Game Info -->
    <div class="game-info">
        Score: <span class="score" id="score">0</span> | 
        Speed: <span id="speed">0</span> km/h
        <br>
        <button id="startBtn">Start Game</button>
    </div>
    
    <!-- Bottom Ad Unit with ID -->
    <div class="ad-container">
        <div class="ad-label">AD UNIT ID: BOTTOM_BANNER_728x90</div>
        <div class="ad-unit" style="width: 728px; height: 90px;">
            <!-- Replace with actual AdSense code -->
            ADVERTISEMENT PLACEHOLDER (728x90)
        </div>
    </div>
    
    <!-- Game Over Popup -->
    <div class="game-over" id="gameOver">
        <div class="popup">
            <h2>GAME OVER!</h2>
            <p>Your Score: <span id="finalScore">0</span></p>
            <button id="restartBtn">Play Again</button>
        </div>
    </div>
    
    <!-- Footer -->
    <div class="footer">
        &copy; 2023 Speed Racer | Play Free Online Games
    </div>
    
    <script>
        // Game Setup
        const canvas = document.getElementById("gameCanvas");
        const ctx = canvas.getContext("2d");
        const scoreElement = document.getElementById("score");
        const speedElement = document.getElementById("speed");
        const startBtn = document.getElementById("startBtn");
        const gameOverScreen = document.getElementById("gameOver");
        const finalScoreElement = document.getElementById("finalScore");
        const restartBtn = document.getElementById("restartBtn");
        
        // Game Variables
        let score = 0;
        let speed = 0;
        let gameRunning = false;
        let playerX = canvas.width / 2 - 15;
        let roadY = 0;
        let cars = [];
        let keys = {
            ArrowLeft: false,
            ArrowRight: false
        };
        
        // Player Car
        function drawPlayerCar() {
            ctx.fillStyle = "#2196F3";
            ctx.fillRect(playerX, canvas.height - 100, 30, 50);
            
            // Car details
            ctx.fillStyle = "#0D47A1";
            ctx.fillRect(playerX + 5, canvas.height - 90, 20, 30);
        }
        
        // Road
        function drawRoad() {
            ctx.fillStyle = "#333";
            ctx.fillRect(0, 0, canvas.width, canvas.height);
            
            // Road markings
            ctx.strokeStyle = "#fff";
            ctx.lineWidth = 3;
            ctx.setLineDash([30, 20]);
            ctx.beginPath();
            ctx.moveTo(canvas.width / 2, roadY);
            ctx.lineTo(canvas.width / 2, roadY + canvas.height);
            ctx.stroke();
            ctx.setLineDash([]);
            
            roadY += speed / 2;
            if (roadY > 30) roadY = 0;
        }
        
        // Enemy Cars
        function createEnemyCar() {
            if (Math.random() < 0.02 && gameRunning) {
                cars.push({
                    x: Math.random() * (canvas.width - 30),
                    y: -50,
                    width: 30,
                    height: 50,
                    speed: 3 + Math.random() * 3
                });
            }
        }
        
        function drawEnemyCars() {
            ctx.fillStyle = "#FF5722";
            cars.forEach((car, index) => {
                ctx.fillRect(car.x, car.y, car.width, car.height);
                car.y += car.speed;
                
                // Remove cars that are off-screen
                if (car.y > canvas.height) {
                    cars.splice(index, 1);
                    score += 5;
                    scoreElement.textContent = score;
                }
                
                // Collision Detection
                if (
                    playerX < car.x + car.width &&
                    playerX + 30 > car.x &&
                    canvas.height - 100 < car.y + car.height &&
                    canvas.height - 100 + 50 > car.y
                ) {
                    gameOver();
                }
            });
        }
        
        // Game Loop
        function gameLoop() {
            if (!gameRunning) return;
            
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            drawRoad();
            drawPlayerCar();
            drawEnemyCars();
            createEnemyCar();
            
            // Player Movement
            if (keys.ArrowLeft && playerX > 0) playerX -= 5;
            if (keys.ArrowRight && playerX < canvas.width - 30) playerX += 5;
            
            // Increase Speed
            if (speed < 10) speed += 0.01;
            speedElement.textContent = Math.floor(speed * 20);
            
            requestAnimationFrame(gameLoop);
        }
        
        // Start Game
        startBtn.addEventListener("click", () => {
            score = 0;
            speed = 0;
            cars = [];
            gameRunning = true;
            scoreElement.textContent = score;
            gameOverScreen.style.display = "none";
            gameLoop();
        });
        
        // Restart Game
        restartBtn.addEventListener("click", () => {
            gameOverScreen.style.display = "none";
            score = 0;
            speed = 0;
            cars = [];
            gameRunning = true;
            scoreElement.textContent = score;
            gameLoop();
        });
        
        // Game Over
        function gameOver() {
            gameRunning = false;
            finalScoreElement.textContent = score;
            gameOverScreen.style.display = "flex";
        }
        
        // Keyboard Controls
        window.addEventListener("keydown", (e) => {
            if (e.key in keys) keys[e.key] = true;
        });
        
        window.addEventListener("keyup", (e) => {
            if (e.key in keys) keys[e.key] = false;
        });
    </script>
</body>
</html>
