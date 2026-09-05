<!DOCTYPE html>
<html lang="kn-Latn">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Adbhuta Hand Magic - MediaPipe Chamatkaara</title>
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- MediaPipe Hands & Camera Utils CDN -->
  <script src="https://cdn.jsdelivr.net/npm/@mediapipe/camera_utils/camera_utils.js" crossorigin="anonymous"></script>
  <script src="https://cdn.jsdelivr.net/npm/@mediapipe/hands/hands.js" crossorigin="anonymous"></script>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Cinzel:wght@500;700;900&family=Poppins:wght@300;400;600&display=swap');

    body {
      font-family: 'Poppins', sans-serif;
      overflow: hidden;
      user-select: none;
      background-color: #030712;
    }

    .font-mystic {
      font-family: 'Cinzel', serif;
    }

    /* Magic glow mattu animations */
    .glow-magic {
      box-shadow: 0 0 25px rgba(236, 72, 153, 0.45), 0 0 50px rgba(168, 85, 247, 0.35);
    }
    .text-glow-orange {
      text-shadow: 0 0 12px rgba(249, 115, 22, 0.85), 0 0 24px rgba(234, 88, 12, 0.6);
    }
    .text-glow-blue {
      text-shadow: 0 0 12px rgba(56, 189, 248, 0.85), 0 0 24px rgba(14, 165, 233, 0.6);
    }

    /* Custom Glassmorphism panel */
    .glass-box {
      background: rgba(15, 23, 42, 0.72);
      backdrop-filter: blur(14px);
      border: 1px solid rgba(255, 255, 255, 0.12);
    }

    /* Video feed mirror */
    #webcam {
      transform: scaleX(-1);
    }
  </style>
</head>
<body class="relative w-screen h-screen bg-black text-white">

  <!-- Main Chamatkaara Canvas (Ellavoo illi render aaguthe) -->
  <canvas id="magicCanvas" class="absolute inset-0 w-full h-full z-10 pointer-events-auto"></canvas>

  <!-- Invisible mirror webcam feed for processing -->
  <video id="webcam" class="hidden" autoplay playsinline muted></video>

  <!-- Melina Title Bar & Status -->
  <header class="absolute top-0 left-0 right-0 z-20 p-4 sm:p-6 flex flex-wrap justify-between items-center pointer-events-none">
    <div class="pointer-events-auto flex items-center gap-3">
      <div class="w-10 h-10 rounded-full bg-gradient-to-tr from-amber-500 via-rose-500 to-indigo-600 flex items-center justify-center glow-magic animate-pulse">
        <span class="text-xl">✨</span>
      </div>
      <div>
        <h1 class="text-xl sm:text-2xl font-bold font-mystic tracking-wider text-transparent bg-clip-text bg-gradient-to-r from-amber-300 via-pink-400 to-cyan-400 text-glow-orange">
          ADBHUTA MAGIC SHOW
        </h1>
        <p class="text-xs text-indigo-300 tracking-wide">
          MediaPipe AI Kaimudre Chamatkaara
        </p>
      </div>
    </div>

    <!-- Status indicator badge -->
    <div class="pointer-events-auto flex items-center gap-2 mt-2 sm:mt-0">
      <span id="statusIndicator" class="px-3 py-1.5 rounded-full text-xs font-semibold glass-box flex items-center gap-2 text-yellow-300 border border-yellow-500/30">
        <span class="w-2 h-2 rounded-full bg-yellow-400 animate-ping"></span>
        <span id="statusText">Camera Siddhavaaguttide...</span>
      </span>
      <button id="soundToggleBtn" class="glass-box hover:bg-slate-800/80 px-3 py-1.5 rounded-full text-xs font-medium text-slate-200 transition border border-white/10 flex items-center gap-1.5">
        <span id="soundIcon">🔇</span> <span id="soundStatusText">Shabda Off</span>
      </button>
      <button id="toggleGuideBtn" class="glass-box hover:bg-slate-800/80 px-3 py-1.5 rounded-full text-xs font-medium text-slate-200 transition border border-white/10">
        ℹ️ Sahaya
      </button>
    </div>
  </header>

  <!-- Kelagina Magic Modes Bar -->
  <div class="absolute bottom-4 sm:bottom-6 left-1/2 -translate-x-1/2 z-20 w-[94%] max-w-2xl pointer-events-none">
    <div class="glass-box p-2.5 rounded-2xl flex items-center justify-around gap-1.5 sm:gap-3 pointer-events-auto shadow-2xl">
      <button class="mode-btn flex-1 py-2 px-2 rounded-xl text-xs sm:text-sm font-semibold transition-all duration-300 flex flex-col items-center gap-1 bg-gradient-to-r from-amber-600 to-orange-600 text-white shadow-lg shadow-orange-900/40" data-mode="fire">
        <span class="text-lg sm:text-xl">🔥</span>
        <span>Agni Mandala</span>
      </button>

      <button class="mode-btn flex-1 py-2 px-2 rounded-xl text-xs sm:text-sm font-semibold transition-all duration-300 flex flex-col items-center gap-1 hover:bg-slate-800/70 text-slate-300" data-mode="lightning">
        <span class="text-lg sm:text-xl">⚡</span>
        <span>Vidyut Taranga</span>
      </button>

      <button class="mode-btn flex-1 py-2 px-2 rounded-xl text-xs sm:text-sm font-semibold transition-all duration-300 flex flex-col items-center gap-1 hover:bg-slate-800/70 text-slate-300" data-mode="stars">
        <span class="text-lg sm:text-xl">✨</span>
        <span>Nakshatra Dhooli</span>
      </button>

      <button class="mode-btn flex-1 py-2 px-2 rounded-xl text-xs sm:text-sm font-semibold transition-all duration-300 flex flex-col items-center gap-1 hover:bg-slate-800/70 text-slate-300" data-mode="telekinesis">
        <span class="text-lg sm:text-xl">🔮</span>
        <span>Vastu Chamatkaara</span>
      </button>
    </div>
  </div>

  <!-- Kaimudre Sahaya Margadarshi (Gestures Guide Panel) -->
  <aside id="guidePanel" class="absolute top-20 right-4 sm:right-6 z-20 w-72 sm:w-80 glass-box rounded-2xl p-4 transition-all duration-300 shadow-2xl pointer-events-auto">
    <div class="flex justify-between items-center mb-3 pb-2 border-b border-slate-700/60">
      <h2 class="font-mystic font-bold text-sm tracking-wide text-amber-300">KAIMUDRE VIVARANE</h2>
      <button id="closeGuideBtn" class="text-slate-400 hover:text-white text-xs">✕ Muchhu</button>
    </div>

    <ul class="text-xs space-y-2.5 text-slate-300">
      <li class="flex items-start gap-2">
        <span class="text-base">🖐️</span>
        <div>
          <b class="text-amber-200">Arida Kai (Open Palm):</b>
          <p>Dr. Strange magic ring mattu energy blast shuru aaguthe.</p>
        </div>
      </li>
      <li class="flex items-start gap-2">
        <span class="text-base">✊</span>
        <div>
          <b class="text-orange-300">Mutti (Closed Fist):</b>
          <p>Shakthi charge maadi, kai arithaga doora blast aaguthe.</p>
        </div>
      </li>
      <li class="flex items-start gap-2">
        <span class="text-base">🤏</span>
        <div>
          <b class="text-cyan-300">Beralu Serisi (Pinch):</b>
          <p>Telekinesis orbs hididukolli athava nakshatra explosion madi.</p>
        </div>
      </li>
      <li class="flex items-start gap-2">
        <span class="text-base">👆</span>
        <div>
          <b class="text-purple-300">Beralu Torisi (Point):</b>
          <p>Beralina thudiyinda bijli sparks athava trail baruthe.</p>
        </div>
      </li>
      <li class="flex items-start gap-2 border-t border-slate-700/40 pt-2">
        <span class="text-base">🖱️</span>
        <div class="text-[11px] text-slate-400">
          <i>Webcam illava? Chinte beda! Screen mele mouse/touch drag madi chamatkaara nodi!</i>
        </div>
      </li>
    </ul>
  </aside>

  <!-- Live Spell Info HUD -->
  <div class="absolute bottom-24 left-6 z-20 pointer-events-none hidden sm:block">
    <div id="spellInfoHUD" class="glass-box px-4 py-2 rounded-xl text-xs flex items-center gap-3 text-slate-300 border border-white/5">
      <div id="gestureIcon" class="text-2xl animate-bounce">🖐️</div>
      <div>
        <div id="detectedGestureText" class="font-semibold text-amber-300">Kai hudukuttide...</div>
        <div id="gestureHintText" class="text-[11px] text-slate-400">Cameramunde nimma kai thodisi</div>
      </div>
    </div>
  </div>

  <!-- Custom Alert Toast (Browser alert balasadhe) -->
  <div id="toastBox" class="fixed top-5 left-1/2 -translate-x-1/2 z-50 transition-all duration-300 opacity-0 pointer-events-none">
    <div id="toastContent" class="glass-box px-5 py-2.5 rounded-full text-xs font-semibold shadow-2xl flex items-center gap-2 text-white border border-amber-500/40">
      <span>✨</span> <span id="toastMsg">Chamatkaara Shuruvaagide!</span>
    </div>
  </div>

  <script>
    // ==========================================
    // 1. SOUND EFFECTS SYNTHESIZER (Web Audio API)
    // ==========================================
    let audioCtx = null;
    let isSoundEnabled = false;

    function initAudioContext() {
      if (!audioCtx) {
        const AudioContextClass = window.AudioContext || window.webkitAudioContext;
        audioCtx = new AudioContextClass();
      }
      if (audioCtx.state === 'suspended') {
        audioCtx.resume();
      }
    }

    // Shabda tayarike: Fire whoosh
    function playFireSfx() {
      if (!isSoundEnabled || !audioCtx) return;
      try {
        const now = audioCtx.currentTime;
        const osc = audioCtx.createOscillator();
        const gain = audioCtx.createGain();
        osc.type = 'sawtooth';
        osc.frequency.setValueAtTime(140, now);
        osc.frequency.exponentialRampToValueAtTime(40, now + 0.35);
        gain.gain.setValueAtTime(0.2, now);
        gain.gain.exponentialRampToValueAtTime(0.01, now + 0.35);
        osc.connect(gain);
        gain.connect(audioCtx.destination);
        osc.start(now);
        osc.stop(now + 0.35);
      } catch (e) { }
    }

    // Shabda tayarike: Electric Zap
    function playLightningSfx() {
      if (!isSoundEnabled || !audioCtx) return;
      try {
        const now = audioCtx.currentTime;
        const osc = audioCtx.createOscillator();
        const gain = audioCtx.createGain();
        osc.type = 'triangle';
        osc.frequency.setValueAtTime(600 + Math.random() * 800, now);
        osc.frequency.exponentialRampToValueAtTime(120, now + 0.15);
        gain.gain.setValueAtTime(0.25, now);
        gain.gain.exponentialRampToValueAtTime(0.001, now + 0.15);
        osc.connect(gain);
        gain.connect(audioCtx.destination);
        osc.start(now);
        osc.stop(now + 0.15);
      } catch (e) { }
    }

    // Shabda tayarike: Magic Chime / Sparkle
    function playSparkleSfx(freq = 880) {
      if (!isSoundEnabled || !audioCtx) return;
      try {
        const now = audioCtx.currentTime;
        const osc = audioCtx.createOscillator();
        const gain = audioCtx.createGain();
        osc.type = 'sine';
        osc.frequency.setValueAtTime(freq, now);
        osc.frequency.exponentialRampToValueAtTime(freq * 1.5, now + 0.25);
        gain.gain.setValueAtTime(0.15, now);
        gain.gain.exponentialRampToValueAtTime(0.001, now + 0.25);
        osc.connect(gain);
        gain.connect(audioCtx.destination);
        osc.start(now);
        osc.stop(now + 0.25);
      } catch (e) { }
    }

    // ==========================================
    // 2. CANVAS MATTU SYSTEM SETUP
    // ==========================================
    const canvas = document.getElementById('magicCanvas');
    const ctx = canvas.getContext('2d');
    const video = document.getElementById('webcam');

    const statusIndicator = document.getElementById('statusIndicator');
    const statusText = document.getElementById('statusText');
    const soundToggleBtn = document.getElementById('soundToggleBtn');
    const soundIcon = document.getElementById('soundIcon');
    const soundStatusText = document.getElementById('soundStatusText');
    const guidePanel = document.getElementById('guidePanel');
    const toggleGuideBtn = document.getElementById('toggleGuideBtn');
    const closeGuideBtn = document.getElementById('closeGuideBtn');
    const detectedGestureText = document.getElementById('detectedGestureText');
    const gestureHintText = document.getElementById('gestureHintText');
    const gestureIcon = document.getElementById('gestureIcon');

    let currentMode = 'fire'; // 'fire', 'lightning', 'stars', 'telekinesis'
    let width = (canvas.width = window.innerWidth);
    let height = (canvas.height = window.innerHeight);

    window.addEventListener('resize', () => {
      width = canvas.width = window.innerWidth;
      height = canvas.height = window.innerHeight;
      initTelekinesisOrbs();
    });

    // Custom in-page Toast Sandesha
    function showToast(msg) {
      const toastBox = document.getElementById('toastBox');
      const toastMsg = document.getElementById('toastMsg');
      toastMsg.innerText = msg;
      toastBox.classList.remove('opacity-0', 'pointer-events-none');
      setTimeout(() => {
        toastBox.classList.add('opacity-0', 'pointer-events-none');
      }, 2600);
    }

    // ==========================================
    // 3. MAGIC SPELLS & PARTICLES ARCHITECTURE
    // ==========================================
    const particles = [];
    const ribbonPoints = [];
    const MAX_PARTICLES = 360;

    // Particle Object class
    class MagicParticle {
      constructor(x, y, vx, vy, size, color, life, decay, type = 'glow') {
        this.x = x;
        this.y = y;
        this.vx = vx;
        this.vy = vy;
        this.size = size;
        this.color = color;
        this.life = life;
        this.maxLife = life;
        this.decay = decay;
        this.type = type;
        this.rotation = Math.random() * Math.PI * 2;
        this.vRot = (Math.random() - 0.5) * 0.1;
      }

      update() {
        this.x += this.vx;
        this.y += this.vy;
        this.rotation += this.vRot;
        this.life -= this.decay;
        if (this.type === 'fire') {
          this.vy -= 0.15; // Benki mele yeruttade
          this.size *= 0.97;
        } else if (this.type === 'star') {
          this.vx *= 0.98;
          this.vy *= 0.98;
        }
      }

      draw(c) {
        if (this.life <= 0) return;
        const alpha = Math.max(0, this.life / this.maxLife);
        c.save();
        c.translate(this.x, this.y);
        c.rotate(this.rotation);
        c.globalAlpha = alpha;

        if (this.type === 'fire') {
          const grad = c.createRadialGradient(0, 0, 0, 0, 0, this.size);
          grad.addColorStop(0, '#fff3b0');
          grad.addColorStop(0.35, '#f97316');
          grad.addColorStop(1, 'rgba(220, 38, 38, 0)');
          c.fillStyle = grad;
          c.beginPath();
          c.arc(0, 0, this.size, 0, Math.PI * 2);
          c.fill();
        } else if (this.type === 'star') {
          c.fillStyle = this.color;
          c.beginPath();
          for (let i = 0; i < 5; i++) {
            c.lineTo(Math.cos(((18 + i * 72) * Math.PI) / 180) * this.size, -Math.sin(((18 + i * 72) * Math.PI) / 180) * this.size);
            c.lineTo(Math.cos(((54 + i * 72) * Math.PI) / 180) * (this.size / 2.2), -Math.sin(((54 + i * 72) * Math.PI) / 180) * (this.size / 2.2));
          }
          c.closePath();
          c.fill();
        } else {
          // Standard luminous particle
          c.fillStyle = this.color;
          c.beginPath();
          c.arc(0, 0, this.size, 0, Math.PI * 2);
          c.fill();
        }
        c.restore();
      }
    }

    // Telekinesis floating mystic orbs
    const teleOrbs = [];
    function initTelekinesisOrbs() {
      teleOrbs.length = 0;
      const orbColors = [
        '#f59e0b', '#ec4899', '#8b5cf6', '#06b6d4', '#10b981', '#ef4444'
      ];
      for (let i = 0; i < 7; i++) {
        teleOrbs.push({
          x: width * 0.2 + Math.random() * (width * 0.6),
          y: height * 0.2 + Math.random() * (height * 0.5),
          vx: (Math.random() - 0.5) * 2.5,
          vy: (Math.random() - 0.5) * 2.5,
          radius: 28 + Math.random() * 18,
          color: orbColors[i % orbColors.length],
          glowAngle: Math.random() * Math.PI * 2,
          isGrabbed: false,
          runes: ['᚛', 'ᚚ', 'ᚐ', 'ᚌ', 'ᚙ', '᚜'][i % 6]
        });
      }
    }
    initTelekinesisOrbs();

    // Dr. Strange Magic Circle (Agni Mandala) draw maduvudu
    let runeRotation = 0;
    function drawMysticMandala(c, x, y, scale = 1, intensity = 1) {
      c.save();
      c.translate(x, y);
      c.scale(scale, scale);

      // Outer glowing fire rings
      c.strokeStyle = `rgba(251, 146, 60, ${0.75 * intensity})`;
      c.lineWidth = 3;
      c.beginPath();
      c.arc(0, 0, 80, 0, Math.PI * 2);
      c.stroke();

      c.strokeStyle = `rgba(245, 158, 11, ${0.9 * intensity})`;
      c.lineWidth = 1.5;
      c.beginPath();
      c.arc(0, 0, 70, 0, Math.PI * 2);
      c.stroke();

      // Rotating Rune Rings
      c.save();
      c.rotate(runeRotation);
      c.strokeStyle = `rgba(234, 88, 12, ${0.85 * intensity})`;
      c.lineWidth = 2;

      // Draw Squares / Triangles
      for (let i = 0; i < 4; i++) {
        c.rotate(Math.PI / 2);
        c.strokeRect(-40, -40, 80, 80);
      }
      c.restore();

      c.save();
      c.rotate(-runeRotation * 1.5);
      // Inner mystic circle with sacred geometry
      c.beginPath();
      c.arc(0, 0, 48, 0, Math.PI * 2);
      c.stroke();

      for (let i = 0; i < 8; i++) {
        c.rotate(Math.PI / 4);
        c.beginPath();
        c.moveTo(0, 0);
        c.lineTo(48, 0);
        c.stroke();
      }
      c.restore();

      // Core Energy Core
      const coreGrad = c.createRadialGradient(0, 0, 0, 0, 0, 30);
      coreGrad.addColorStop(0, `rgba(255, 255, 255, ${0.95 * intensity})`);
      coreGrad.addColorStop(0.4, `rgba(251, 146, 60, ${0.7 * intensity})`);
      coreGrad.addColorStop(1, 'rgba(234, 88, 12, 0)');
      c.fillStyle = coreGrad;
      c.beginPath();
      c.arc(0, 0, 30, 0, Math.PI * 2);
      c.fill();

      c.restore();
    }

    // Lightning Generator (Recursive fractal discharge)
    function drawLightningArc(c, x1, y1, x2, y2, displace, depth) {
      if (depth <= 0) {
        c.beginPath();
        c.moveTo(x1, y1);
        c.lineTo(x2, y2);
        c.stroke();
        return;
      }
      const midX = (x1 + x2) / 2 + (Math.random() - 0.5) * displace;
      const midY = (y1 + y2) / 2 + (Math.random() - 0.5) * displace;
      drawLightningArc(c, x1, y1, midX, midY, displace / 1.7, depth - 1);
      drawLightningArc(c, midX, midY, x2, y2, displace / 1.7, depth - 1);
    }

    // ==========================================
    // 4. MEDIAPIPE GESTURE TRACKING LOGIC
    // ==========================================
    let isCameraActive = false;
    let handData = null; // Landmark data

    // Mouse / Touch fallback tracker (Camera illadiruvaga sahaya)
    let pointer = {
      x: width / 2,
      y: height / 2,
      isDown: false,
      pinch: false,
      active: false
    };

    window.addEventListener('pointerdown', (e) => {
      initAudioContext();
      pointer.x = e.clientX;
      pointer.y = e.clientY;
      pointer.isDown = true;
      pointer.active = true;
    });

    window.addEventListener('pointermove', (e) => {
      pointer.x = e.clientX;
      pointer.y = e.clientY;
    });

    window.addEventListener('pointerup', () => {
      pointer.isDown = false;
    });

    // Distance calculation formula
    function dist(p1, p2) {
      const dx = p1.x - p2.x;
      const dy = p1.y - p2.y;
      return Math.hypot(dx, dy);
    }

    // MediaPipe landmark galinda kaimudre gurutisuvudu
    function interpretHandGesture(landmarks) {
      // Landmarks: 0: Wrist, 4: Thumb tip, 8: Index tip, 12: Middle tip, 16: Ring tip, 20: Pinky tip
      const wrist = landmarks[0];
      const thumbTip = landmarks[4];
      const indexTip = landmarks[8];
      const middleTip = landmarks[12];
      const ringTip = landmarks[16];
      const pinkyTip = landmarks[20];

      // Distance from wrist
      const dIndex = dist(indexTip, wrist);
      const dMiddle = dist(middleTip, wrist);
      const dRing = dist(ringTip, wrist);
      const dPinky = dist(pinkyTip, wrist);

      // Pinch check: Index tip mattu thumb tip hattira iddeya?
      const pinchDist = dist(indexTip, thumbTip);
      const isPinch = pinchDist < 0.08;

      // Fist check: Ellaa beralugalu wristge thumba hattira iddare
      const isFist = dIndex < 0.28 && dMiddle < 0.28 && dRing < 0.28 && dPinky < 0.28;

      // Open Palm check: Ellaa beralugalu dooraviddare
      const isPalmOpen = dIndex > 0.42 && dMiddle > 0.45 && dRing > 0.42 && dPinky > 0.38;

      // Pointing check: Kevala index matra mele ide
      const isPointing = dIndex > 0.4 && dMiddle < 0.35 && dRing < 0.32;

      return {
        isPinch,
        isFist,
        isPalmOpen,
        isPointing,
        pinchDist,
        palmCenter: {
          x: (landmarks[0].x + landmarks[9].x) / 2,
          y: (landmarks[0].y + landmarks[9].y) / 2
        },
        indexTip: { x: indexTip.x, y: indexTip.y },
        thumbTip: { x: thumbTip.x, y: thumbTip.y }
      };
    }

    // MediaPipe Results Callback
    function onHandResults(results) {
      if (results.multiHandLandmarks && results.multiHandLandmarks.length > 0) {
        handData = results.multiHandLandmarks;
        statusText.innerText = `Kai Gurutiside (${handData.length})`;
        statusIndicator.className = 'px-3 py-1.5 rounded-full text-xs font-semibold glass-box flex items-center gap-2 text-emerald-300 border border-emerald-500/30';
      } else {
        handData = null;
        statusText.innerText = 'Kai Hudukuttide...';
        statusIndicator.className = 'px-3 py-1.5 rounded-full text-xs font-semibold glass-box flex items-center gap-2 text-amber-300 border border-amber-500/30';
      }
    }

    // MediaPipe Hands Library Init
    async function setupMediaPipe() {
      try {
        statusText.innerText = 'AI Model Load Aaguttide...';
        const hands = new Hands({
          locateFile: (file) => `https://cdn.jsdelivr.net/npm/@mediapipe/hands/${file}`
        });

        hands.setOptions({
          maxNumHands: 2,
          modelComplexity: 1,
          minDetectionConfidence: 0.55,
          minTrackingConfidence: 0.5
        });

        hands.onResults(onHandResults);

        // Webcam video stream shuru madi
        const stream = await navigator.mediaDevices.getUserMedia({
          video: {
            width: { ideal: 640 },
            height: { ideal: 480 },
            facingMode: 'user'
          },
          audio: false
        });

        video.srcObject = stream;
        await video.play();

        const camera = new Camera(video, {
          onFrame: async () => {
            await hands.send({ image: video });
          },
          width: 640,
          height: 480
        });

        camera.start();
        isCameraActive = true;
        showToast('Camera mattu AI Siddhavaagide!');
      } catch (err) {
        console.warn('Camera shuru madalu aagilla, mouse/touch mode balsi:', err);
        statusText.innerText = 'Mouse / Touch Mode Chalu';
        statusIndicator.className = 'px-3 py-1.5 rounded-full text-xs font-semibold glass-box flex items-center gap-2 text-sky-300 border border-sky-500/30';
        showToast('Webcam illadhe Mouse/Touch moolaka kooda chamatkaara madabahudu!');
      }
    }

    // ==========================================
    // 5. MAIN ANIMATION & RENDERING LOOP
    // ==========================================
    let lastTime = performance.now();

    function magicEngineLoop() {
      requestAnimationFrame(magicEngineLoop);

      const now = performance.now();
      const dt = (now - lastTime) / 1000;
      lastTime = now;
      runeRotation += 0.025;

      // Screen Clear with trail fade
      ctx.globalCompositeOperation = 'source-over';
      ctx.fillStyle = 'rgba(3, 7, 18, 0.28)';
      ctx.fillRect(0, 0, width, height);

      // Glow blending
      ctx.globalCompositeOperation = 'lighter';

      // Hand gesture evaluation
      let handsDetected = false;

      if (handData && handData.length > 0) {
        handsDetected = true;

        handData.forEach((landmarks, hIdx) => {
          const gesture = interpretHandGesture(landmarks);

          // Mirror X coordinates since camera is facing user
          const palmX = (1 - gesture.palmCenter.x) * width;
          const palmY = gesture.palmCenter.y * height;
          const idxX = (1 - gesture.indexTip.x) * width;
          const idxY = gesture.indexTip.y * height;
          const thmX = (1 - gesture.thumbTip.x) * width;
          const thmY = gesture.thumbTip.y * height;

          // HUD text update
          if (hIdx === 0) {
            if (gesture.isPalmOpen) {
              detectedGestureText.innerText = 'Arida Kai (Open Palm)';
              gestureHintText.innerText = 'Agni Shakthi mattu Mandala jaagrutavagide';
              gestureIcon.innerText = '🖐️';
            } else if (gesture.isFist) {
              detectedGestureText.innerText = 'Mutti (Fist)';
              gestureHintText.innerText = 'Shakthi sangraha aaguttide... Bisi blast madalu beralu tegeyiri!';
              gestureIcon.innerText = '✊';
            } else if (gesture.isPinch) {
              detectedGestureText.innerText = 'Beralu Serisi (Pinch)';
              gestureHintText.innerText = 'Magic aakarshane chalu';
              gestureIcon.innerText = '🤏';
            } else if (gesture.isPointing) {
              detectedGestureText.innerText = 'Beralu Torisi (Point)';
              gestureHintText.innerText = 'Targeting spell ready';
              gestureIcon.innerText = '👆';
            }
          }

          // Execute current spell based on active mode
          executeSpell(currentMode, {
            palmX, palmY, idxX, idxY, thmX, thmY, gesture
          });
        });
      }

      // If no hands detected, check mouse / touch interaction fallback
      if (!handsDetected) {
        if (pointer.active) {
          const simulatedGesture = {
            isPalmOpen: !pointer.isDown,
            isFist: pointer.isDown,
            isPinch: false,
            isPointing: true,
            palmCenter: { x: pointer.x, y: pointer.y },
            indexTip: { x: pointer.x, y: pointer.y }
          };

          detectedGestureText.innerText = pointer.isDown ? 'Touch / Click (Mutti)' : 'Touch Move (Arida Kai)';
          gestureHintText.innerText = 'Mouse inda chamatkaara nadeyuttide';
          gestureIcon.innerText = pointer.isDown ? '✊' : '🖐️';

          executeSpell(currentMode, {
            palmX: pointer.x,
            palmY: pointer.y,
            idxX: pointer.x,
            idxY: pointer.y,
            thmX: pointer.x - 20,
            thmY: pointer.y,
            gesture: simulatedGesture
          });
        }
      }

      // Update & Render All Floating Particles
      for (let i = particles.length - 1; i >= 0; i--) {
        const p = particles[i];
        p.update();
        p.draw(ctx);
        if (p.life <= 0) {
          particles.splice(i, 1);
        }
      }

      // Limit array explosion
      if (particles.length > MAX_PARTICLES) {
        particles.splice(0, particles.length - MAX_PARTICLES);
      }

      // If mode is telekinesis, update orbs simulation
      if (currentMode === 'telekinesis') {
        renderTelekinesisSystem(ctx);
      }
    }

    // ==========================================
    // 6. SPELL EXECUTION ENGINE
    // ==========================================
    function executeSpell(mode, h) {
      const { palmX, palmY, idxX, idxY, thmX, thmY, gesture } = h;

      switch (mode) {
        case 'fire':
          // 1. Agni Mandala (Dr. Strange Style Ring)
          if (gesture.isPalmOpen) {
            drawMysticMandala(ctx, palmX, palmY, 1.25, 1.0);
            if (Math.random() < 0.45) {
              playFireSfx();
            }

            // Spawn fire spark particles
            for (let i = 0; i < 4; i++) {
              const ang = Math.random() * Math.PI * 2;
              const spd = 2 + Math.random() * 4;
              particles.push(
                new MagicParticle(
                  palmX + Math.cos(ang) * 60,
                  palmY + Math.sin(ang) * 60,
                  Math.cos(ang) * spd,
                  Math.sin(ang) * spd,
                  8 + Math.random() * 12,
                  '#f97316',
                  1.0,
                  0.035,
                  'fire'
                )
              );
            }
          } else if (gesture.isFist) {
            // Imploding charge sphere
            drawMysticMandala(ctx, palmX, palmY, 0.45, 1.5);
            for (let i = 0; i < 3; i++) {
              const ang = Math.random() * Math.PI * 2;
              const dist = 70 + Math.random() * 40;
              particles.push(
                new MagicParticle(
                  palmX + Math.cos(ang) * dist,
                  palmY + Math.sin(ang) * dist,
                  -Math.cos(ang) * 4,
                  -Math.sin(ang) * 4,
                  5 + Math.random() * 5,
                  '#fbbf24',
                  0.7,
                  0.04,
                  'fire'
                )
              );
            }
          } else {
            // Standard small palm aura
            drawMysticMandala(ctx, palmX, palmY, 0.7, 0.5);
          }
          break;

        case 'lightning':
          // 2. Vidyut Taranga (Lightning Arcs)
          ctx.strokeStyle = '#38bdf8';
          ctx.lineWidth = 3.5;
          ctx.shadowColor = '#0284c7';
          ctx.shadowBlur = 18;

          // Lightning between index and thumb or palm
          drawLightningArc(ctx, idxX, idxY, thmX, thmY, 35, 4);

          if (gesture.isPointing || gesture.isPalmOpen) {
            // Shoot bolts outward to corners/edges
            const targetX = idxX + (Math.random() - 0.5) * 400;
            const targetY = idxY - 200 - Math.random() * 200;
            ctx.strokeStyle = '#a855f7';
            ctx.lineWidth = 2.5;
            drawLightningArc(ctx, idxX, idxY, targetX, targetY, 45, 5);

            if (Math.random() < 0.25) {
              playLightningSfx();
            }

            // Glow Sparks at fingertip
            for (let i = 0; i < 3; i++) {
              particles.push(
                new MagicParticle(
                  idxX,
                  idxY,
                  (Math.random() - 0.5) * 8,
                  (Math.random() - 0.5) * 8,
                  4 + Math.random() * 6,
                  '#38bdf8',
                  0.5,
                  0.05,
                  'glow'
                )
              );
            }
          }
          ctx.shadowBlur = 0;
          break;

        case 'stars':
          // 3. Nakshatra Dhooli (Stardust Painter & Supernova)
          ribbonPoints.push({ x: idxX, y: idxY, life: 1.0 });
          if (ribbonPoints.length > 50) ribbonPoints.shift();

          // Draw continuous glowing stardust ribbon
          if (ribbonPoints.length > 2) {
            ctx.beginPath();
            ctx.moveTo(ribbonPoints[0].x, ribbonPoints[0].y);
            for (let i = 1; i < ribbonPoints.length; i++) {
              const pt = ribbonPoints[i];
              ctx.lineTo(pt.x, pt.y);
            }
            ctx.strokeStyle = '#ec4899';
            ctx.lineWidth = 5;
            ctx.shadowColor = '#f43f5e';
            ctx.shadowBlur = 15;
            ctx.stroke();
            ctx.shadowBlur = 0;
          }

          // Emit cosmic star particles
          for (let i = 0; i < 2; i++) {
            const hue = (now / 15 + i * 40) % 360;
            particles.push(
              new MagicParticle(
                idxX + (Math.random() - 0.5) * 16,
                idxY + (Math.random() - 0.5) * 16,
                (Math.random() - 0.5) * 3,
                (Math.random() - 0.5) * 3,
                7 + Math.random() * 8,
                `hsl(${hue}, 90%, 65%)`,
                1.2,
                0.025,
                'star'
              )
            );
          }

          if (gesture.isPinch) {
            // Supernova burst on pinch!
            for (let i = 0; i < 8; i++) {
              const ang = Math.random() * Math.PI * 2;
              const spd = 4 + Math.random() * 8;
              particles.push(
                new MagicParticle(
                  idxX,
                  idxY,
                  Math.cos(ang) * spd,
                  Math.sin(ang) * spd,
                  10 + Math.random() * 8,
                  '#fb7185',
                  1.0,
                  0.04,
                  'star'
                )
              );
            }
            playSparkleSfx(1100);
          }
          break;

        case 'telekinesis':
          // 4. Vastu Chamatkaara (Telekinetic levitation)
          teleOrbs.forEach((orb) => {
            const d = Math.hypot(idxX - orb.x, idxY - orb.y);

            // Pinch gesture grabbed orb
            if (gesture.isPinch && d < orb.radius * 2.2) {
              orb.isGrabbed = true;
              orb.x += (idxX - orb.x) * 0.3;
              orb.y += (idxY - orb.y) * 0.3;
              orb.vx = (idxX - orb.x) * 0.1;
              orb.vy = (idxY - orb.y) * 0.1;
              playSparkleSfx(750);
            } else {
              orb.isGrabbed = false;
              // Open palm pushes orbs away with psychic wave
              if (gesture.isPalmOpen && d < 180) {
                const pushAng = Math.atan2(orb.y - palmY, orb.x - palmX);
                orb.vx += Math.cos(pushAng) * 2.8;
                orb.vy += Math.sin(pushAng) * 2.8;
              }
            }
          });
          break;
      }
    }

    // Telekinesis physics simulation
    function renderTelekinesisSystem(c) {
      teleOrbs.forEach((orb) => {
        if (!orb.isGrabbed) {
          orb.x += orb.vx;
          orb.y += orb.vy;
          orb.vx *= 0.985;
          orb.vy *= 0.985;

          // Wall bounce physics
          if (orb.x < orb.radius) { orb.x = orb.radius; orb.vx *= -0.85; }
          if (orb.x > width - orb.radius) { orb.x = width - orb.radius; orb.vx *= -0.85; }
          if (orb.y < orb.radius) { orb.y = orb.radius; orb.vy *= -0.85; }
          if (orb.y > height - orb.radius) { orb.y = height - orb.radius; orb.vy *= -0.85; }
        }

        // Draw Mystic Glowing Orb
        c.save();
        c.translate(orb.x, orb.y);

        const grad = c.createRadialGradient(0, 0, 4, 0, 0, orb.radius);
        grad.addColorStop(0, '#ffffff');
        grad.addColorStop(0.5, orb.color);
        grad.addColorStop(1, 'rgba(0, 0, 0, 0.2)');

        c.fillStyle = grad;
        c.shadowColor = orb.color;
        c.shadowBlur = orb.isGrabbed ? 35 : 20;

        c.beginPath();
        c.arc(0, 0, orb.radius, 0, Math.PI * 2);
        c.fill();

        // Orb Rune symbol
        c.fillStyle = '#ffffff';
        c.font = 'bold 16px serif';
        c.textAlign = 'center';
        c.textBaseline = 'middle';
        c.fillText(orb.runes, 0, 0);

        c.restore();
      });
    }

    // ==========================================
    // 7. UI EVENT LISTENERS & INTERACTION
    // ==========================================

    // Mode Selector Buttons
    const modeButtons = document.querySelectorAll('.mode-btn');
    modeButtons.forEach((btn) => {
      btn.addEventListener('click', () => {
        initAudioContext();
        modeButtons.forEach((b) => {
          b.className = 'mode-btn flex-1 py-2 px-2 rounded-xl text-xs sm:text-sm font-semibold transition-all duration-300 flex flex-col items-center gap-1 hover:bg-slate-800/70 text-slate-300';
        });

        btn.className = 'mode-btn flex-1 py-2 px-2 rounded-xl text-xs sm:text-sm font-semibold transition-all duration-300 flex flex-col items-center gap-1 bg-gradient-to-r from-amber-600 to-orange-600 text-white shadow-lg shadow-orange-900/40';
        currentMode = btn.getAttribute('data-mode');

        // Toast feedback
        const modeTitles = {
          fire: 'Agni Mandala Chamatkaara!',
          lightning: 'Vidyut Taranga Magic!',
          stars: 'Nakshatra Dhooli Mode!',
          telekinesis: 'Vastu Chamatkaara (Telekinesis)!'
        };
        showToast(modeTitles[currentMode]);
        playSparkleSfx(600);
      });
    });

    // Sound On/Off Toggle
    soundToggleBtn.addEventListener('click', () => {
      initAudioContext();
      isSoundEnabled = !isSoundEnabled;
      if (isSoundEnabled) {
        soundIcon.innerText = '🔊';
        soundStatusText.innerText = 'Shabda On';
        soundToggleBtn.classList.add('border-emerald-500/50', 'text-emerald-300');
        showToast('Chamatkaara Shabda Chaluvaagide');
        playSparkleSfx(880);
      } else {
        soundIcon.innerText = '🔇';
        soundStatusText.innerText = 'Shabda Off';
        soundToggleBtn.classList.remove('border-emerald-500/50', 'text-emerald-300');
        showToast('Shabda Nillisalaagide');
      }
    });

    // Guide Panel Toggle
    toggleGuideBtn.addEventListener('click', () => {
      guidePanel.classList.toggle('hidden');
    });
    closeGuideBtn.addEventListener('click', () => {
      guidePanel.classList.add('hidden');
    });

    // Start App on Window Load
    window.addEventListener('load', () => {
      magicEngineLoop();
      setupMediaPipe();
    });
  </script>
</body>
</html>
