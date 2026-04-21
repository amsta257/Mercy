Mercy💕💕
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
  <title>Mercy, will you be my Ride or Die? 💖🔥</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      user-select: none;
    }

    body {
      min-height: 100vh;
      background: linear-gradient(145deg, #ffb7c5 0%, #ffd9e6 40%, #ffe4f0 100%);
      font-family: 'Segoe UI', 'Poppins', 'Quicksand', system-ui, -apple-system, 'Helvetica Neue', sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 20px;
      position: relative;
      overflow-x: hidden;
    }

    /* Floating hearts background */
    .floating-bg {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 1;
      overflow: hidden;
    }

    .floating-bg i {
      position: absolute;
      font-size: 1.5rem;
      color: rgba(220, 70, 110, 0.35);
      animation: floatUp 15s infinite linear;
      bottom: -10%;
    }

    @keyframes floatUp {
      0% {
        transform: translateY(0) rotate(0deg);
        opacity: 0;
      }
      15% {
        opacity: 0.7;
      }
      85% {
        opacity: 0.6;
      }
      100% {
        transform: translateY(-120vh) rotate(360deg);
        opacity: 0;
      }
    }

    /* main card */
    .proposal-card {
      position: relative;
      z-index: 20;
      max-width: 650px;
      width: 100%;
      background: rgba(255, 251, 253, 0.98);
      backdrop-filter: blur(1px);
      border-radius: 80px 60px 85px 60px;
      box-shadow: 0 35px 55px rgba(0, 0, 0, 0.2), 0 0 0 12px rgba(255, 190, 210, 0.7);
      padding: 2rem 2rem 2.5rem;
      text-align: center;
      animation: softAppear 0.7s cubic-bezier(0.2, 0.9, 0.4, 1.1);
    }

    @keyframes softAppear {
      0% {
        transform: scale(0.92) translateY(20px);
        opacity: 0;
      }
      100% {
        transform: scale(1) translateY(0);
        opacity: 1;
      }
    }

    .icon-bounce {
      font-size: 5.2rem;
      filter: drop-shadow(2px 8px 18px rgba(0, 0, 0, 0.15));
      margin-bottom: 0.2rem;
      display: inline-block;
      animation: gentleBounce 2.5s infinite ease;
    }

    @keyframes gentleBounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-8px); }
    }

    h1 {
      font-size: 2.7rem;
      background: linear-gradient(125deg, #c0395b, #e84393, #ff70a6);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
      margin: 0.5rem 0 0.2rem;
      font-weight: 800;
      font-family: 'Dancing Script', cursive;
    }

    .sweet-message {
      font-size: 1.2rem;
      color: #b84c6e;
      background: #fff0f6;
      display: inline-block;
      padding: 0.4rem 1.5rem;
      border-radius: 60px;
      margin: 0.8rem 0 1rem;
      font-weight: 500;
      box-shadow: inset 0 1px 2px #ffe0e8, 0 4px 8px rgba(0,0,0,0.02);
    }

    .question {
      font-size: 2rem;
      font-weight: bold;
      color: #c13b6b;
      margin: 1.3rem 0 1rem;
      font-family: 'Dancing Script', cursive;
      letter-spacing: 1px;
      background: rgba(255, 235, 240, 0.8);
      display: inline-block;
      padding: 0.3rem 1.8rem;
      border-radius: 80px;
    }

    .mercy-name {
      font-size: 2.2rem;
      background: linear-gradient(120deg, #e84393, #ff9fbc);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
      display: inline-block;
      margin: 0 5px;
    }

    /* buttons container */
    .buttons {
      display: flex;
      justify-content: center;
      gap: 40px;
      flex-wrap: wrap;
      margin: 2rem 0 1rem;
      position: relative;
      min-height: 95px;
    }

    .btn {
      font-size: 1.7rem;
      font-weight: bold;
      padding: 0.8rem 2rem;
      border: none;
      border-radius: 60px;
      cursor: pointer;
      transition: all 0.2s ease;
      font-family: inherit;
      box-shadow: 0 8px 18px rgba(0, 0, 0, 0.12);
      display: inline-flex;
      align-items: center;
      gap: 12px;
    }

    .btn-yes {
      background: #e84393;
      color: white;
      border: 2px solid #ffbfcf;
    }

    .btn-yes:hover {
      background: #c72a74;
      transform: scale(1.05);
      box-shadow: 0 14px 24px rgba(232, 67, 147, 0.4);
    }

    .btn-no {
      background: #c2a5ad;
      color: #311e26;
      position: relative;
      transition: all 0.08s linear;
      border: 2px solid #fad1db;
    }

    /* music controls - minimal and elegant */
    .music-control {
      margin-top: 1rem;
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 12px;
      background: rgba(255, 235, 240, 0.8);
      backdrop-filter: blur(4px);
      padding: 8px 20px;
      border-radius: 100px;
      width: fit-content;
      margin-left: auto;
      margin-right: auto;
      border: 1px solid #ffbfcf;
    }
    
    .music-btn {
      background: #e84393;
      border: none;
      color: white;
      font-size: 1rem;
      padding: 8px 18px;
      border-radius: 40px;
      cursor: pointer;
      font-weight: bold;
      display: inline-flex;
      align-items: center;
      gap: 8px;
      transition: 0.2s;
      font-family: inherit;
    }
    
    .music-btn:hover {
      background: #c72a74;
      transform: scale(0.97);
    }
    
    .music-status {
      font-size: 0.8rem;
      color: #b84c6e;
      font-weight: 500;
    }

    /* footer note */
    .footer-note {
      margin-top: 1.8rem;
      font-size: 0.9rem;
      color: #cc7b99;
      border-top: 1px dashed #ffcddb;
      padding-top: 1.3rem;
      display: flex;
      justify-content: center;
      gap: 18px;
      flex-wrap: wrap;
    }

    /* YES celebration modal */
    .modal {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.75);
      backdrop-filter: blur(8px);
      z-index: 1000;
      display: flex;
      align-items: center;
      justify-content: center;
      opacity: 0;
      visibility: hidden;
      transition: all 0.3s ease;
    }

    .modal.active {
      opacity: 1;
      visibility: visible;
    }

    .modal-content {
      background: #fff7f9;
      max-width: 520px;
      width: 90%;
      border-radius: 55px;
      padding: 2rem 1.8rem;
      text-align: center;
      transform: scale(0.8);
      transition: transform 0.3s cubic-bezier(0.34, 1.2, 0.64, 1);
      border: 2px solid #ffb7cb;
    }

    .modal.active .modal-content {
      transform: scale(1);
    }

    .modal-content h2 {
      font-size: 2.5rem;
      color: #d43f7a;
      font-family: 'Dancing Script', cursive;
      margin-bottom: 0.5rem;
    }

    .celebration-zone {
      font-size: 3.2rem;
      letter-spacing: 12px;
      margin: 15px 0;
    }

    .close-modal {
      background: #e84393;
      border: none;
      color: white;
      font-size: 1.2rem;
      padding: 0.7rem 1.5rem;
      border-radius: 50px;
      margin-top: 20px;
      cursor: pointer;
      font-weight: bold;
    }

    @keyframes sparklePulse {
      0% { text-shadow: 0 0 0 #ffb7c5; }
      100% { text-shadow: 0 0 12px #ff80a5, 0 0 5px #ffb347; }
    }

    @media (max-width: 550px) {
      .proposal-card { padding: 1.5rem; }
      h1 { font-size: 2rem; }
      .question { font-size: 1.6rem; }
      .btn { font-size: 1.3rem; padding: 0.6rem 1.3rem; }
      .mercy-name { font-size: 1.8rem; }
      .music-btn { font-size: 0.9rem; padding: 6px 14px; }
    }
  </style>
</head>
<body>

<div class="floating-bg" id="floatingBg"></div>

<div class="proposal-card">
  <div class="icon-bounce">🌸💖👸🏽🔥</div>
  <h1>To my everything, <span class="mercy-name">Mercy</span> 🌹</h1>
  <div class="sweet-message">You're my anchor, my wild heart, my forever 💗✨</div>
  <div class="question">🔥 Mercy, will you be my RIDE OR DIE? 🔥</div>
  
  <div class="buttons">
    <button class="btn btn-yes" id="yesBtn">💘 YES! ALWAYS & FOREVER 💘</button>
    <button class="btn btn-no" id="noBtn">😅 No... 😅</button>
  </div>
  
  <!-- Music control - beautiful song that auto-plays -->
  <div class="music-control">
    <button class="music-btn" id="playMusicBtn">🎵 Our Romantic Song 🎵</button>
    <span class="music-status" id="musicStatus">♫ loading your song... ♫</span>
  </div>
  
  <div class="footer-note">
    <span>💞 Through every storm and every sunrise 💞</span>
    <span>⭐️ Mercy = My ride or die ⭐️</span>
    <span>🌹 Together forever, no matter what 🌹</span>
  </div>
</div>

<!-- Acceptance modal -->
<div id="proposalModal" class="modal">
  <div class="modal-content">
    <div class="celebration-zone">🎉💖🔥💍✨🎊</div>
    <h2>MERCY SAID YES! 💕👸🏽🔥</h2>
    <p>You've just made me the happiest person in the universe, Mercy! 🌟</p>
    <p>I promise to ride with you through every high and every low, to always have your back, and to love you more every single day. 💗</p>
    <p><strong>🔥 My Ride or Die — my Mercy 🔥</strong></p>
    <button class="close-modal" id="closeModalBtn">💋 To forever and beyond 💋</button>
  </div>
</div>

<script>
  (function() {
    // ---------- FLOATING HEARTS BACKGROUND ----------
    const floatContainer = document.getElementById('floatingBg');
    const FLOATING_ITEMS = ['❤️', '💖', '💗', '🌸', '🌼', '💫', '✨', '💘', '💕', '🌺', '🦋', '🌹', '👸🏽', '💍', '🌟', '🎵', '🎶', '🔥', '⚡'];
    
    function createFloatingItem() {
      const el = document.createElement('i');
      el.innerHTML = FLOATING_ITEMS[Math.floor(Math.random() * FLOATING_ITEMS.length)];
      const size = Math.random() * 26 + 14;
      el.style.fontSize = size + 'px';
      el.style.left = Math.random() * 100 + '%';
      el.style.opacity = Math.random() * 0.55 + 0.2;
      el.style.animationDuration = Math.random() * 13 + 8 + 's';
      el.style.animationDelay = Math.random() * 12 + 's';
      floatContainer.appendChild(el);
      setTimeout(() => { if(el && el.remove) el.remove(); }, 17000);
    }
    
    for(let i = 0; i < 45; i++) setTimeout(() => createFloatingItem(), i * 170);
    setInterval(createFloatingItem, 1600);
    
    // ---------- BEAUTIFUL SONG THAT PLAYS AUTOMATICALLY ----------
    // Using a stunning, romantic piano melody (royalty-free from Pixabay)
    // This song is soft, emotional, and perfect for a proposal
    const musicURL = 'https://cdn.pixabay.com/download/audio/2022/02/22/audio_dd3f5c3f1a.mp3?filename=romantic-love-piano-109054.mp3';
    let audio = null;
    let musicPlaying = false;
    let playAttempted = false;
    
    function initAudio() {
      if (audio) return audio;
      audio = new Audio();
      audio.loop = true;
      audio.volume = 0.5; // perfect volume - audible but gentle
      audio.src = musicURL;
      audio.preload = 'auto';
      return audio;
    }
    
    function startMusic() {
      if (!audio) initAudio();
      if (!audio) return;
      if (musicPlaying) return;
      
      const playPromise = audio.play();
      if (playPromise !== undefined) {
        playPromise.then(() => {
          musicPlaying = true;
          const statusSpan = document.getElementById('musicStatus');
          if (statusSpan) statusSpan.innerHTML = '🎶 playing softly for you 🎶';
          const playBtn = document.getElementById('playMusicBtn');
          if (playBtn) playBtn.innerHTML = '🎵 Music Playing 🎵';
        }).catch((err) => {
          console.log("Auto-play was prevented by browser:", err);
          musicPlaying = false;
          const statusSpan = document.getElementById('musicStatus');
          if (statusSpan) statusSpan.innerHTML = '🔊 tap anywhere to play our song 🔊';
        });
      }
    }
    
    function stopMusic() {
      if (audio && musicPlaying) {
        audio.pause();
        musicPlaying = false;
        const statusSpan = document.getElementById('musicStatus');
        if (statusSpan) statusSpan.innerHTML = '🎵 music paused — click to resume 🎵';
        const playBtn = document.getElementById('playMusicBtn');
        if (playBtn) playBtn.innerHTML = '🎵 Play our song 🎵';
      }
    }
    
    function toggleMusic() {
      if (!audio) initAudio();
      if (musicPlaying) stopMusic();
      else startMusic();
    }
    
    // Attach manual play button
    const playBtnElement = document.getElementById('playMusicBtn');
    if (playBtnElement) {
      playBtnElement.addEventListener('click', (e) => {
        e.preventDefault();
        toggleMusic();
      });
    }
    
    // AUTO-PLAY: attempt to play music immediately when page loads
    function attemptAutoPlay() {
      if (playAttempted) return;
      playAttempted = true;
      if (!audio) initAudio();
      startMusic();
    }
    
    // Try to autoplay right away
    attemptAutoPlay();
    
    // Fallback: modern browsers block autoplay without user interaction.
    // So we'll start music on the very first tap/click anywhere on the page if it didn't start yet.
    const globalStartMusic = function() {
      if (!musicPlaying) {
        startMusic();
      }
      // Remove listeners after first successful attempt
      document.body.removeEventListener('click', globalStartMusic);
      document.body.removeEventListener('touchstart', globalStartMusic);
    };
    
    // Add fallback listeners only if music isn't playing after 0.8 seconds
    setTimeout(() => {
      if (!musicPlaying) {
        document.body.addEventListener('click', globalStartMusic);
        document.body.addEventListener('touchstart', globalStartMusic);
      }
    }, 800);
    
    // Pre-initialize audio for faster response
    initAudio();
    
    // ----- NO BUTTON PLAYFUL "RUN AWAY" LOGIC (Ride or Die Edition)-----
    const yesButton = document.getElementById('yesBtn');
    const noButton = document.getElementById('noBtn');
    const modal = document.getElementById('proposalModal');
    const closeModalBtn = document.getElementById('closeModalBtn');
    
    let dodgeAttempts = 0;
    
    function getRandomPositionInsideContainer(btn, container) {
      if (!container) return { x: 10, y: 10 };
      const containerRect = container.getBoundingClientRect();
      const btnRect = btn.getBoundingClientRect();
      const maxX = containerRect.width - btnRect.width - 15;
      const maxY = containerRect.height - btnRect.height - 15;
      let randX = Math.max(8, Math.random() * maxX);
      let randY = Math.max(8, Math.random() * maxY);
      const yesBtn = document.getElementById('yesBtn');
      if (yesBtn) {
        const yesRect = yesBtn.getBoundingClientRect();
        const relativeYesX = yesRect.left - containerRect.left;
        const relativeYesY = yesRect.top - containerRect.top;
        if (Math.hypot(randX - relativeYesX, randY - relativeYesY) < 70 && maxX > 100) {
          randX = (randX + 70) % maxX;
          randY = (randY + 50) % maxY;
        }
      }
      return { x: Math.min(maxX - 5, Math.max(5, randX)), y: Math.min(maxY - 5, Math.max(5, randY)) };
    }
    
    function moveNoButtonAway() {
      const container = document.querySelector('.buttons');
      if (!container) return;
      if (window.getComputedStyle(noButton).position !== 'absolute') {
        noButton.style.position = 'absolute';
        container.style.position = 'relative';
        container.style.minHeight = '95px';
        noButton.style.left = noButton.offsetLeft + 'px';
        noButton.style.top = noButton.offsetTop + 'px';
        noButton.style.margin = '0';
      }
      const { x, y } = getRandomPositionInsideContainer(noButton, container);
      noButton.style.left = x + 'px';
      noButton.style.top = y + 'px';
      dodgeAttempts++;
      if (dodgeAttempts === 2) {
        noButton.textContent = "🥺 Wait, Mercy? 🥺";
        noButton.style.background = "#e2b6c2";
      } else if (dodgeAttempts === 4) {
        noButton.textContent = "💞 I love you... maybe YES? 💞";
        noButton.style.background = "#ffb7c5";
        noButton.style.color = "#a1345a";
      } else if (dodgeAttempts === 6) {
        noButton.textContent = "💘 YES! I'M YOUR RIDE OR DIE! 💘";
        noButton.style.background = "#e84393";
        noButton.style.color = "white";
        noButton.style.border = "2px solid gold";
        noButton.removeEventListener('click', noClickHandler);
        noButton.removeEventListener('mouseenter', moveNoButtonAway);
        noButton.removeEventListener('touchstart', touchNoHandler);
        noButton.addEventListener('click', () => celebrateYes());
        noButton.style.cursor = 'pointer';
      }
    }
    
    function noClickHandler(e) {
      e.preventDefault();
      if (dodgeAttempts >= 6) { celebrateYes(); return; }
      moveNoButtonAway();
      const msg = document.createElement('div');
      msg.innerText = "💗 Mercy, think again? Be my ride or die 💗";
      msg.style.position = 'fixed';
      msg.style.left = e.clientX + 'px';
      msg.style.top = e.clientY - 40 + 'px';
      msg.style.backgroundColor = '#fff0f3';
      msg.style.padding = '6px 15px';
      msg.style.borderRadius = '50px';
      msg.style.fontSize = '0.95rem';
      msg.style.fontWeight = 'bold';
      msg.style.color = '#c72a74';
      msg.style.zIndex = '10001';
      msg.style.pointerEvents = 'none';
      document.body.appendChild(msg);
      setTimeout(() => msg.remove(), 850);
    }
    
    function touchNoHandler(e) {
      e.preventDefault();
      if (dodgeAttempts >= 6) celebrateYes();
      else moveNoButtonAway();
    }
    
    noButton.addEventListener('click', noClickHandler);
    noButton.addEventListener('mouseenter', () => { if (dodgeAttempts < 6) moveNoButtonAway(); });
    noButton.addEventListener('touchstart', touchNoHandler);
    
    // ---------- CELEBRATION (with extra joy) ----------
    function celebrateYes() {
      // Ensure the romantic music is playing for the big moment
      if (!musicPlaying && audio) startMusic();
      else if (!audio) { initAudio(); startMusic(); }
      
      modal.classList.add('active');
      
      // Confetti explosion
      if (typeof confetti === 'function') {
        confetti({ particleCount: 300, spread: 110, origin: { y: 0.6 }, colors: ['#e84393', '#ffb7c5', '#ff6b6b', '#ffd966'] });
        confetti({ particleCount: 200, spread: 140, origin: { y: 0.3, x: 0.2 }, startVelocity: 20 });
        confetti({ particleCount: 200, spread: 140, origin: { y: 0.4, x: 0.8 }, startVelocity: 20 });
        setTimeout(() => confetti({ particleCount: 600, spread: 90, origin: { y: 0.5 }, colors: ['#ffd966', '#e84393', '#f8c291', '#ff85a1'] }), 180);
        setTimeout(() => confetti({ particleCount: 400, spread: 130, origin: { y: 0.7 } }), 450);
      } else {
        for (let i=0; i<80; i++) setTimeout(() => createFloatingItem(), i*30);
      }
      
      // big burst of hearts and Mercy-themed elements
      const bigSymbols = ['💖', '💘', '💗', '🌸', '🔥', '💍', '👸🏽', '🌹', '✨', '💕', '🎶', '⚡'];
      for (let i=0; i<40; i++) {
        const burst = document.createElement('div');
        burst.style.position = 'fixed';
        burst.style.fontSize = (Math.random() * 48 + 28) + 'px';
        burst.style.left = Math.random() * 100 + '%';
        burst.style.top = Math.random() * 80 + 10 + '%';
        burst.style.pointerEvents = 'none';
        burst.style.zIndex = '999';
        burst.style.opacity = '0.9';
        burst.style.animation = 'floatUp 1.5s ease-out forwards';
        burst.innerHTML = bigSymbols[Math.floor(Math.random() * bigSymbols.length)];
        document.body.appendChild(burst);
        setTimeout(() => burst.remove(), 1600);
      }
      
      // Personalized floating "Ride or Die" messages for Mercy
      const rideMessages = ['🔥 Ride or Die 🔥', '💖 Mercy + You Forever 💖', '⚡ Through It All ⚡', '👸🏽 My Ride or Die Queen 👸🏽', '🌹 Together Always 🌹'];
      for (let m=0; m<25; m++) {
        const mercyMsg = document.createElement('div');
        mercyMsg.style.position = 'fixed';
        mercyMsg.style.fontSize = (Math.random() * 30 + 22) + 'px';
        mercyMsg.style.left = Math.random() * 100 + '%';
        mercyMsg.style.top = Math.random() * 90 + '%';
        mercyMsg.style.pointerEvents = 'none';
        mercyMsg.style.zIndex = '1000';
        mercyMsg.style.opacity = '0.9';
        mercyMsg.style.animation = 'floatUp 2s ease-in-out forwards';
        mercyMsg.innerHTML = rideMessages[Math.floor(Math.random() * rideMessages.length)];
        mercyMsg.style.fontWeight = 'bold';
        mercyMsg.style.fontFamily = "'Dancing Script', cursive";
        mercyMsg.style.color = '#e84393';
        mercyMsg.style.textShadow = '0 0 5px white';
        document.body.appendChild(mercyMsg);
        setTimeout(() => mercyMsg.remove(), 2100);
      }
    }
    
    yesButton.addEventListener('click', celebrateYes);
    closeModalBtn.addEventListener('click', () => modal.classList.remove('active'));
    modal.addEventListener('click', (e) => { if (e.target === modal) modal.classList.remove('active'); });
    
    // Load canvas-confetti library
    if (typeof confetti !== 'function') {
      const script = document.createElement('script');
      script.src = 'https://cdn.jsdelivr.net/npm/canvas-confetti@1';
      script.onload = () => { console.log('🎉 Confetti ready for Mercy!'); };
      document.head.appendChild(script);
    }
    
    // Gentle pulsing animation on question text
    const questionEl = document.querySelector('.question');
    if (questionEl) {
      setInterval(() => {
        questionEl.style.transform = 'scale(1.02)';
        setTimeout(() => { if(questionEl) questionEl.style.transform = 'scale(1)'; }, 400);
      }, 2700);
    }
    
    // Sparkle effect on YES button
    setTimeout(() => { if(yesButton) yesButton.style.animation = 'sparklePulse 1.2s infinite alternate'; }, 1000);
    
    // Sweet little popup message that appears after a few seconds
    setTimeout(() => {
      const lovePopup = document.createElement('div');
      lovePopup.innerText = "🔥 Mercy, let's ride through life together 🔥";
      lovePopup.style.position = 'fixed';
      lovePopup.style.bottom = '20px';
      lovePopup.style.left = '20px';
      lovePopup.style.backgroundColor = '#ffecf0';
      lovePopup.style.padding = '10px 20px';
      lovePopup.style.borderRadius = '50px';
      lovePopup.style.fontSize = '0.9rem';
      lovePopup.style.fontWeight = 'bold';
      lovePopup.style.color = '#c72a74';
      lovePopup.style.boxShadow = '0 6px 16px rgba(0,0,0,0.1)';
      lovePopup.style.zIndex = '1002';
      lovePopup.style.border = '1px solid #ffb7c5';
      lovePopup.style.pointerEvents = 'none';
      lovePopup.style.fontFamily = 'inherit';
      document.body.appendChild(lovePopup);
      setTimeout(() => lovePopup.remove(), 6000);
    }, 2500);
    
    console.log("%c🔥 Mercy, my ride or die — beautiful music is playing just for you! 🔥", "color: #e84393; font-size: 15px; font-weight: bold;");
  })();
</script>
</body>
</html>
