<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Orange Clicker Game</title>
    <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-5431940865562150" crossorigin="anonymous"></script>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #fff8f0;
            overflow-x: hidden;
        }
        
        .ad-banner {
            width: 100%;
            height: 90px;
            background: linear-gradient(135deg, #ff9a44, #ff6b6b);
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            font-weight: bold;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        .top-ad {
            border-bottom: 2px solid #ffa500;
        }
        
        .bottom-ad {
            border-top: 2px solid #ffa500;
            position: fixed;
            bottom: 0;
        }
        
        .container {
            max-width: 800px;
            margin: 20px auto;
            padding: 20px;
            text-align: center;
            min-height: calc(100vh - 270px);
        }
        
        h1 {
            color: #ff7b25;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
        }
        
        .counter {
            font-size: 24px;
            color: #ff7b25;
            margin: 20px 0;
        }
        
        .oranges-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            margin-top: 30px;
            min-height: 300px;
        }
        
        .orange {
            width: 80px;
            height: 80px;
            background: radial-gradient(circle at 30% 30%, #ffa500, #ff8c00);
            border-radius: 50%;
            cursor: pointer;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
            transition: transform 0.2s;
            position: relative;
            animation: float 3s infinite ease-in-out;
        }
        
        .orange:hover {
            transform: scale(1.1);
        }
        
        .orange::before {
            content: "";
            position: absolute;
            width: 15px;
            height: 15px;
            background: rgba(255,255,255,0.3);
            border-radius: 50%;
            top: 20px;
            left: 20px;
        }
        
        .orange::after {
            content: "";
            position: absolute;
            width: 5px;
            height: 10px;
            background: #8b4513;
            top: 15px;
            left: 40px;
            transform: rotate(30deg);
        }
        
        @keyframes float {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-10px);
            }
        }
        
        .moving-orange {
            position: absolute;
            animation: moveAround 10s linear infinite;
        }
        
        @keyframes moveAround {
            0% {
                transform: translate(0, 0);
            }
            25% {
                transform: translate(200px, 100px);
            }
            50% {
                transform: translate(400px, 0);
            }
            75% {
                transform: translate(200px, -100px);
            }
            100% {
                transform: translate(0, 0);
            }
        }
        
        .stats {
            background-color: white;
            padding: 15px;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            margin-top: 20px;
        }
        
        .reset-btn {
            background-color: #ff6b6b;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            font-size: 16px;
            cursor: pointer;
            margin-top: 15px;
            transition: background-color 0.3s;
        }
        
        .reset-btn:hover {
            background-color: #ff5252;
        }
    </style>
</head>
<body>
    <!-- Top AdMob Banner -->
    <div class="ad-banner top-ad">
        <ins class="adsbygoogle"
             style="display:block"
             data-ad-client="ca-pub-5431940865562150"
             data-ad-slot="5033810539"
             data-ad-format="auto"
             data-full-width-responsive="true"></ins>
        <script>
             (adsbygoogle = window.adsbygoogle || []).push({});
        </script>
    </div>
    
    <div class="container">
        <h1>🍊 Orange Clicker Game 🍊</h1>
        <p>Click the orange to make more oranges! They'll float around your screen.</p>
        
        <div class="counter">
            Oranges: <span id="count">1</span>
        </div>
        
        <div class="oranges-container" id="oranges">
            <div class="orange" onclick="createOrange(this)"></div>
        </div>
        
        <div class="stats">
            <p>Total clicks: <span id="clicks">0</span></p>
            <p>Oranges per second: <span id="ops">0</span></p>
            <button class="reset-btn" onclick="resetGame()">Reset Game</button>
        </div>
    </div>
    
    <!-- Bottom AdMob Banner -->
    <div class="ad-banner bottom-ad">
        <ins class="adsbygoogle"
             style="display:block"
             data-ad-client="ca-pub-5431940865562150"
             data-ad-slot="5033810539"
             data-ad-format="auto"
             data-full-width-responsive="true"></ins>
        <script>
             (adsbygoogle = window.adsbygoogle || []).push({});
        </script>
    </div>

    <script>
        let orangeCount = 1;
        let clickCount = 0;
        let orangesPerSecond = 0;
        let movingOranges = [];
        
        function createOrange(clickedOrange) {
            clickCount++;
            document.getElementById('clicks').textContent = clickCount;
            
            // Create two new oranges
            for (let i = 0; i < 2; i++) {
                const newOrange = document.createElement('div');
                newOrange.className = 'orange moving-orange';
                
                // Random position and animation
                const startX = Math.random() * window.innerWidth;
                const startY = Math.random() * (window.innerHeight - 180) + 90;
                const duration = 5 + Math.random() * 10;
                
                newOrange.style.left = startX + 'px';
                newOrange.style.top = startY + 'px';
                newOrange.style.animation = `moveAround ${duration}s linear infinite`;
                newOrange.style.animationDelay = Math.random() * 5 + 's';
                
                newOrange.onclick = function() {
                    createOrange(this);
                };
                
                document.body.appendChild(newOrange);
                movingOranges.push(newOrange);
                orangeCount++;
            }
            
            // Update counter
            document.getElementById('count').textContent = orangeCount;
            
            // Remove the clicked orange if it's not the original one
            if (!clickedOrange.parentElement.id === 'oranges') {
                clickedOrange.remove();
                const index = movingOranges.indexOf(clickedOrange);
                if (index > -1) {
                    movingOranges.splice(index, 1);
                }
            }
            
            // Calculate oranges per second (simple version)
            if (clickCount > 1) {
                orangesPerSecond = Math.round((orangeCount / clickCount) * 10);
                document.getElementById('ops').textContent = orangesPerSecond;
            }
        }
        
        function resetGame() {
            // Remove all moving oranges
            movingOranges.forEach(orange => {
                if (orange.parentNode) {
                    orange.parentNode.removeChild(orange);
                }
            });
            movingOranges = [];
            
            // Reset counters
            orangeCount = 1;
            clickCount = 0;
            orangesPerSecond = 0;
            
            document.getElementById('count').textContent = orangeCount;
            document.getElementById('clicks').textContent = clickCount;
            document.getElementById('ops').textContent = orangesPerSecond;
            
            // Recreate the original orange if it's missing
            const orangesContainer = document.getElementById('oranges');
            if (orangesContainer.children.length === 0) {
                const originalOrange = document.createElement('div');
                originalOrange.className = 'orange';
                originalOrange.onclick = function() {
                    createOrange(this);
                };
                orangesContainer.appendChild(originalOrange);
            }
        }
        
        // Make original oranges move after a while
        setTimeout(() => {
            const originalOrange = document.querySelector('#oranges .orange');
            if (originalOrange) {
                originalOrange.classList.add('moving-orange');
                originalOrange.style.position = 'absolute';
                originalOrange.style.left = '50%';
                originalOrange.style.top = '50%';
                originalOrange.style.animation = 'moveAround 8s linear infinite';
                movingOranges.push(originalOrange);
            }
        }, 5000);
    </script>
</body>
</html>
