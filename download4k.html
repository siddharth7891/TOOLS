<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ultra HD Video Downloader - Download YouTube Videos in 4K, 2K, 1080p</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        :root {
            --primary-color: #ff0000;
            --primary-dark: #cc0000;
            --secondary-color: #282828;
            --light-gray: #f5f5f5;
            --medium-gray: #e0e0e0;
            --dark-gray: #333333;
            --white: #ffffff;
        }
        
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        
        body {
            font-family: 'Roboto', sans-serif;
            background-color: var(--light-gray);
            color: var(--dark-gray);
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* Header Styles */
        .header {
            background-color: var(--primary-color);
            color: var(--white);
            padding: 20px 0;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            position: relative;
            z-index: 10;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .logo i {
            font-size: 28px;
        }
        
        .logo h1 {
            font-size: 24px;
            font-weight: 700;
            margin: 0;
        }
        
        .logo p {
            font-size: 14px;
            opacity: 0.9;
            margin: 0;
        }
        
        /* Ad Styles */
        .ad-container {
            background-color: var(--medium-gray);
            padding: 15px;
            text-align: center;
            margin: 15px 0;
            border-radius: 6px;
            border: 1px dashed #999;
        }
        
        .ad-label {
            font-size: 12px;
            color: #666;
            margin-bottom: 5px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        /* Main Content Styles */
        .main-content {
            background-color: var(--white);
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            padding: 30px;
            margin: 30px 0;
            position: relative;
        }
        
        .section-title {
            font-size: 22px;
            margin-bottom: 20px;
            color: var(--secondary-color);
            position: relative;
            padding-bottom: 10px;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 3px;
            background-color: var(--primary-color);
        }
        
        /* URL Input Section */
        .url-input-container {
            display: flex;
            margin-bottom: 25px;
            gap: 10px;
        }
        
        #video-url {
            flex: 1;
            padding: 15px;
            border: 2px solid var(--medium-gray);
            border-radius: 6px;
            font-size: 16px;
            transition: all 0.3s ease;
        }
        
        #video-url:focus {
            border-color: var(--primary-color);
            outline: none;
            box-shadow: 0 0 0 3px rgba(255, 0, 0, 0.1);
        }
        
        #download-btn {
            padding: 0 25px;
            background-color: var(--primary-color);
            color: var(--white);
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-size: 16px;
            font-weight: 500;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        #download-btn:hover {
            background-color: var(--primary-dark);
            transform: translateY(-2px);
        }
        
        /* Video Preview Section */
        .video-preview {
            display: none;
            margin-bottom: 30px;
            animation: fadeIn 0.5s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .video-container {
            position: relative;
            padding-bottom: 56.25%; /* 16:9 Aspect Ratio */
            height: 0;
            overflow: hidden;
            border-radius: 8px;
            background-color: #000;
        }
        
        .video-container iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: none;
        }
        
        .video-info {
            margin-top: 15px;
        }
        
        .video-title {
            font-size: 18px;
            font-weight: 500;
            margin-bottom: 5px;
        }
        
        .video-meta {
            display: flex;
            gap: 15px;
            font-size: 14px;
            color: #666;
        }
        
        /* Quality Options */
        .quality-options {
            display: none;
            margin-top: 25px;
            animation: fadeIn 0.5s ease;
        }
        
        .quality-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 12px;
            margin-top: 15px;
        }
        
        .quality-btn {
            padding: 12px 15px;
            background-color: var(--white);
            border: 2px solid var(--medium-gray);
            border-radius: 6px;
            text-align: left;
            cursor: pointer;
            transition: all 0.2s ease;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .quality-btn:hover {
            border-color: var(--primary-color);
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        
        .quality-btn i {
            color: var(--primary-color);
            font-size: 18px;
        }
        
        .quality-label {
            font-weight: 500;
        }
        
        .quality-size {
            font-size: 12px;
            color: #666;
            margin-top: 3px;
        }
        
        /* Loading State */
        .loading {
            display: none;
            text-align: center;
            margin: 30px 0;
            animation: fadeIn 0.3s ease;
        }
        
        .spinner {
            border: 4px solid rgba(0, 0, 0, 0.1);
            border-radius: 50%;
            border-top: 4px solid var(--primary-color);
            width: 40px;
            height: 40px;
            animation: spin 1s linear infinite;
            margin: 0 auto 15px;
        }
        
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        /* Footer Styles */
        .footer {
            background-color: var(--secondary-color);
            color: var(--white);
            padding: 30px 0;
            margin-top: 40px;
        }
        
        .footer-content {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 20px;
        }
        
        .footer-links {
            display: flex;
            gap: 20px;
        }
        
        .footer-links a {
            color: var(--white);
            text-decoration: none;
            opacity: 0.8;
            transition: opacity 0.2s ease;
        }
        
        .footer-links a:hover {
            opacity: 1;
        }
        
        .copyright {
            opacity: 0.7;
            font-size: 14px;
            margin-top: 20px;
        }
        
        /* Responsive Styles */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
                gap: 10px;
            }
            
            .url-input-container {
                flex-direction: column;
            }
            
            #download-btn {
                width: 100%;
                justify-content: center;
                padding: 15px;
            }
            
            .quality-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Top Ad Banner -->
    <div class="container">
        <div class="ad-container">
            <div class="ad-label">Advertisement</div>
            <!-- Ad code would go here -->
            <div style="width: 100%; height: 90px; background-color: #f0f0f0; display: flex; align-items: center; justify-content: center; border-radius: 4px;">
                <p style="color: #999;">Top Banner Ad (728x90)</p>
            </div>
        </div>
    </div>
    
    <!-- Header -->
    <header class="header">
        <div class="container header-content">
            <div class="logo">
                <i class="fas fa-play-circle"></i>
                <div>
                    <h1>Ultra HD Video Downloader</h1>
                    <p>Download videos in 4K, 2K, 1080p and more</p>
                </div>
            </div>
            <div class="header-buttons">
                <button style="background: transparent; border: none; color: white; font-size: 16px; cursor: pointer;">
                    <i class="fas fa-question-circle"></i> Help
                </button>
            </div>
        </div>
    </header>
    
    <!-- Main Content -->
    <div class="container">
        <div class="main-content">
            <h2 class="section-title">Download YouTube Videos</h2>
            <p style="margin-bottom: 20px; color: #666;">Paste YouTube video URL below to download in high quality</p>
            
            <div class="url-input-container">
                <input type="text" id="video-url" placeholder="https://www.youtube.com/watch?v=..." />
                <button id="download-btn">
                    <i class="fas fa-download"></i> Process
                </button>
            </div>
            
            <!-- Video Preview Section -->
            <div class="video-preview" id="video-preview">
                <div class="video-container" id="video-embed">
                    <!-- Video iframe will be inserted here -->
                </div>
                <div class="video-info">
                    <h3 class="video-title" id="video-title">Video Title Will Appear Here</h3>
                    <div class="video-meta">
                        <span><i class="fas fa-eye"></i> <span id="video-views">0</span> views</span>
                        <span><i class="far fa-clock"></i> <span id="video-duration">0:00</span></span>
                        <span><i class="far fa-calendar-alt"></i> <span id="video-date">Jan 1, 2023</span></span>
                    </div>
                </div>
            </div>
            
            <!-- Loading State -->
            <div class="loading" id="loading">
                <div class="spinner"></div>
                <p>Processing video information...</p>
            </div>
            
            <!-- Quality Options -->
            <div class="quality-options" id="quality-options">
                <h2 class="section-title">Download Options</h2>
                <p style="margin-bottom: 15px; color: #666;">Select your preferred quality to download</p>
                
                <div class="quality-grid">
                    <button class="quality-btn" data-quality="2160">
                        <i class="fas fa-film"></i>
                        <div>
                            <div class="quality-label">4K Ultra HD (2160p)</div>
                            <div class="quality-size">MP4 • ≈500MB</div>
                        </div>
                    </button>
                    
                    <button class="quality-btn" data-quality="1440">
                        <i class="fas fa-film"></i>
                        <div>
                            <div class="quality-label">2K Quad HD (1440p)</div>
                            <div class="quality-size">MP4 • ≈300MB</div>
                        </div>
                    </button>
                    
                    <button class="quality-btn" data-quality="1080">
                        <i class="fas fa-film"></i>
                        <div>
                            <div class="quality-label">Full HD (1080p)</div>
                            <div class="quality-size">MP4 • ≈150MB</div>
                        </div>
                    </button>
                    
                    <button class="quality-btn" data-quality="720">
                        <i class="fas fa-film"></i>
                        <div>
                            <div class="quality-label">HD (720p)</div>
                            <div class="quality-size">MP4 • ≈80MB</div>
                        </div>
                    </button>
                    
                    <button class="quality-btn" data-quality="480">
                        <i class="fas fa-film"></i>
                        <div>
                            <div class="quality-label">SD (480p)</div>
                            <div class="quality-size">MP4 • ≈50MB</div>
                        </div>
                    </button>
                    
                    <button class="quality-btn" data-quality="360">
                        <i class="fas fa-film"></i>
                        <div>
                            <div class="quality-label">360p</div>
                            <div class="quality-size">MP4 • ≈30MB</div>
                        </div>
                    </button>
                    
                    <button class="quality-btn" data-quality="audio">
                        <i class="fas fa-music"></i>
                        <div>
                            <div class="quality-label">Audio Only</div>
                            <div class="quality-size">MP3 • ≈10MB</div>
                        </div>
                    </button>
                </div>
            </div>
        </div>
    </div>
    
    <!-- Bottom Ad Banner -->
    <div class="container">
        <div class="ad-container">
            <div class="ad-label">Advertisement</div>
            <!-- Ad code would go here -->
            <div style="width: 100%; height: 250px; background-color: #f0f0f0; display: flex; align-items: center; justify-content: center; border-radius: 4px;">
                <p style="color: #999;">Bottom Rectangle Ad (300x250)</p>
            </div>
        </div>
    </div>
    
    <!-- Footer -->
    <footer class="footer">
        <div class="container footer-content">
            <div class="footer-links">
                <a href="#"><i class="fas fa-home"></i> Home</a>
                <a href="#"><i class="fas fa-info-circle"></i> About</a>
                <a href="#"><i class="fas fa-question-circle"></i> FAQ</a>
                <a href="#"><i class="fas fa-shield-alt"></i> Privacy</a>
                <a href="#"><i class="fas fa-file-alt"></i> Terms</a>
                <a href="#"><i class="fas fa-envelope"></i> Contact</a>
            </div>
            <div class="copyright">
                &copy; 2023 Ultra HD Video Downloader. This tool is for educational purposes only.
            </div>
        </div>
    </footer>
    
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const videoUrlInput = document.getElementById('video-url');
            const downloadBtn = document.getElementById('download-btn');
            const videoPreview = document.getElementById('video-preview');
            const videoEmbed = document.getElementById('video-embed');
            const videoTitle = document.getElementById('video-title');
            const videoViews = document.getElementById('video-views');
            const videoDuration = document.getElementById('video-duration');
            const videoDate = document.getElementById('video-date');
            const loading = document.getElementById('loading');
            const qualityOptions = document.getElementById('quality-options');
            
            // Sample video data (in a real app, this would come from an API)
            const sampleVideoData = {
                title: "Amazing Nature in 4K | Relaxing Video",
                views: "1,245,678",
                duration: "8:32",
                date: "May 15, 2023",
                id: "dQw4w9WgXcQ" // Sample video ID
            };
            
            downloadBtn.addEventListener('click', function() {
                const videoUrl = videoUrlInput.value.trim();
                
                if (!videoUrl) {
                    showError('Please enter a YouTube video URL');
                    return;
                }
                
                // Simple URL validation
                if (!isValidYouTubeUrl(videoUrl)) {
                    showError('Please enter a valid YouTube URL');
                    return;
                }
                
                // Extract video ID (simplified version)
                const videoId = extractVideoId(videoUrl);
                
                if (!videoId) {
                    showError('Could not extract video ID from URL');
                    return;
                }
                
                // Show loading state
                loading.style.display = 'block';
                videoPreview.style.display = 'none';
                qualityOptions.style.display = 'none';
                
                // Simulate API call with setTimeout
                setTimeout(function() {
                    // Hide loading
                    loading.style.display = 'none';
                    
                    // Show video preview
                    showVideoPreview(videoId);
                    
                    // Show quality options
                    qualityOptions.style.display = 'block';
                    
                    // Update video info (in a real app, this would come from API)
                    updateVideoInfo(sampleVideoData);
                    
                    // Scroll to quality options
                    qualityOptions.scrollIntoView({ behavior: 'smooth' });
                }, 2000);
            });
            
            // Handle quality selection
            document.querySelectorAll('.quality-btn').forEach(btn => {
                btn.addEventListener('click', function() {
                    const quality = this.getAttribute('data-quality');
                    const videoUrl = videoUrlInput.value.trim();
                    const videoId = extractVideoId(videoUrl);
                    
                    showDownloadStarted(quality, videoId);
                });
            });
            
            // Helper functions
            function isValidYouTubeUrl(url) {
                return url.includes('youtube.com') || url.includes('youtu.be');
            }
            
            function extractVideoId(url) {
                // Very simplified version - in a real app you'd need more robust parsing
                if (url.includes('v=')) {
                    return url.split('v=')[1].split('&')[0];
                } else if (url.includes('youtu.be/')) {
                    return url.split('youtu.be/')[1].split('?')[0];
                }
                return null;
            }
            
            function showVideoPreview(videoId) {
                videoEmbed.innerHTML = `
                    <iframe src="https://www.youtube.com/embed/${videoId}?autoplay=0&showinfo=0&controls=1" 
                            frameborder="0" 
                            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                            allowfullscreen>
                    </iframe>
                `;
                videoPreview.style.display = 'block';
            }
            
            function updateVideoInfo(data) {
                videoTitle.textContent = data.title;
                videoViews.textContent = data.views;
                videoDuration.textContent = data.duration;
                videoDate.textContent = data.date;
            }
            
            function showDownloadStarted(quality, videoId) {
                let qualityLabel = '';
                switch(quality) {
                    case '2160': qualityLabel = '4K (2160p)'; break;
                    case '1440': qualityLabel = '2K (1440p)'; break;
                    case '1080': qualityLabel = 'Full HD (1080p)'; break;
                    case '720': qualityLabel = 'HD (720p)'; break;
                    case '480': qualityLabel = 'SD (480p)'; break;
                    case '360': qualityLabel = '360p'; break;
                    case 'audio': qualityLabel = 'Audio Only (MP3)'; break;
                    default: qualityLabel = 'Unknown Quality';
                }
                
                alert(`Starting download in ${qualityLabel} quality...\n\nVideo ID: ${videoId}\n\nIn a real application, this would initiate the download process.`);
            }
            
            function showError(message) {
                alert(message);
            }
        });
    </script>
</body>
</html>
