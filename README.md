# Mercy
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
  <title>Mercy, will you be my girlfriend? 💖</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      user-select: none; /* prevents accidental text selection on buttons */
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

    /* Floating hearts, roses & sparkles background */
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
      transition: all 0.3s ease;
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

    /* romantic header */
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
      padding: 0.2rem 1.5rem;
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
      transition: 0.2s;
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

    /* footer note */
    .footer-note {
      margin-top: 2rem;
      font-size: 0.9rem;
      color: #cc7b99;
      border-top: 1px dashed #ffcddb;
      padding-top: 1.3rem;
      display: flex;
      justify-content: center;
      gap: 18px;
      flex-wrap: wrap;
    }

    .footer-note span {
      font-size: 1rem;
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
      box-shadow: 0 30px 45px rgba(0, 0, 0, 0.3);
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

    .modal-content p {
      font-size: 1.2rem;
      margin: 0.7rem 0;
      color: #5a2e3e;
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
      transition: all 0.2s;
    }

    .close-modal:hover {
      background: #b32c6b;
      transform: scale(0.96);
    }

    /* sparkle animation */
    @keyframes sparklePulse {
      0% { text-shadow: 0 0 0 #ffb7c5; }
      100% { text-shadow: 0 0 12px #ff80a5, 0 0 5px #ffb347; }
    }

    /* responsive */
    @media (max-width: 550px) {
      .proposal-card {
        padding: 1.5rem;
      }
      h1 {
        font-size: 2rem;
      }
      .question {
        font-size: 1.6rem;
      }
      .btn {
        font-size: 1.3rem;
        padding: 0.6rem 1.3rem;
      }
      .icon-bounce {
        font-size: 4rem;
      }
      .mercy-name {
        font-size: 1.8rem;
      }
    }
  </style>
</head>
<body>

<div class="floating-bg" id="floatingBg"></div>

<div class="proposal-card">
  <div class="icon-bounce">🌸💖👸🏽🌸</div>
  <h1>To my sweet <span class="mercy-name">Mercy</span> 🌹</h1>
  <div class="sweet-message">Every heartbeat whispers your name, Mercy 💗✨</div>
  <div class="question">💍 Mercy, will you be my girlfriend? 💍</div>
  
  <div class="buttons">
    <button class="btn btn-yes" id="yesBtn">💘 YES! ABSOLUTELY 💘</button>
    <button class="btn btn-no" id="noBtn">😅 No... 😅</button>
  </div>
  
  <div class="footer-note">
    <span>💞 You make my world magical 💞</span>
    <span>⭐️ Mercy = My sunshine ⭐️</span>
    <span>🌹 I'm crazy about you 🌹</span>
  </div>
</div>

<!-- Acceptance modal with Mercy's name -->
<div id="proposalModal" class="modal">
  <div class="modal-content">
    <div class="celebration-zone">🎉💖🥳💍✨🎊</div>
    <h2>MERCY SAID YES! 💕👸🏽</h2>
    <p>You've just made me the happiest person in the universe, Mercy! 🌟</p>
    <p>I promise to cherish you, make you smile, and love you more every single day. 💗</p>
    <p><strong>🌸 Officially my girlfriend — my Mercy 🌸</strong></p>
    <button class="close-modal" id="closeModalBtn">💋 To forever with you 💋</button>
  </div>
</div>

<script>
  (function() {
    // ---------- floating hearts + cute icons (including Mercy themed) ----------
    const floatContainer = document.getElementById('floatingBg');
    const FLOATING_ITEMS = ['❤️', '💖', '💗', '🌸', '🌼', '💫', '✨', '💘', '💕', '🌺', '🦋', '🌹', '👸🏽', '💍', '🌟'];
    
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
    
    for(let i = 0; i < 45; i++) {
      setTimeout(() => createFloatingItem(), i * 170);
    }
    setInterval(createFloatingItem, 1600);
    
    // ---------- elements ----------
    const yesButton = document.getElementById('yesBtn');
    const noButton = document.getElementById('noBtn');
    const modal = document.getElementById('proposalModal');
    const closeModalBtn = document.getElementById('closeModalBtn');
    
    // Celebration: confetti + modal + floating burst (personalized for Mercy)
    function celebrateYes() {
      modal.classList.add('active');
      
      // confetti library check + burst
      if (typeof confetti === 'function') {
        confetti({ particleCount: 250, spread: 100, origin: { y: 0.6 }, colors: ['#e84393', '#ffb7c5', '#ff6b9d', '#f7c0cb', '#ff9fbc'] });
        confetti({ particleCount: 180, spread: 130, origin: { y: 0.3, x: 0.2 }, startVelocity: 18 });
        confetti({ particleCount: 180, spread: 130, origin: { y: 0.4, x: 0.8 }, startVelocity: 18 });
        setTimeout(() => {
          confetti({ particleCount: 500, spread: 80, origin: { y: 0.5 }, startVelocity: 22, colors: ['#ffd966', '#e84393', '#f8c291', '#ffb3c6', '#ff85a1'] });
        }, 180);
        setTimeout(() => {
          confetti({ particleCount: 350, spread: 120, origin: { y: 0.7 }, startVelocity: 16 });
        }, 450);
      } else {
        // fallback extra floating hearts
        for (let i=0; i<60; i++) setTimeout(() => createFloatingItem(), i*30);
      }
      
      // big burst of hearts and Mercy-themed elements all over screen
      const bigSymbols = ['💖', '💘', '💗', '🌸', '🎀', '💍', '👸🏽', '🌹', '✨', '💕'];
      for (let i=0; i<30; i++) {
        const burstHeart = document.createElement('div');
        burstHeart.style.position = 'fixed';
        burstHeart.style.fontSize = (Math.random() * 45 + 28) + 'px';
        burstHeart.style.left = Math.random() * 100 + '%';
        burstHeart.style.top = Math.random() * 80 + 10 + '%';
        burstHeart.style.pointerEvents = 'none';
        burstHeart.style.zIndex = '999';
        burstHeart.style.opacity = '0.9';
        burstHeart.style.animation = 'floatUp 1.5s ease-out forwards';
        burstHeart.innerHTML = bigSymbols[Math.floor(Math.random() * bigSymbols.length)];
        document.body.appendChild(burstHeart);
        setTimeout(() => burstHeart.remove(), 1600);
      }
      
      // Extra personalized floating "Mercy" hearts
      for (let m=0; m<15; m++) {
        const mercyHeart = document.createElement('div');
        mercyHeart.style.position = 'fixed';
        mercyHeart.style.fontSize = (Math.random() * 30 + 24) + 'px';
        mercyHeart.style.left = Math.random() * 100 + '%';
        mercyHeart.style.top = Math.random() * 90 + '%';
        mercyHeart.style.pointerEvents = 'none';
        mercyHeart.style.zIndex = '1000';
        mercyHeart.style.opacity = '0.85';
        mercyHeart.style.animation = 'floatUp 2s ease-in-out forwards';
        mercyHeart.innerHTML = '💖 Mercy 💖';
        mercyHeart.style.fontWeight = 'bold';
        mercyHeart.style.fontFamily = "'Dancing Script', cursive";
        mercyHeart.style.color = '#e84393';
        mercyHeart.style.textShadow = '0 0 5px white';
        document.body.appendChild(mercyHeart);
        setTimeout(() => mercyHeart.remove(), 2100);
      }
    }
    
    // ----- NO button playful "run away" logic with romantic twist for Mercy-----
    let dodgeAttempts = 0;
    
    // helper to get random position inside buttons container
    function getRandomPositionInsideContainer(btn, container) {
      if (!container) return { x: 10, y: 10 };
      const containerRect = container.getBoundingClientRect();
      const btnRect = btn.getBoundingClientRect();
      const maxX = containerRect.width - btnRect.width - 15;
      const maxY = containerRect.height - btnRect.height - 15;
      let randX = Math.max(8, Math.random() * maxX);
      let randY = Math.max(8, Math.random() * maxY);
      // Avoid overlapping too much with yes button area
      const yesBtn = document.getElementById('yesBtn');
      if (yesBtn) {
        const yesRect = yesBtn.getBoundingClientRect();
        const relativeYesX = yesRect.left - containerRect.left;
        const relativeYesY = yesRect.top - containerRect.top;
        const dx = randX - relativeYesX;
        const dy = randY - relativeYesY;
        if (Math.hypot(dx, dy) < 70 && maxX > 100) {
          randX = (randX + 70) % maxX;
          randY = (randY + 50) % maxY;
        }
      }
      return { x: Math.min(maxX - 5, Math.max(5, randX)), y: Math.min(maxY - 5, Math.max(5, randY)) };
    }
    
    function moveNoButtonAway() {
      const container = document.querySelector('.buttons');
      if (!container) return;
      const btn = noButton;
      // change to absolute if not already
      if (window.getComputedStyle(btn).position !== 'absolute') {
        btn.style.position = 'absolute';
        container.style.position = 'relative';
        container.style.minHeight = '95px';
        // set initial left/top from current offset
        const leftPos = btn.offsetLeft;
        const topPos = btn.offsetTop;
        btn.style.left = leftPos + 'px';
        btn.style.top = topPos + 'px';
        btn.style.margin = '0';
      }
      const { x, y } = getRandomPositionInsideContainer(btn, container);
      btn.style.left = x + 'px';
      btn.style.top = y + 'px';
      
      dodgeAttempts++;
      // Playful text transformation (including Mercy)
      if (dodgeAttempts === 2) {
        noButton.textContent = "🥺 Wait, Mercy? 🥺";
        noButton.style.background = "#e2b6c2";
      } else if (dodgeAttempts === 4) {
        noButton.textContent = "💞 I love you... maybe YES? 💞";
        noButton.style.background = "#ffb7c5";
        noButton.style.color = "#a1345a";
      } else if (dodgeAttempts === 6) {
        noButton.textContent = "💘 YES, MERCY LOVES YOU! 💘";
        noButton.style.background = "#e84393";
        noButton.style.color = "white";
        noButton.style.border = "2px solid gold";
        // remove all dodge events and convert to yes action
        noButton.removeEventListener('click', noClickHandler);
        noButton.removeEventListener('mouseenter', moveNoButtonAway);
        noButton.removeEventListener('touchstart', touchNoHandler);
        noButton.addEventListener('click', () => celebrateYes());
        noButton.style.cursor = 'pointer';
        noButton.style.transform = 'scale(1.02)';
        noButton.style.transition = '0.2s';
      } else if (dodgeAttempts > 6) {
        // already converted, nothing else
        return;
      }
    }
    
    // Handlers for no button
    function noClickHandler(e) {
      e.preventDefault();
      if (dodgeAttempts >= 6) {
        celebrateYes();
        return;
      }
      moveNoButtonAway();
      // add cute floating message with Mercy's name
      const tempMsg = document.createElement('div');
      tempMsg.innerText = "💗 Mercy, think again? 💗";
      tempMsg.style.position = 'fixed';
      tempMsg.style.left = e.clientX + 'px';
      tempMsg.style.top = e.clientY - 40 + 'px';
      tempMsg.style.backgroundColor = '#fff0f3';
      tempMsg.style.padding = '6px 15px';
      tempMsg.style.borderRadius = '50px';
      tempMsg.style.fontSize = '0.95rem';
      tempMsg.style.fontWeight = 'bold';
      tempMsg.style.color = '#c72a74';
      tempMsg.style.boxShadow = '0 5px 15px rgba(0,0,0,0.1)';
      tempMsg.style.zIndex = '10001';
      tempMsg.style.pointerEvents = 'none';
      document.body.appendChild(tempMsg);
      setTimeout(() => tempMsg.remove(), 850);
    }
    
    function touchNoHandler(e) {
      e.preventDefault();
      if (dodgeAttempts >= 6) {
        celebrateYes();
        return;
      }
      moveNoButtonAway();
    }
    
    function mouseEnterHandler() {
      if (dodgeAttempts < 6) {
        moveNoButtonAway();
      }
    }
    
    // Attach dodge events
    noButton.addEventListener('click', noClickHandler);
    noButton.addEventListener('mouseenter', mouseEnterHandler);
    noButton.addEventListener('touchstart', touchNoHandler);
    
    // YES button event
    yesButton.addEventListener('click', () => {
      celebrateYes();
    });
    
    // Close modal logic
    closeModalBtn.addEventListener('click', () => {
      modal.classList.remove('active');
      // extra love hearts after closing modal
      for(let i=0; i<30; i++) {
        setTimeout(() => createFloatingItem(), i * 50);
      }
    });
    
    modal.addEventListener('click', (e) => {
      if (e.target === modal) {
        modal.classList.remove('active');
      }
    });
    
    // Load canvas-confetti dynamically
    if (typeof confetti !== 'function') {
      const script = document.createElement('script');
      script.src = 'https://cdn.jsdelivr.net/npm/canvas-confetti@1';
      script.onload = () => {
        console.log('confetti ready for Mercy');
      };
      document.head.appendChild(script);
    }
    
    // extra romantic effect: heartbeat on question text
    const questionEl = document.querySelector('.question');
    if (questionEl) {
      setInterval(() => {
        questionEl.style.transform = 'scale(1.02)';
        setTimeout(() => { if(questionEl) questionEl.style.transform = 'scale(1)'; }, 400);
      }, 2700);
    }
    
    // Preload a gentle sparkle on Yes button after load
    setTimeout(() => {
      if(yesButton) yesButton.style.animation = 'sparklePulse 1.2s infinite alternate';
    }, 1000);
    
    // Add a special little floating message after 2 seconds: "Mercy, you're amazing 🌸"
    setTimeout(() => {
      const lovePopup = document.createElement('div');
      lovePopup.innerText = "🌸 Mercy, you're my dream come true 🌸";
      lovePopup.style.position = 'fixed';
      lovePopup.style.bottom = '20px';
      lovePopup.style.left = '20px';
      lovePopup.style.backgroundColor = '#ffecf0';
      lovePopup.style.padding = '8px 18px';
      lovePopup.style.borderRadius = '40px';
      lovePopup.style.fontSize = '0.9rem';
      lovePopup.style.fontWeight = 'bold';
      lovePopup.style.color = '#c72a74';
      lovePopup.style.boxShadow = '0 4px 12px rgba(0,0,0,0.1)';
      lovePopup.style.zIndex = '1002';
      lovePopup.style.fontFamily = 'inherit';
      lovePopup.style.border = '1px solid #ffb7c5';
      lovePopup.style.pointerEvents = 'none';
      document.body.appendChild(lovePopup);
      setTimeout(() => lovePopup.remove(), 5000);
    }, 2200);
    
    console.log("%c💖 Mercy, the answer is YES from the bottom of my heart! 💖", "color: #e84393; font-size: 15px; font-weight: bold;");
  })();
</script>
</body>
</html>
