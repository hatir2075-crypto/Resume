# Auncle-gamer

<!DOCTYPE html>
<html lang="hi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes, shrink-to-fit=no, viewport-fit=cover">
  <title>💎 AUNCLE GAMER STUDIO • Free Fire MAX Diamonds</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #020202;
      font-family: 'Poppins', 'Segoe UI', system-ui, -apple-system, sans-serif;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 0.8rem;
      margin: 0;
      position: relative;
      overflow-x: hidden;
    }

    .premium-bg {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: radial-gradient(ellipse at 30% 30%, #1e1500 0%, #000000 85%);
      z-index: -2;
    }

    .gold-dust {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-image: radial-gradient(circle at 25% 25%, rgba(255, 200, 0, 0.12) 0%, transparent 35%),
        radial-gradient(circle at 75% 60%, rgba(255, 180, 0, 0.1) 0%, transparent 40%),
        radial-gradient(circle at 50% 80%, rgba(212, 175, 55, 0.08) 0%, transparent 45%);
      z-index: -1;
      pointer-events: none;
    }

    .welcome-overlay {
      position: fixed;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      background: radial-gradient(ellipse at center, #1c1400 0%, #000000 100%);
      display: flex;
      align-items: center;
      justify-content: center;
      z-index: 1000;
      backdrop-filter: blur(10px);
      animation: fadeInWelcome 0.5s ease-out;
    }

    .welcome-inner {
      text-align: center;
      padding: 2rem;
      animation: scaleUpGold 0.8s cubic-bezier(0.25, 0.46, 0.45, 0.94);
    }

    .welcome-logo {
      font-size: 8rem;
      filter: drop-shadow(0 0 70px #f0a500) drop-shadow(0 0 30px #ff8c00);
      animation: floatSkull 3s infinite alternate ease-in-out;
      margin-bottom: 1.2rem;
      line-height: 1;
    }

    .welcome-heading {
      font-size: clamp(3rem, 12vw, 5.5rem);
      font-weight: 900;
      letter-spacing: 5px;
      text-transform: uppercase;
      background: linear-gradient(180deg, #ffdf00 0%, #d4af37 30%, #b8860b 60%, #ffd700 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      filter: drop-shadow(0 10px 20px black);
      text-shadow: 0 0 60px #b8860b, 0 0 100px #ff8c00;
      line-height: 1.1;
      margin-bottom: 1rem;
    }

    .welcome-studio {
      font-size: 2.5rem;
      font-weight: 800;
      letter-spacing: 8px;
      color: #ffcc80;
      text-shadow: 0 0 40px #ff6f00, 0 0 70px #bf360c;
      animation: shimmerGold 2s infinite;
      margin-top: 0.3rem;
    }

    .welcome-timer-bar {
      margin-top: 2.8rem;
      width: 160px;
      height: 6px;
      background: #1f1f1f;
      border-radius: 30px;
      overflow: hidden;
      margin-left: auto;
      margin-right: auto;
      box-shadow: 0 0 30px #ffb300;
    }

    .timer-fill {
      width: 0%;
      height: 100%;
      background: linear-gradient(90deg, #ffd966, #ff8c00, #f9d423);
      border-radius: 30px;
      box-shadow: 0 0 20px #ffaa00;
      transition: width 0.1s linear;
    }

    @keyframes fadeInWelcome {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    @keyframes scaleUpGold {
      0% { transform: scale(0.85); opacity: 0; filter: blur(8px); }
      100% { transform: scale(1); opacity: 1; filter: blur(0); }
    }

    @keyframes floatSkull {
      0% { transform: translateY(0px); }
      100% { transform: translateY(-14px); }
    }

    @keyframes shimmerGold {
      0%, 100% { opacity: 0.85; text-shadow: 0 0 30px #ff8c00; }
      50% { opacity: 1; text-shadow: 0 0 70px #ffa500, 0 0 100px #ff4500; }
    }

    .popup-overlay {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.92);
      backdrop-filter: blur(16px);
      display: flex;
      align-items: center;
      justify-content: center;
      z-index: 999;
      animation: fadeIn 0.35s ease;
    }

    .popup-card {
      background: #0c0e14;
      border: 2px solid #f0b90b;
      border-radius: 3.5rem;
      padding: 2.5rem 2rem;
      max-width: 370px;
      width: 85%;
      text-align: center;
      box-shadow: 0 0 80px #f0b90b77, 0 20px 45px black;
      animation: popBounce 0.5s cubic-bezier(0.34, 1.56, 0.64, 1);
    }

    .skeleton-icon {
      font-size: 6rem;
      filter: drop-shadow(0 0 35px #ffaa00);
    }

    .popup-title {
      font-size: 3rem;
      font-weight: 900;
      color: #ffd966;
      text-shadow: 0 0 25px #f0a500;
      margin: 0.4rem 0 1.2rem;
    }

    .popup-btn, .youtube-btn {
      background: #cc0000;
      color: white;
      font-weight: 800;
      font-size: 1.4rem;
      padding: 1rem 1.8rem;
      border-radius: 3rem;
      border: none;
      cursor: pointer;
      width: 100%;
      box-shadow: 0 0 35px #ff0000aa;
      margin: 1.2rem 0 0.5rem;
      text-transform: uppercase;
      letter-spacing: 1px;
      transition: all 0.2s;
    }

    .popup-btn:hover, .youtube-btn:hover {
      background: #e60000;
      box-shadow: 0 0 50px #ff4444;
    }

    .diamond-btn {
      background: linear-gradient(135deg, #f9d423, #f83600);
      font-weight: 900;
      border: none;
      padding: 1rem;
      border-radius: 3rem;
      width: 100%;
      cursor: pointer;
      font-size: 1.4rem;
      letter-spacing: 1px;
      box-shadow: 0 10px 30px rgba(245, 158, 11, 0.7);
      transition: 0.2s;
      text-transform: uppercase;
    }

    .diamond-btn:disabled {
      opacity: 0.6;
      filter: grayscale(0.5);
      pointer-events: none;
    }

    .wallpaper-btn {
      background: linear-gradient(135deg, #6a11cb, #2575fc);
      font-weight: 900;
      border: none;
      padding: 1rem;
      border-radius: 3rem;
      width: 100%;
      cursor: pointer;
      font-size: 1.4rem;
      letter-spacing: 1px;
      box-shadow: 0 10px 30px rgba(37, 117, 252, 0.7);
      transition: 0.2s;
      text-transform: uppercase;
      color: white;
      margin-top: 1rem;
    }

    .wallpaper-btn:hover {
      box-shadow: 0 15px 40px rgba(37, 117, 252, 0.9);
      transform: scale(1.02);
    }

    .hidden {
      display: none !important;
    }

    .main-container {
      position: relative;
      z-index: 10;
      width: 100%;
      max-width: 500px;
      background: rgba(10, 10, 17, 0.85);
      backdrop-filter: blur(24px);
      -webkit-backdrop-filter: blur(24px);
      border: 1.5px solid rgba(212, 175, 55, 0.55);
      border-radius: 3rem;
      padding: 2.2rem 1.8rem;
      box-shadow: 0 30px 60px black, 0 0 0 2px rgba(255, 200, 0, 0.35);
      display: flex;
      flex-direction: column;
      align-items: center;
      max-height: 90vh;
      overflow-y: auto;
    }

    /* AK47 Gun Logo */
    .channel-logo-container {
      width: 100%;
      display: flex;
      flex-direction: column;
      align-items: center;
      margin-bottom: 1rem;
    }

    .channel-logo {
      width: 100px;
      height: 100px;
      border-radius: 50%;
      border: 3px solid #f0b90b;
      box-shadow: 0 0 30px rgba(240, 185, 11, 0.7), 0 0 60px rgba(255, 0, 0, 0.4);
      object-fit: cover;
      background: #1a1d28;
      animation: logoGlow 2s infinite alternate;
    }

    @keyframes logoGlow {
      0% { box-shadow: 0 0 30px rgba(240, 185, 11, 0.7), 0 0 60px rgba(255, 0, 0, 0.4); }
      100% { box-shadow: 0 0 50px rgba(240, 185, 11, 1), 0 0 80px rgba(255, 0, 0, 0.7); }
    }

    .channel-name-logo {
      color: #ffd966;
      font-size: 1.8rem;
      font-weight: 900;
      margin-top: 0.5rem;
      letter-spacing: 2px;
      text-shadow: 0 0 20px #f0a500;
    }

    /* Auncle Gamer AD Banner */
    .ad-banner {
      width: 100%;
      background: linear-gradient(135deg, #1a0a00, #2d1a00, #1a0a00);
      border: 2px solid #f0b90b;
      border-radius: 1.5rem;
      padding: 1rem;
      margin: 0.8rem 0;
      text-align: center;
      position: relative;
      overflow: hidden;
      box-shadow: 0 0 30px rgba(240, 185, 11, 0.4);
    }

    .ad-banner::before {
      content: '';
      position: absolute;
      top: -50%;
      left: -50%;
      width: 200%;
      height: 200%;
      background: linear-gradient(45deg, transparent 40%, rgba(255,215,0,0.1) 50%, transparent 60%);
      animation: shine 3s infinite;
    }

    @keyframes shine {
      0% { transform: translateX(-100%) rotate(45deg); }
      100% { transform: translateX(100%) rotate(45deg); }
    }

    .ad-title {
      color: #ffd966;
      font-size: 1.5rem;
      font-weight: 900;
      letter-spacing: 3px;
      text-shadow: 0 0 20px #f0a500;
      position: relative;
      z-index: 1;
    }

    .ad-subtitle {
      color: #ffaa00;
      font-size: 1rem;
      font-weight: 700;
      margin-top: 0.3rem;
      position: relative;
      z-index: 1;
    }

    .ad-diamonds {
      font-size: 2rem;
      margin: 0.3rem 0;
      position: relative;
      z-index: 1;
      animation: bounce 1s infinite;
    }

    @keyframes bounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }

    .ad-btn {
      background: #cc0000;
      color: white;
      border: none;
      padding: 0.6rem 1.5rem;
      border-radius: 2rem;
      font-weight: 800;
      font-size: 1rem;
      cursor: pointer;
      margin-top: 0.5rem;
      position: relative;
      z-index: 1;
      box-shadow: 0 0 20px rgba(255,0,0,0.6);
      transition: 0.2s;
    }

    .ad-btn:hover {
      background: #ff0000;
      box-shadow: 0 0 35px rgba(255,0,0,0.9);
    }

    .uid-label {
      color: #ffd966;
      font-weight: 700;
      font-size: 1.2rem;
      margin: 0.5rem 0 0.2rem;
      letter-spacing: 0.5px;
      text-align: center;
    }

    .uid-input {
      width: 100%;
      padding: 1.1rem 1.4rem;
      border-radius: 3rem;
      border: 2px solid #f0b90b;
      background: #0b0d14;
      color: #fff;
      font-size: 1.2rem;
      font-weight: 600;
      text-align: center;
      letter-spacing: 1px;
      outline: none;
      margin: 0.8rem 0 1.4rem;
      transition: 0.2s;
      box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.7);
    }

    .uid-input:focus {
      border-color: #ffd966;
      box-shadow: 0 0 25px #f0b90b, inset 0 0 5px black;
    }

    .success-message {
      background: #1a3329;
      border-left: 8px solid #00e676;
      padding: 1.2rem 1.2rem;
      border-radius: 2rem;
      font-weight: 700;
      font-size: 1.3rem;
      margin-top: 1.2rem;
      color: #c6ffd9;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 0.5rem;
      box-shadow: 0 0 25px #00c853;
      animation: glowPulse 1.8s infinite;
      width: 100%;
    }

    /* Wallpaper Gallery Styles */
    .wallpaper-gallery {
      width: 100%;
      margin-top: 1.5rem;
      display: none;
    }

    .wallpaper-gallery.show {
      display: block;
    }

    .gallery-title {
      color: #ffd966;
      font-size: 1.5rem;
      font-weight: 800;
      text-align: center;
      margin-bottom: 1rem;
      text-shadow: 0 0 20px #f0a500;
    }

    .wallpaper-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1rem;
      width: 100%;
    }

    .wallpaper-card {
      background: #1a1d28;
      border-radius: 1.5rem;
      overflow: hidden;
      border: 2px solid #f0b90b55;
      cursor: pointer;
      transition: all 0.3s;
      position: relative;
    }

    .wallpaper-card:hover {
      border-color: #f0b90b;
      box-shadow: 0 0 30px rgba(240, 185, 11, 0.5);
      transform: translateY(-5px);
    }

    .wallpaper-preview {
      width: 100%;
      height: 200px;
      object-fit: cover;
      display: block;
    }

    .wallpaper-name {
      padding: 0.8rem;
      text-align: center;
      color: #ffd966;
      font-weight: 700;
      font-size: 0.9rem;
      background: #0f1119;
    }

    .download-btn {
      background: #f0b90b;
      color: #000;
      border: none;
      padding: 0.5rem 1rem;
      border-radius: 1.5rem;
      font-weight: 800;
      cursor: pointer;
      width: 100%;
      font-size: 0.8rem;
      transition: 0.2s;
    }

    .download-btn:hover {
      background: #ffd966;
    }

    /* Fullscreen wallpaper viewer */
    .wallpaper-viewer {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0,0,0,0.95);
      z-index: 3000;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
    }

    .wallpaper-viewer img {
      max-width: 95%;
      max-height: 80vh;
      border-radius: 1rem;
      border: 3px solid #f0b90b;
    }

    .close-viewer {
      position: absolute;
      top: 20px;
      right: 20px;
      background: #cc0000;
      color: white;
      border: none;
      width: 50px;
      height: 50px;
      border-radius: 50%;
      font-size: 1.5rem;
      cursor: pointer;
    }

    .viewer-download {
      background: #f0b90b;
      color: #000;
      border: none;
      padding: 1rem 2rem;
      border-radius: 2rem;
      font-weight: 800;
      font-size: 1.2rem;
      margin-top: 1rem;
      cursor: pointer;
    }

    @keyframes glowPulse {
      0% { box-shadow: 0 0 10px #00e676; }
      50% { box-shadow: 0 0 30px #00ff88; }
      100% { box-shadow: 0 0 10px #00e676; }
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    @keyframes popBounce {
      0% { transform: scale(0.7); opacity: 0; }
      80% { transform: scale(1.02); }
      100% { transform: scale(1); opacity: 1; }
    }

    .card-step {
      background: #181b24;
      border-radius: 2rem;
      padding: 1.4rem;
      width: 100%;
      margin: 0.8rem 0;
      text-align: center;
    }
  </style>
</head>
<body>
<div class="premium-bg"></div>
<div class="gold-dust"></div>

<!-- ========== FULLSCREEN WELCOME (5 सेकंड) ========== -->
<div id="welcomeScreen" class="welcome-overlay">
  <div class="welcome-inner">
    <div class="welcome-logo">🔫💀</div>
    <h1 class="welcome-heading">Auncle<br>Gamer</h1>
    <div class="welcome-studio">✦ STUDIO ✦</div>
    <div class="welcome-timer-bar">
      <div id="timerFill" class="timer-fill" style="width: 0%;"></div>
    </div>
  </div>
</div>

<!-- SKELETON POPUP -->
<div id="skeletonPopup" class="popup-overlay hidden">
  <div class="popup-card">
    <div class="skeleton-icon">🔫💀</div>
    <div class="popup-title">AUNCLE<br>GAMER</div>
    <div style="color:#ddd; font-weight:bold; font-size:1.2rem; margin:1rem 0;">
      YouTube पर <strong>@Auncle-2</strong> सब्सक्राइब करो!
    </div>
    <button id="popupSubscribeBtn" class="popup-btn">▶️ SUBSCRIBE NOW</button>
    <div style="color:#ffae42; margin-top:0.8rem;">फ्री डायमंड पाने के लिए</div>
  </div>
</div>

<!-- MAIN WEBSITE -->
<div id="mainWebsite" class="main-container hidden">
  
  <!-- 🔫 YouTube Channel Logo - AK47 Gun -->
  <div class="channel-logo-container">
    <img src="https://cdn-icons-png.flaticon.com/512/1033/1033332.png" 
         alt="AK47 Gun Logo" 
         class="channel-logo"
         onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
    <div style="display:none; width:100px; height:100px; border-radius:50%; border:3px solid #f0b90b; background:#1a1d28; align-items:center; justify-content:center; font-size:3rem; box-shadow: 0 0 30px rgba(240,185,11,0.7);" class="channel-logo">
      🔫
    </div>
    <div class="channel-name-logo">@Auncle-2</div>
  </div>

  <!-- 🎬 Auncle Gamer AD Banner -->
  <div class="ad-banner">
    <div class="ad-title">🔫 AUNCLE GAMER 🔫</div>
    <div class="ad-diamonds">💎💀💎</div>
    <div class="ad-subtitle">Free Fire MAX Diamonds Free!</div>
    <button class="ad-btn" onclick="window.open('https://www.youtube.com/@Auncle-2', '_blank')">▶️ SUBSCRIBE NOW</button>
  </div>

  <div class="card-step">
    <p style="color:white; font-weight:bold; font-size:1.1rem;">@Auncle-2 को YouTube पर सब्सक्राइब करें</p>
    <button id="youtubeRedirectBtn" class="youtube-btn">▶️ SUBSCRIBE @Auncle-2</button>
    <p style="color:#aaa; font-size:0.8rem; margin-top:0.3rem;">सब्सक्राइब के बाद UID डालें</p>
  </div>

  <div style="width:100%; margin:0.5rem 0;">
    <div class="uid-label">अपना Free Fire MAX UID डालें (कम से कम 11 अंक)</div>
    <input type="text" id="uidInput" class="uid-input" placeholder="जैसे: 12345678901" minlength="11" maxlength="15" inputmode="numeric" autocomplete="off">
    <button id="claimDiamondBtn" class="diamond-btn">💎 DIAMOND भेजो 💎</button>
  </div>

  <div id="successBox" class="success-message hidden">
    <span>💎✅ Diamond💎 successful to send your UID</span>
  </div>

  <!-- 🎮 3D GAMING WALLPAPERS SECTION -->
  <button id="wallpaperBtn" class="wallpaper-btn">🖼️ 3D GAMING WALLPAPERS</button>
  
  <div id="wallpaperGallery" class="wallpaper-gallery">
    <div class="gallery-title">🔥 3D GAMING WALLPAPERS 🔥</div>
    <div class="wallpaper-grid" id="wallpaperGrid"></div>
  </div>

  <div style="color:#888; font-size:0.75rem; margin-top:0.8rem;">केवल वास्तविक UID काम करेगा</div>
</div>

<!-- Wallpaper Viewer -->
<div id="wallpaperViewer" class="wallpaper-viewer hidden">
  <button class="close-viewer" onclick="closeViewer()">✕</button>
  <img id="viewerImage" src="" alt="Wallpaper">
  <a id="viewerDownload" class="viewer-download" download href="">⬇️ DOWNLOAD WALLPAPER</a>
</div>

<script>
  (function() {
    // ========== WALLPAPERS ==========
    const wallpaperData = [
      { name: "🔫 Free Fire MAX 3D", url: "https://images.unsplash.com/photo-1542751371-adc38448a05e?w=600&h=400&fit=crop", download: "https://images.unsplash.com/photo-1542751371-adc38448a05e?w=1920&h=1080&fit=crop" },
      { name: "⚔️ Gaming Warrior 3D", url: "https://images.unsplash.com/photo-1538481199705-c710c4e965fc?w=600&h=400&fit=crop", download: "https://images.unsplash.com/photo-1538481199705-c710c4e965fc?w=1920&h=1080&fit=crop" },
      { name: "💀 Skull Gaming 3D", url: "https://images.unsplash.com/photo-1550745165-9bc0b252726f?w=600&h=400&fit=crop", download: "https://images.unsplash.com/photo-1550745165-9bc0b252726f?w=1920&h=1080&fit=crop" },
      { name: "🎮 Cyberpunk Game 3D", url: "https://images.unsplash.com/photo-1552820728-8b83bb6b2cf7?w=600&h=400&fit=crop", download: "https://images.unsplash.com/photo-1552820728-8b83bb6b2cf7?w=1920&h=1080&fit=crop" },
      { name: "👑 Battle Royale 3D", url: "https://images.unsplash.com/photo-1511512578047-dfb367046420?w=600&h=400&fit=crop", download: "https://images.unsplash.com/photo-1511512578047-dfb367046420?w=1920&h=1080&fit=crop" }
    ];

    function generateWallpapers() {
      const grid = document.getElementById('wallpaperGrid');
      grid.innerHTML = '';
      wallpaperData.forEach((wall) => {
        const card = document.createElement('div');
        card.className = 'wallpaper-card';
        card.innerHTML = `
          <img src="${wall.url}" alt="${wall.name}" class="wallpaper-preview" loading="lazy">
          <div class="wallpaper-name">${wall.name}</div>
          <button class="download-btn" onclick="event.stopPropagation(); downloadWallpaper('${wall.download}', '${wall.name}')">⬇️ DOWNLOAD</button>
        `;
        card.addEventListener('click', () => openViewer(wall.url, wall.download));
        grid.appendChild(card);
      });
    }

    window.openViewer = function(imgUrl, downloadUrl) {
      document.getElementById('viewerImage').src = imgUrl;
      document.getElementById('viewerDownload').href = downloadUrl;
      document.getElementById('viewerDownload').download = 'Auncle_Gamer_3D_Wallpaper.jpg';
      document.getElementById('wallpaperViewer').classList.remove('hidden');
    };

    window.closeViewer = function() {
      document.getElementById('wallpaperViewer').classList.add('hidden');
    };

    window.downloadWallpaper = function(url, name) {
      const link = document.createElement('a');
      link.href = url;
      link.download = name.replace(/\s+/g, '_') + '_Auncle_Gamer.jpg';
      link.target = '_blank';
      document.body.appendChild(link);
      link.click();
      document.body.removeChild(link);
      alert('✅ Wallpaper download start ho raha hai!');
    };

    document.getElementById('wallpaperViewer').addEventListener('click', function(e) {
      if (e.target === this) closeViewer();
    });

    document.getElementById('wallpaperBtn').addEventListener('click', function() {
      const gallery = document.getElementById('wallpaperGallery');
      if (gallery.classList.contains('show')) {
        gallery.classList.remove('show');
        this.textContent = '🖼️ 3D GAMING WALLPAPERS';
      } else {
        gallery.classList.add('show');
        this.textContent = '⬆️ HIDE WALLPAPERS';
        if (document.getElementById('wallpaperGrid').children.length === 0) {
          generateWallpapers();
        }
      }
    });

    // ========== WEBSITE LOGIC ==========
    const welcomeScreen = document.getElementById('welcomeScreen');
    const skeletonPopup = document.getElementById('skeletonPopup');
    const mainWebsite = document.getElementById('mainWebsite');
    const timerFill = document.getElementById('timerFill');
    
    const WELCOME_DURATION = 5000;
    const startTime = Date.now();
    
    const timerInterval = setInterval(() => {
      const elapsed = Date.now() - startTime;
      const percent = Math.min(100, (elapsed / WELCOME_DURATION) * 100);
      if (timerFill) timerFill.style.width = percent + '%';
      if (elapsed >= WELCOME_DURATION) clearInterval(timerInterval);
    }, 30);

    setTimeout(() => {
      welcomeScreen.classList.add('hidden');
      skeletonPopup.classList.remove('hidden');
      clearInterval(timerInterval);
      if (timerFill) timerFill.style.width = '100%';
    }, WELCOME_DURATION);

    document.getElementById('popupSubscribeBtn').addEventListener('click', function() {
      window.open('https://www.youtube.com/@Auncle-2', '_blank');
      localStorage.setItem('auncle_subscribed', 'true');
      skeletonPopup.classList.add('hidden');
      mainWebsite.classList.remove('hidden');
    });

    document.getElementById('youtubeRedirectBtn').addEventListener('click', function() {
      window.open('https://www.youtube.com/@Auncle-2', '_blank');
      localStorage.setItem('auncle_subscribed', 'true');
      alert('✅ YouTube पर @Auncle-2 को सब्सक्राइब करें और वापस आएं!');
    });

    const uidInput = document.getElementById('uidInput');
    const claimBtn = document.getElementById('claimDiamondBtn');
    const successBox = document.getElementById('successBox');

    uidInput.addEventListener('input', function() {
      if (!successBox.classList.contains('hidden')) successBox.classList.add('hidden');
      if (claimBtn.disabled) claimBtn.disabled = false;
    });

    claimBtn.addEventListener('click', function() {
      const subscribed = localStorage.getItem('auncle_subscribed') === 'true';
      if (!subscribed) { alert('⚠️ पहले YouTube पर @Auncle-2 को सब्सक्राइब करें!'); return; }
      
      const uid = uidInput.value.trim();
      if (uid === '') { alert('❌ कृपया अपना Free Fire MAX UID डालें।'); uidInput.focus(); return; }
      if (uid.length < 11) { alert('❌ UID कम से कम 11 अंकों का होना चाहिए।'); uidInput.focus(); return; }
      if (uid.length > 15) { alert('❌ UID 15 अंकों से अधिक नहीं हो सकता।'); uidInput.focus(); return; }
      if (!/^[0-9]+$/.test(uid)) { alert('❌ UID में केवल संख्याएं (0-9) होनी चाहिए।'); uidInput.focus(); return; }
      
      successBox.classList.remove('hidden');
      claimBtn.disabled = true;
      setTimeout(() => { claimBtn.disabled = false; }, 4000);
    });

    if (localStorage.getItem('auncle_subscribed') === 'true') {
      setTimeout(() => {
        welcomeScreen.classList.add('hidden');
        skeletonPopup.classList.add('hidden');
        mainWebsite.classList.remove('hidden');
      }, WELCOME_DURATION);
    }

    console.log('🔫 AUNCLE GAMER STUDIO 💎');
    console.log('🖼️ 3D Gaming Wallpapers Ready!');
  })();
</script>
</body>
</html>
