<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Rock Paper Scissors</title>
  <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&family=DM+Sans:wght@400;600&display=swap" rel="stylesheet" />
  <style>
    :root {
      --bg: #0a0a0f;
      --surface: #13131a;
      --border: #2a2a3a;
      --accent: #f0e040;
      --accent2: #ff6b6b;
      --accent3: #6bffd8;
      --text: #f0eedc;
      --muted: #7a7a9a;
      --win: #6bffd8;
      --lose: #ff6b6b;
      --draw: #f0e040;
    }

    * { box-sizing: border-box; margin: 0; padding: 0; }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: 'DM Sans', sans-serif;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 2rem 1rem;
      overflow-x: hidden;
    }

    /* Scanline overlay */
    body::before {
      content: '';
      position: fixed;
      inset: 0;
      background: repeating-linear-gradient(
        0deg,
        transparent,
        transparent 2px,
        rgba(0,0,0,0.08) 2px,
        rgba(0,0,0,0.08) 4px
      );
      pointer-events: none;
      z-index: 100;
    }

    /* Grid bg */
    body::after {
      content: '';
      position: fixed;
      inset: 0;
      background-image:
        linear-gradient(rgba(240,224,64,0.03) 1px, transparent 1px),
        linear-gradient(90deg, rgba(240,224,64,0.03) 1px, transparent 1px);
      background-size: 40px 40px;
      pointer-events: none;
      z-index: 0;
    }

    .wrapper {
      position: relative;
      z-index: 1;
      width: 100%;
      max-width: 540px;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 1.5rem;
    }

    /* TITLE */
    .title {
      font-family: 'Press Start 2P', monospace;
      font-size: clamp(0.75rem, 2.5vw, 1rem);
      color: var(--accent);
      text-align: center;
      line-height: 1.8;
      text-shadow: 0 0 20px rgba(240,224,64,0.5);
      letter-spacing: 0.05em;
    }

    .title span {
      color: var(--accent3);
    }

    /* SCOREBOARD */
    .scoreboard {
      display: flex;
      gap: 1rem;
      width: 100%;
    }

    .score-box {
      flex: 1;
      background: var(--surface);
      border: 1px solid var(--border);
      border-top: 2px solid var(--accent);
      padding: 1rem;
      text-align: center;
    }

    .score-box.cpu-box {
      border-top-color: var(--accent2);
    }

    .score-label {
      font-family: 'Press Start 2P', monospace;
      font-size: 0.5rem;
      color: var(--muted);
      letter-spacing: 0.1em;
      margin-bottom: 0.5rem;
    }

    .score-num {
      font-family: 'Press Start 2P', monospace;
      font-size: 2rem;
      color: var(--text);
    }

    /* BATTLE ARENA */
    .arena {
      width: 100%;
      background: var(--surface);
      border: 1px solid var(--border);
      padding: 1.5rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 1rem;
      min-height: 140px;
      position: relative;
    }

    .arena::before {
      content: 'VS';
      font-family: 'Press Start 2P', monospace;
      font-size: 0.6rem;
      color: var(--border);
      position: absolute;
      left: 50%;
      transform: translateX(-50%);
      letter-spacing: 0.1em;
    }

    .fighter {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 0.5rem;
      flex: 1;
    }

    .fighter-label {
      font-family: 'Press Start 2P', monospace;
      font-size: 0.45rem;
      color: var(--muted);
      letter-spacing: 0.1em;
    }

    .hand-display {
      width: 80px;
      height: 80px;
      border: 1px solid var(--border);
      background: #0d0d14;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 2.8rem;
      transition: transform 0.2s;
      position: relative;
    }

    .hand-display img {
      width: 52px;
      height: 52px;
      object-fit: contain;
    }

    .hand-display.shake {
      animation: arcade-shake 0.4s ease;
    }

    .hand-display.winner {
      border-color: var(--win);
      box-shadow: 0 0 16px rgba(107,255,216,0.3);
    }

    .hand-display.loser {
      border-color: var(--lose);
      opacity: 0.5;
    }

    @keyframes arcade-shake {
      0%   { transform: translateY(0) rotate(0deg); }
      20%  { transform: translateY(-10px) rotate(-3deg); }
      40%  { transform: translateY(6px) rotate(3deg); }
      60%  { transform: translateY(-6px) rotate(-2deg); }
      80%  { transform: translateY(4px) rotate(1deg); }
      100% { transform: translateY(0) rotate(0deg); }
    }

    /* RESULT */
    .result-bar {
      width: 100%;
      background: var(--surface);
      border: 1px solid var(--border);
      padding: 0.9rem 1.25rem;
      text-align: center;
      font-family: 'Press Start 2P', monospace;
      font-size: 0.6rem;
      color: var(--muted);
      letter-spacing: 0.05em;
      line-height: 1.8;
      min-height: 56px;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .result-bar.win  { color: var(--win);  border-color: var(--win);  }
    .result-bar.lose { color: var(--lose); border-color: var(--lose); }
    .result-bar.draw { color: var(--draw); border-color: var(--draw); }

    /* CHOICES */
    .choices {
      display: flex;
      gap: 0.75rem;
      width: 100%;
    }

    .choice-btn {
      flex: 1;
      background: var(--surface);
      border: 1px solid var(--border);
      padding: 1rem 0.5rem;
      cursor: pointer;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 0.6rem;
      transition: border-color 0.15s, transform 0.15s, background 0.15s;
      color: var(--text);
    }

    .choice-btn:hover {
      border-color: var(--accent);
      background: rgba(240,224,64,0.05);
      transform: translateY(-3px);
    }

    .choice-btn:active {
      transform: scale(0.96) translateY(0);
    }

    .choice-btn img {
      width: 52px;
      height: 52px;
      object-fit: contain;
      image-rendering: pixelated;
    }

    .choice-name {
      font-family: 'Press Start 2P', monospace;
      font-size: 0.45rem;
      color: var(--muted);
      letter-spacing: 0.08em;
    }

    /* HISTORY */
    .history {
      width: 100%;
    }

    .history-title {
      font-family: 'Press Start 2P', monospace;
      font-size: 0.45rem;
      color: var(--muted);
      letter-spacing: 0.1em;
      margin-bottom: 0.5rem;
    }

    .history-list {
      display: flex;
      flex-direction: column;
      gap: 4px;
    }

    .history-item {
      display: flex;
      justify-content: space-between;
      align-items: center;
      background: var(--surface);
      border: 1px solid var(--border);
      padding: 0.4rem 0.75rem;
      font-size: 0.8rem;
      color: var(--muted);
    }

    .history-item .outcome {
      font-family: 'Press Start 2P', monospace;
      font-size: 0.4rem;
      letter-spacing: 0.1em;
    }

    .outcome.win  { color: var(--win); }
    .outcome.lose { color: var(--lose); }
    .outcome.draw { color: var(--draw); }

    /* RESET */
    .reset-btn {
      font-family: 'Press Start 2P', monospace;
      font-size: 0.5rem;
      color: var(--muted);
      background: transparent;
      border: 1px solid var(--border);
      padding: 0.6rem 1.2rem;
      cursor: pointer;
      letter-spacing: 0.08em;
      transition: color 0.15s, border-color 0.15s;
    }

    .reset-btn:hover {
      color: var(--accent2);
      border-color: var(--accent2);
    }

    /* PIXEL corners decoration */
    .corner-deco {
      position: relative;
    }
    .corner-deco::before,
    .corner-deco::after {
      content: '';
      position: absolute;
      width: 8px;
      height: 8px;
      border-color: var(--accent);
      border-style: solid;
    }
    .corner-deco::before {
      top: -1px; left: -1px;
      border-width: 2px 0 0 2px;
    }
    .corner-deco::after {
      bottom: -1px; right: -1px;
      border-width: 0 2px 2px 0;
    }
  </style>
</head>
<body>

<div class="wrapper">

  <div class="title">
    ROCK<br/>
    PAPER<br/>
    <span>SCISSORS</span>
  </div>

  <!-- Scoreboard -->
  <div class="scoreboard">
    <div class="score-box">
      <div class="score-label">PLAYER</div>
      <div class="score-num" id="p-score">00</div>
    </div>
    <div class="score-box cpu-box">
      <div class="score-label">CPU</div>
      <div class="score-num" id="c-score">00</div>
    </div>
  </div>

  <!-- Arena -->
  <div class="arena corner-deco">
    <div class="fighter">
      <div class="fighter-label">YOU</div>
      <div class="hand-display" id="p-hand">❓</div>
    </div>
    <div style="width:40px;"></div>
    <div class="fighter">
      <div class="fighter-label">CPU</div>
      <div class="hand-display" id="c-hand">❓</div>
    </div>
  </div>

  <!-- Result -->
  <div class="result-bar" id="result-bar">CHOOSE YOUR WEAPON</div>

  <!-- Choices -->
  <div class="choices">
    <button class="choice-btn" onclick="play('rock')">
      <!--
        REPLACE THESE SRC VALUES WITH YOUR OWN IMAGES!
        Example: src="images/my-rock.png"
        Put your image files in an /images folder next to this HTML file.
      -->
      <img src="https://cdn.jsdelivr.net/npm/twemoji@14.0.2/assets/svg/1faa8.svg" alt="rock" />
      <span class="choice-name">ROCK</span>
    </button>
    <button class="choice-btn" onclick="play('paper')">
      <img src="https://cdn.jsdelivr.net/npm/twemoji@14.0.2/assets/svg/1f4c4.svg" alt="paper" />
      <span class="choice-name">PAPER</span>
    </button>
    <button class="choice-btn" onclick="play('scissors')">
      <img src="https://cdn.jsdelivr.net/npm/twemoji@14.0.2/assets/svg/2702.svg" alt="scissors" />
      <span class="choice-name">SCISSORS</span>
    </button>
  </div>

  <!-- Reset -->
  <button class="reset-btn" onclick="resetGame()">[ RESET SCORES ]</button>

  <!-- History -->
  <div class="history" id="history-wrap" style="display:none;">
    <div class="history-title">ROUND LOG</div>
    <div class="history-list" id="history-list"></div>
  </div>

</div>

<script>
  // ─── DATA ────────────────────────────────────────────
  const choices = ['rock', 'paper', 'scissors'];

  // Emoji fallbacks shown in arena when no image loads
  const emoji = { rock: '🪨', paper: '📄', scissors: '✂️' };

  // Image sources — swap these for your own designs!
  const imgs = {
    rock:     'https://cdn.jsdelivr.net/npm/twemoji@14.0.2/assets/svg/1faa8.svg',
    paper:    'https://cdn.jsdelivr.net/npm/twemoji@14.0.2/assets/svg/1f4c4.svg',
    scissors: 'https://cdn.jsdelivr.net/npm/twemoji@14.0.2/assets/svg/2702.svg'
  };

  let playerScore = 0;
  let cpuScore    = 0;
  let roundLog    = [];

  // ─── GAME LOGIC ───────────────────────────────────────
  function getResult(player, cpu) {
    if (player === cpu) return 'draw';
    const wins = { rock: 'scissors', scissors: 'paper', paper: 'rock' };
    return wins[player] === cpu ? 'win' : 'lose';
  }

  function play(playerChoice) {
    // CPU picks randomly
    const cpuChoice = choices[Math.floor(Math.random() * 3)];
    const result    = getResult(playerChoice, cpuChoice);

    // Update scores
    if (result === 'win')  playerScore++;
    if (result === 'lose') cpuScore++;

    // Update score display (pad to 2 digits)
    document.getElementById('p-score').textContent = String(playerScore).padStart(2, '0');
    document.getElementById('c-score').textContent = String(cpuScore).padStart(2, '0');

    // Update arena hands with images
    const pH = document.getElementById('p-hand');
    const cH = document.getElementById('c-hand');

    // Remove old state classes
    pH.classList.remove('shake', 'winner', 'loser');
    cH.classList.remove('shake', 'winner', 'loser');

    // Inject images
    pH.innerHTML = `<img src="${imgs[playerChoice]}" alt="${playerChoice}" />`;
    cH.innerHTML = `<img src="${imgs[cpuChoice]}"    alt="${cpuChoice}"    />`;

    // Trigger shake animation (force reflow first so it replays)
    void pH.offsetWidth;
    pH.classList.add('shake');
    cH.classList.add('shake');

    // Add winner / loser highlight after animation
    setTimeout(() => {
      if (result === 'win')  { pH.classList.add('winner'); cH.classList.add('loser'); }
      if (result === 'lose') { cH.classList.add('winner'); pH.classList.add('loser'); }
    }, 420);

    // Result bar
    const bar = document.getElementById('result-bar');
    const names = { rock: 'ROCK', paper: 'PAPER', scissors: 'SCISSORS' };
    bar.className = 'result-bar ' + result;

    if (result === 'win')  bar.textContent = `YOU WIN!  ${names[playerChoice]} BEATS ${names[cpuChoice]}`;
    if (result === 'lose') bar.textContent = `YOU LOSE! ${names[cpuChoice]} BEATS ${names[playerChoice]}`;
    if (result === 'draw') bar.textContent = `DRAW!  BOTH PICKED ${names[playerChoice]}`;

    // Round log (keep last 5)
    roundLog.unshift({ playerChoice, cpuChoice, result });
    if (roundLog.length > 5) roundLog.pop();
    renderLog();
  }

  // ─── RENDER LOG ───────────────────────────────────────
  function renderLog() {
    const wrap = document.getElementById('history-wrap');
    const list = document.getElementById('history-list');
    const names = { rock: 'Rock', paper: 'Paper', scissors: 'Scissors' };

    wrap.style.display = 'block';
    list.innerHTML = roundLog.map(r =>
      `<div class="history-item">
        <span>${names[r.playerChoice]} vs ${names[r.cpuChoice]}</span>
        <span class="outcome ${r.result}">${r.result.toUpperCase()}</span>
      </div>`
    ).join('');
  }

  // ─── RESET ────────────────────────────────────────────
  function resetGame() {
    playerScore = 0;
    cpuScore    = 0;
    roundLog    = [];

    document.getElementById('p-score').textContent = '00';
    document.getElementById('c-score').textContent = '00';
    document.getElementById('p-hand').innerHTML    = '❓';
    document.getElementById('c-hand').innerHTML    = '❓';

    const bar = document.getElementById('result-bar');
    bar.className   = 'result-bar';
    bar.textContent = 'CHOOSE YOUR WEAPON';

    document.getElementById('p-hand').classList.remove('winner','loser');
    document.getElementById('c-hand').classList.remove('winner','loser');
    document.getElementById('history-wrap').style.display = 'none';
  }
</script>

</body>
</html>
