<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Victoria Cimino, MD/PhD | MAXIMUM VIBE 💅✨</title>
    
    <!-- Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Manrope:wght@300;400;600;800&family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=VT323&family=Press+Start+2P&family=Comic+Neue:wght@700&family=Fira+Code:wght@500&display=swap" rel="stylesheet">

    <style>
        :root {
            --bg-color: #000000; 
            --card-bg: #1c1c21;
            --accent: #b28dff; 
            --accent-glow: rgba(178, 141, 255, 0.6);
            --accent-secondary: #e06c50; 
            --text-main: #ffffff;
            --text-muted: #a1a1aa;
            --gap: 20px;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            cursor: none; 
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-main);
            font-family: 'Manrope', sans-serif;
            overflow-x: hidden;
            position: relative;
        }

        /* -----------------------
           OPTIMIZED BACKGROUND
           ----------------------- */
        .emoji-bg-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0; 
            overflow: hidden;
            will-change: transform; 
        }

        .floater {
            position: absolute;
            font-size: 3rem; 
            opacity: 1; 
            user-select: none;
            animation-name: float;
            animation-timing-function: linear;
            animation-iteration-count: infinite;
            top: 0; 
        }

        @keyframes float {
            0% { transform: translate3d(0, 110vh, 0) rotate(0deg); }
            100% { transform: translate3d(0, -20vh, 0) rotate(360deg); }
        }

        /* -----------------------
           CONTAINER
           ----------------------- */
        .container {
            max-width: 1200px;
            margin: 40px auto;
            padding: 60px 40px;
            position: relative;
            z-index: 2;
            background: rgba(10, 10, 12, 0.6); 
            backdrop-filter: blur(4px); 
            border-radius: 40px;
            border: 1px solid rgba(255,255,255,0.1);
            box-shadow: 0 0 50px rgba(0,0,0,0.8); 
        }

        /* -----------------------
           CUSTOM CURSOR
           ----------------------- */
        .cursor-outline {
            position: fixed;
            top: 0;
            left: 0;
            transform: translate(-50%, -50%);
            border-radius: 50%;
            z-index: 9999;
            pointer-events: none;
            width: 40px; 
            height: 40px;
            border: 2px solid rgba(255, 255, 255, 0.9);
            transition: width 0.1s, height 0.1s, background-color 0.1s; 
            box-shadow: 0 0 10px white;
        }

        /* NEW: Glitch Mode for Cursor (The Poop Transformation) */
        .cursor-poop-mode {
            border: none !important;
            box-shadow: none !important;
            background: transparent !important;
            width: auto !important;
            height: auto !important;
            font-size: 3rem; /* Big emoji */
            line-height: 1;
            display: flex;
            justify-content: center;
            align-items: center;
            /* Jitter Animation */
            animation: cursor-shake 0.1s infinite; 
        }

        /* Margin shake allows Transform to still handle mouse position */
        @keyframes cursor-shake {
            0% { margin-left: -3px; margin-top: 2px; }
            25% { margin-left: 3px; margin-top: -2px; }
            50% { margin-left: -1px; margin-top: 3px; }
            75% { margin-left: 2px; margin-top: -1px; }
            100% { margin-left: 0; margin-top: 0; }
        }

        /* -----------------------
           TERMINAL OVERLAY (Top Right Notification)
           ----------------------- */
        .terminal-overlay {
            position: fixed;
            top: 20px;
            right: 20px;
            width: 400px;
            height: auto;
            background: rgba(0, 0, 0, 0.95); 
            border: 2px solid #00ff00;
            box-shadow: 0 0 20px rgba(0, 255, 0, 0.4);
            z-index: 20000;
            display: flex;
            flex-direction: column;
            padding: 20px;
            border-radius: 8px;
            font-family: 'Fira Code', 'Courier New', monospace;
            font-size: 1rem;
            pointer-events: none;
            transform: translateX(120%); 
            transition: transform 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        .terminal-overlay.active { transform: translateX(0); }

        .term-line {
            margin-bottom: 8px;
            opacity: 0; 
            transform: translateX(10px);
            transition: all 0.2s;
        }
        .term-line.visible { opacity: 1; transform: translateX(0); }

        .color-green { color: #00ff00; text-shadow: 0 0 5px #00ff00; }
        .color-red { color: #ff0000; text-shadow: 0 0 5px #ff0000; font-weight: bold; }
        .color-blue { color: #00ffff; text-shadow: 0 0 5px #00ffff; }
        
        /* -----------------------
           POP-UP AD STYLES
           ----------------------- */
        .fake-popup {
            position: fixed;
            z-index: 10000; 
            min-width: 250px;
            max-width: 350px;
            box-shadow: 10px 10px 0px rgba(0,0,0,0.5);
            cursor: auto !important; 
        }
        
        .fake-popup * { cursor: auto !important; }

        /* 1. Windows 95 */
        .popup-win95 {
            background: #c0c0c0;
            border: 2px outset #ffffff;
            font-family: 'Courier New', monospace;
            color: black;
            padding: 2px;
        }
        .win95-header {
            background: #000080;
            color: white;
            padding: 4px 8px;
            font-weight: bold;
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 14px;
        }
        .win95-body { padding: 15px; text-align: center; font-size: 14px; }
        .win95-btn { margin-top: 10px; cursor: pointer; border: 2px outset white; background: #c0c0c0; }

        /* 2. Cyber/Hacker */
        .popup-cyber {
            background: #000;
            border: 2px solid #00ff00;
            font-family: 'VT323', monospace;
            color: #00ff00;
        }
        .cyber-header {
            border-bottom: 2px solid #00ff00;
            padding: 5px;
            background: rgba(0, 255, 0, 0.1);
        }
        .cyber-body { padding: 15px; text-align: center; font-size: 1.4rem; }
        .blink { animation: blink 1s infinite; }
        @keyframes blink { 50% { opacity: 0; } }

        /* 3. Retro/Hot Dog */
        .popup-retro {
            background: yellow;
            border: 4px dashed red;
            font-family: 'Comic Sans MS', cursive;
            color: red;
        }
        .retro-body { padding: 20px; text-align: center; font-weight: bold; font-size: 1.1rem; }
        .retro-btn { background: blue; color: white; border: none; padding: 10px; cursor: pointer; }

        /* 4. Lottery */
        .popup-lottery {
            background: repeating-linear-gradient(45deg, #ffcc00, #ffcc00 10px, #ffdd44 10px, #ffdd44 20px);
            border: 5px solid #ff00ff;
            color: #000;
            font-family: sans-serif;
            text-align: center;
        }
        .lottery-header { background: #ff00ff; color: white; padding: 5px; font-weight: bold; animation: flash 0.5s infinite; }
        .lottery-body { padding: 20px; background: rgba(255,255,255,0.8); border: 2px solid black; margin: 10px; }
        @keyframes flash { 50% { background: red; } }

        /* 5. Fatal Error */
        .popup-error {
            background: #cc0000;
            border: 2px solid white;
            color: white;
            font-family: Arial, sans-serif;
            box-shadow: 0 0 20px red;
        }
        .error-header { padding: 5px; background: white; color: red; font-weight: 900; display: flex; justify-content: space-between; }
        .error-body { padding: 20px; text-align: center; }
        .error-icon { font-size: 40px; margin-bottom: 10px; display: block; }

        /* 6. MSN Chat */
        .popup-chat {
            background: #f0f4f9;
            border: 1px solid #6688aa;
            border-radius: 5px 5px 0 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            color: black;
        }
        .chat-header {
            background: linear-gradient(to bottom, #b0c4de, #86a0bb);
            padding: 5px 10px;
            color: white;
            font-size: 12px;
            border-radius: 4px 4px 0 0;
            display: flex; justify-content: space-between;
        }
        .chat-body { padding: 10px; font-size: 13px; }
        .chat-msg { color: #000080; margin-bottom: 5px; }

        /* 7. Mac Classic */
        .popup-mac {
            background: #fff;
            border: 2px solid black;
            border-radius: 5px;
            box-shadow: 3px 3px 0 black;
            font-family: 'Chicago', sans-serif; 
            color: black;
        }
        .mac-header {
            border-bottom: 2px solid black;
            padding: 3px;
            background: repeating-linear-gradient(90deg, black, black 1px, white 1px, white 2px);
            text-align: center;
        }
        .mac-title { background: white; padding: 0 10px; font-size: 12px; }
        .mac-body { padding: 20px; text-align: center; }
        .mac-btn { border: 2px solid black; background: white; padding: 5px 15px; border-radius: 10px; cursor: pointer; }

        /* 8. Virus */
        .popup-virus {
            background: #000000;
            border: 2px solid red;
            color: red;
            font-family: 'VT323', monospace;
            text-align: center;
            width: 300px;
        }
        .virus-header { background: red; color: black; font-weight: bold; padding: 2px; }
        .virus-body { padding: 15px; }
        .virus-bar { width: 100%; height: 15px; border: 1px solid red; margin-top: 10px; position: relative; }
        .virus-fill { height: 100%; background: red; width: 0%; animation: loadBar 3s infinite; }
        @keyframes loadBar { 0% {width: 0%} 50% {width: 70%} 100% {width: 100%} }

        /* 9. Clippy */
        .popup-clippy {
            background: #ffffcc;
            border: 1px solid black;
            border-radius: 10px;
            color: black;
            font-family: 'Comic Neue', cursive;
            max-width: 250px;
            border-bottom-left-radius: 0;
        }
        .clippy-body { padding: 15px; position: relative; font-size: 14px; }
        .clippy-btn { background: white; border: 1px solid black; margin-top: 5px; padding: 2px 8px; cursor: pointer; font-size: 12px; }

        /* 10. Spam Email */
        .popup-spam {
            background: white;
            border: 2px outset #ccc;
            color: navy;
            font-family: 'Times New Roman', serif;
        }
        .spam-header { background: navy; color: white; padding: 2px 5px; font-weight: bold; font-family: sans-serif; font-size: 12px; }
        .spam-body { padding: 10px; font-size: 14px; line-height: 1.1; }
        .spam-link { color: blue; text-decoration: underline; cursor: pointer; font-weight: bold; }

        /* -----------------------
           TYPOGRAPHY
           ----------------------- */
        h1 {
            font-family: 'Playfair Display', serif;
            font-size: clamp(3rem, 7vw, 6rem);
            line-height: 1.2; 
            margin-bottom: 25px;
            letter-spacing: -0.02em;
            text-shadow: 4px 4px 0px rgba(0,0,0,1); 
        }

        .title-row { 
            display: block; 
            white-space: nowrap; 
        }

        .grad-text { color: #ffffff; font-weight: 400; }

        .highlight-text {
            color: #ffffff;
            background: none;
            -webkit-text-fill-color: #ffffff;
            font-style: italic;
            text-shadow: 0 0 15px var(--accent-glow);
        }

        .title-emoji {
            display: inline-block;
            vertical-align: middle;
            margin-left: 15px;
            position: relative;
            top: -5px; 
            filter: drop-shadow(0 0 5px rgba(0,0,0,0.8));
        }

        p {
            color: #eee;
            font-size: 1.15rem;
            text-shadow: 0 2px 4px rgba(0,0,0,1);
            font-weight: 500;
        }

        /* -----------------------
           LAYOUT ELEMENTS
           ----------------------- */
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 0 40px 0;
        }

        .logo { font-weight: 800; font-size: 1.5rem; letter-spacing: -0.05em; }

        .status-pill {
            background: rgba(255, 255, 255, 0.2); 
            padding: 8px 16px;
            border-radius: 50px;
            font-size: 0.85rem;
            display: flex;
            align-items: center;
            gap: 10px;
            border: 2px solid rgba(255,255,255,0.5);
            backdrop-filter: blur(5px);
        }

        .status-dot {
            width: 8px; height: 8px;
            background-color: #00ff88;
            border-radius: 50%;
            box-shadow: 0 0 10px #00ff88;
        }

        .hero { margin-bottom: 80px; max-width: 100%; }

        .hero-tags { display: flex; gap: 10px; margin-top: 30px; flex-wrap: wrap; }

        .tag {
            border: 1px solid rgba(255,255,255,0.4);
            color: #fff;
            padding: 10px 20px;
            border-radius: 100px;
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: 0.1s;
            background: #000; 
            box-shadow: 0 4px 10px rgba(0,0,0,0.5);
        }
        .tag:hover { border-color: var(--accent); color: var(--accent); transform: scale(1.1); box-shadow: 0 0 20px var(--accent); }

        /* -----------------------
           BENTO GRID
           ----------------------- */
        .bento-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            grid-template-rows: 340px 340px 220px 220px 220px; 
            gap: var(--gap);
            margin-bottom: 20px;
        }

        .bento-card {
            background-color: var(--card-bg);
            border-radius: 24px;
            padding: 30px;
            position: relative;
            z-index: 1; 
            transition: transform 0.1s linear; 
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            overflow: hidden; 
            box-shadow: 0 10px 40px rgba(0,0,0,0.5);
            transform-style: preserve-3d;
            will-change: transform; 
            border-style: solid;
            border-width: 4px;
        }

        .bento-card:hover {
            z-index: 10;
            box-shadow: 0 0 40px rgba(255,255,255,0.1);
        }

        /* 🌈 UNIQUE BORDER COLORS */
        .card-photo-main { border-color: #ff00ff; } 
        .card-bio { border-color: #00ff88; } 
        .card-stats { border-color: #00ffff; } 
        .card-review { border-color: #ffff00; } 
        .card-exp { border-color: #ff5500; } 
        .card-fun { border-color: #b28dff; } 
        .card-philosophy { border-color: #ff0055; } 
        .card-contact { border-color: #ffffff; } 
        .card-ick { border-color: #aaff00; } 
        .card-coffee { border-color: #ff9900; } 
        .card-aura { border-color: #0099ff; } 

        /* Canvas Overlay */
        .sparkle-canvas {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 5;
        }

        .bento-card h3, 
        .bento-card p, 
        .bento-card div, 
        .bento-card ul {
            position: relative;
            z-index: 6;
        }

        /* 1. Main Photo */
        .card-photo-main {
            grid-column: span 2;
            grid-row: span 2;
            background-image: url('victoria.jpg'); 
            background-size: cover;
            background-position: center 20%; 
            justify-content: flex-end !important;
        }
        .card-photo-main::after {
            content: ''; position: absolute; inset: 0;
            background: linear-gradient(to top, rgba(0,0,0,0.9) 0%, transparent 60%);
            z-index: 2; 
        }
        
        /* 2. Bio */
        .card-bio { grid-column: span 2; grid-row: span 1; }

        /* 3. Stats */
        .card-stats {
            grid-column: span 1; grid-row: span 1;
            text-align: center; justify-content: center; align-items: center;
            background: linear-gradient(145deg, #1c1c21, #25252b);
        }

        /* 4. Review */
        .card-review {
            grid-column: span 1; grid-row: span 1;
            background-color: var(--card-bg); 
            color: #fff;
        }
        .card-review * { color: #fff !important; text-shadow: none; font-weight: 400; }

        /* 5. Timeline */
        .card-exp { grid-column: span 1; grid-row: span 2; overflow-y: auto; }

        /* 6. Personality */
        .card-fun {
            grid-column: span 1; grid-row: span 1;
            background: var(--accent); color: #000;
        }
        .card-fun * { color: #000 !important; border-color: rgba(0,0,0,0.2) !important; text-shadow: none; font-weight: 600; }

        /* 7. Philosophy */
        .card-philosophy {
            grid-column: span 2; grid-row: span 1;
            position: relative;
        }
        .card-philosophy::before {
            content: '🔮'; position: absolute; right: 20px; top: 10px;
            font-size: 5rem; opacity: 0.1; line-height: 1;
        }

        /* 8. Contact */
        .card-contact {
            grid-column: span 1; grid-row: span 1;
            background: var(--accent-secondary); color: white;
            display: flex; align-items: center; justify-content: center; text-decoration: none;
        }
        .card-contact h3 { color: white; font-size: 1.8rem; }
        .card-contact p { color: rgba(255,255,255,0.8); }

        /* 9. The Ick */
        .card-ick {
            grid-column: span 1; grid-row: span 1;
            background: #2a2a30;
        }
        .ick-list { list-style: none; margin-top: 10px; }
        .ick-list li { margin-bottom: 5px; color: #ff6b6b; font-size: 0.9rem; text-shadow: none; font-weight: 700; }

        /* 10. Coffee */
        .card-coffee {
            grid-column: span 1; grid-row: span 1;
            background: linear-gradient(to bottom, #1c1c21, #463325);
            text-align: center; justify-content: center; align-items: center;
        }

        /* 11. Aura Points */
        .card-aura {
            grid-column: span 2; grid-row: span 1;
            background: linear-gradient(45deg, #1c1c21, #2d1c3d);
        }
        
        /* Typography Helpers */
        .card-title { font-size: 1.4rem; margin-bottom: 10px; font-weight: 800; color: #fff; text-shadow: 0 2px 10px rgba(0,0,0,1); }
        .big-stat {
            font-size: 4rem; font-weight: 700;
            color: #fff;
            background: none;
            text-shadow: 0 0 20px rgba(255,255,255,0.8);
            line-height: 1;
        }
        ul.exp-list { list-style: none; margin-top: 15px; }
        ul.exp-list li { margin-bottom: 20px; padding-left: 15px; border-left: 2px solid var(--border); }
        ul.exp-list li strong { display: block; font-size: 1rem; color: #fff; }
        ul.exp-list li span { font-size: 0.8rem; color: var(--accent); text-transform: uppercase; letter-spacing: 0.5px; }

        /* Mobile */
        @media (max-width: 900px) {
            .container { padding: 30px 20px; margin: 20px auto; width: 95%; }
            .bento-grid {
                grid-template-columns: 1fr;
                grid-template-rows: auto;
                display: flex; flex-direction: column;
            }
            .bento-card { min-height: 280px; }
            .card-photo-main { min-height: 550px; }
            h1 { font-size: 2.8rem; white-space: normal; } 
            .title-row { white-space: normal; }
            .cursor-outline, .sparkle-canvas { display: none; }
            * { cursor: auto; }
        }

        .fade-up {
            opacity: 0; transform: translateY(30px);
            transition: all 0.8s cubic-bezier(0.16, 1, 0.3, 1);
        }
        .visible { opacity: 1; transform: translateY(0); }

    </style>
</head>
<body>

    <!-- TERMINAL OVERLAY INTRO (Top Right Box) -->
    <div id="terminal-overlay" class="terminal-overlay">
        <div class="term-line color-green">> CONNECTING_TO_SERVER... [OK]</div>
        <div class="term-line color-green">> SCANNING_ORGANIZATION...</div>
        <div class="term-line color-red">> ERROR: LEADERSHIP_NOT_FOUND</div>
        <div class="term-line color-blue">> INITIATING_VICTORIA_CIMINO_PROTOCOL...</div>
        <div class="term-line color-green">> UPLOADING_CHAOS.EXE... [100%]</div>
    </div>

    <div class="emoji-bg-container" id="emoji-container"></div>
    <div class="cursor-outline" data-cursor-outline></div>

    <div class="container">
        
        <header class="fade-up">
            <div class="logo">Dr. Cimino 👩🏻‍⚕️✨</div>
            <div class="status-pill">
                <div class="status-dot"></div>
                <span>Current Status: Locked In 🔒🔥</span>
            </div>
        </header>

        <section class="hero fade-up">
            <h1>
                <div class="title-row">
                    <span class="grad-text">Physician.</span> <span class="title-emoji">🩺💀</span>
                </div>
                <div class="title-row">
                    <span class="grad-text">Scientist.</span> <span class="title-emoji">🧪🔬</span>
                </div>
                <div class="title-row">
                    <span class="highlight-text">Main Character.</span> <span class="title-emoji">💅👑</span>
                </div>
            </h1>
            <p>Dr. Victoria Cimino. MD/PhD. I don't just practice medicine; I set the standard. 📉 Bridging the gap between clinical excellence and absolute boss energy. If you want problems solved with style, you're in the right place. 🧠🚀</p>
            <div class="hero-tags">
                <div class="tag">Med Director 🫡</div>
                <div class="tag">Clin. Strategy 📈</div>
                <div class="tag">Patient Stan 🗣️</div>
                <div class="tag">No Cap 🧢</div>
                <div class="tag">System Fixer 🛠️</div>
            </div>
        </section>

        <div class="bento-grid">
            <div class="bento-card card-photo-main fade-up">
                <div class="card-content">
                    <h3 class="card-title" style="color:white;">The Face of Med ✨📸</h3>
                    <p style="color:rgba(255,255,255,0.7);">📍 Yardley, PA | 🦉 Temple Made | 🧪 Einstein Alum</p>
                </div>
            </div>
            <div class="bento-card card-bio fade-up">
                <h3 class="card-title">The Lore 📖👀</h3>
                <p>Board-certified Internist (MD/PhD type beat 🧬). I analyze root causes—whether in a patient's physiology or a hospital's workflow. I treat the whole system. No band-aid fixes. We don't do that here. 🙅‍♀️🛑</p>
            </div>
            <div class="bento-card card-stats fade-up">
                <div class="big-stat">10+ 🗓️</div>
                <div style="margin-top:10px; text-transform: uppercase; letter-spacing:1px; font-size: 0.8rem; color: #ccc;">Years of Slaying</div>
            </div>
            <div class="bento-card card-review fade-up">
                <h3 class="card-title">The Tea ☕️🫖</h3>
                <p style="font-style:italic;">"She actually listens?? 10/10 would recommend. Finally found a doc who passes the vibe check. 😭🙌"</p>
                <div style="margin-top:15px;">⭐⭐⭐⭐⭐</div>
            </div>
            <div class="bento-card card-exp fade-up">
                <h3 class="card-title">My Era 🕰️🚀</h3>
                <ul class="exp-list">
                    <li><strong>Medical Director 🏥</strong><span>Current Mood</span></li>
                    <li><strong>Internal Med 🫀</strong><span>Senior Care Slay</span></li>
                    <li><strong>Residency 🏙️</strong><span>Temple Univ (Philly!)</span></li>
                    <li><strong>MD/PhD 🧬🎓</strong><span>Einstein College of Med</span></li>
                </ul>
            </div>
            <div class="bento-card card-fun fade-up">
                <h3 class="card-title">Touch Grass 🌱☀️</h3>
                <p>When I'm not saving lives, I'm just vibing. Empathy + Humor = The best medicine (literally). 💊😂</p>
            </div>
            <div class="bento-card card-philosophy fade-up">
                <h3 class="card-title">The Philosophy 🔮</h3>
                <p>Data-driven decisions 📊 but make it human 🫂. I believe in transparent leadership and no toxic workplaces allowed. Happy providers = Healed patients. Period. 💅✨</p>
            </div>
            <a href="mailto:email@example.com" class="bento-card card-contact fade-up">
                <div style="text-align: center;">
                    <h3>Hit My Line 📲🤙</h3>
                    <p style="margin-top:5px;">Peep the CV &nearr;</p>
                </div>
            </a>
            <div class="bento-card card-ick fade-up">
                <h3 class="card-title">My Icks 🤢🛑</h3>
                <ul class="ick-list">
                    <li>🚫 Prior Authorizations</li>
                    <li>🚫 Broken Fax Machines</li>
                    <li>🚫 "This is how we've always done it"</li>
                    <li>🚫 Bad Coffee</li>
                </ul>
            </div>
            <div class="bento-card card-coffee fade-up">
                <div>
                    <div style="font-size: 3rem;">☕️🧊</div>
                    <h3 class="card-title" style="margin-top:10px;">Fuel Source</h3>
                    <p>Iced Oat Milk Latte.<br>Even in winter. ❄️</p>
                </div>
            </div>
            <div class="bento-card card-aura fade-up">
                <h3 class="card-title">Aura Points 📈✨</h3>
                <p>+1000 : Fixed a systemic workflow issue<br>+5000 : Patient said "You get me"<br>+500 : Wrote this code<br>-0 : Never losing.</p>
            </div>
        </div>

        <footer style="text-align: center; color: var(--text-muted); padding-bottom: 40px; font-size: 0.9rem;" class="fade-up">
            <p>&copy; 2025 Victoria Cimino. No Cap. 🧢🔥 All Rights Reserved.</p>
        </footer>
    </div>

    <script>
        // 1. OPTIMIZED BACKGROUND
        const emojiContainer = document.getElementById('emoji-container');
        const medicalEmojis = ['🩺', '🧬', '💊', '🧠', '🫀', '🚑', '🏥', '💉', '🦠', '🩸', '🩹', '🦴', '🦷', '👩🏻‍⚕️', '🔬', '✨', '💅', '💀', '🔥', '👀'];

        function createMaximalistBg() {
            const count = window.innerWidth < 800 ? 50 : 80;
            
            for (let i = 0; i < count; i++) {
                const el = document.createElement('div');
                el.classList.add('floater');
                el.innerText = medicalEmojis[Math.floor(Math.random() * medicalEmojis.length)];
                
                el.style.left = Math.random() * 100 + 'vw';
                
                const size = (Math.random() * 4) + 2;
                el.style.fontSize = size + 'rem';
                
                const duration = Math.random() * 10 + 10;
                el.style.animationDuration = duration + 's';
                el.style.animationDelay = -Math.random() * duration + 's';

                emojiContainer.appendChild(el);
            }
        }
        createMaximalistBg();

        // 2. CURSOR
        const cursorOutline = document.querySelector('[data-cursor-outline]');

        window.addEventListener("mousemove", function(e) {
            const posX = e.clientX;
            const posY = e.clientY;
            
            cursorOutline.animate({
                transform: `translate(${posX}px, ${posY}px)`
            }, { duration: 100, fill: "forwards" });
        });
        
        cursorOutline.style.top = '0'; cursorOutline.style.left = '0';

        // 3. POP-UP STYLES
        const popupStyles = [
            (id) => `<div id="${id}" class="fake-popup popup-win95"><div class="win95-header"><span>System Alert</span><span onclick="document.getElementById('${id}').remove()" style="cursor:pointer">X</span></div><div class="win95-body"><p style="color:black; font-weight:bold; text-shadow:none;">HIRE VICTORIA CIMINO!</p><button class="win95-btn" onclick="document.getElementById('${id}').remove()">OK</button></div></div>`,
            (id) => `<div id="${id}" class="fake-popup popup-cyber"><div class="cyber-header">>> INCOMING_TRANSMISSION<span onclick="document.getElementById('${id}').remove()" style="cursor:pointer; float:right;">[X]</span></div><div class="cyber-body"><p class="blink" style="color:#00ff00; text-shadow:none;">> CANDIDATE_FOUND</p><p style="color:#00ff00; margin-top:10px; font-size:1rem; text-shadow:none;">Victoria Cimino is the best choice.</p></div></div>`,
            (id) => `<div id="${id}" class="fake-popup popup-retro"><div class="retro-body"><p style="color:red; font-size:24px; text-shadow:none;">🔥 HOT DEAL! 🔥</p><p style="color:black; font-weight:bold; text-shadow:none;">YES!!!!</p><button class="retro-btn" onclick="document.getElementById('${id}').remove()">HIRE NOW!</button></div></div>`,
            (id) => `<div id="${id}" class="fake-popup popup-lottery"><div class="lottery-header">★ WINNER! ★</div><div class="lottery-body"><p style="color:black; font-size:20px; font-weight:bold; text-shadow:none;">YOU ARE THE 1,000,000th RECRUITER!</p><button style="background:red; color:white; padding:5px 10px; border:none; cursor:pointer;" onclick="document.getElementById('${id}').remove()">CLAIM PRIZE</button></div></div>`,
            (id) => `<div id="${id}" class="fake-popup popup-error"><div class="error-header"><span>FATAL ERROR</span><span onclick="document.getElementById('${id}').remove()" style="cursor:pointer">X</span></div><div class="error-body"><span class="error-icon">⚠️</span><p style="text-shadow:none;">NO MEDICAL DIRECTOR FOUND.</p></div></div>`,
            (id) => `<div id="${id}" class="fake-popup popup-chat"><div class="chat-header"><span>DrVic - Conversation</span><span onclick="document.getElementById('${id}').remove()" style="cursor:pointer">X</span></div><div class="chat-body"><p class="chat-msg" style="text-shadow:none;"><strong>DrVic says:</strong></p><p class="chat-msg" style="text-shadow:none;">heyyy... heard u lookin 4 a leader? 👀</p></div></div>`,
            (id) => `<div id="${id}" class="fake-popup popup-mac"><div class="mac-header"><span class="mac-title">System Update</span></div><div class="mac-body"><p style="color:black; margin-bottom:15px; text-shadow:none;">Update available: "Leadership 2.0"</p><button class="mac-btn" onclick="document.getElementById('${id}').remove()">Install</button></div></div>`,
            (id) => `<div id="${id}" class="fake-popup popup-virus"><div class="virus-header">⚠ INFECTION DETECTED</div><div class="virus-body"><p style="color:red; font-size:18px; margin-bottom:5px; text-shadow:none;">CRITICAL ERROR!</p><div class="virus-bar"><div class="virus-fill"></div></div><p style="color:red; font-size:12px; margin-top:5px; text-shadow:none;">Installing VICTORIA.EXE...</p></div></div>`,
            (id) => `<div id="${id}" class="fake-popup popup-clippy"><div class="clippy-body"><span style="font-size:40px; display:block; margin-bottom:5px;">📎</span><p style="color:black; font-size:14px; margin-bottom:10px; text-shadow:none;">Would you like help finding the best Director?</p><button class="clippy-btn" onclick="document.getElementById('${id}').remove()">Yes.</button></div></div>`,
            (id) => `<div id="${id}" class="fake-popup popup-spam"><div class="spam-header">📧 URGENT PROPOSAL</div><div class="spam-body"><p style="color:black; margin-bottom:5px; text-shadow:none;">I have inherited 10,000,000 Medical Skills.</p><p class="spam-link" onclick="document.getElementById('${id}').remove()">CLICK HERE</p></div></div>`
        ];

        function spawnPopup() {
            const id = 'popup-' + Date.now();
            const styleIndex = Math.floor(Math.random() * popupStyles.length);
            
            const div = document.createElement('div');
            div.innerHTML = popupStyles[styleIndex](id);
            const popupElement = div.firstElementChild;

            const popupWidth = 300; 
            const popupHeight = 200;
            const maxX = window.innerWidth - popupWidth;
            const maxY = window.innerHeight - popupHeight;

            let x, y;
            
            if (Math.random() < 0.8) {
                const edge = Math.floor(Math.random() * 4); 
                switch(edge) {
                    case 0: x = Math.random() * maxX; y = Math.random() * (maxY * 0.15); break;
                    case 1: x = (maxX * 0.85) + (Math.random() * (maxX * 0.15)); y = Math.random() * maxY; break;
                    case 2: x = Math.random() * maxX; y = (maxY * 0.85) + (Math.random() * (maxY * 0.15)); break;
                    case 3: x = Math.random() * (maxX * 0.15); y = Math.random() * maxY; break;
                }
            } else {
                x = Math.random() * maxX;
                y = Math.random() * maxY;
            }
            
            const rotation = (Math.random() * 40) - 20;

            popupElement.style.left = `${x}px`;
            popupElement.style.top = `${y}px`;
            popupElement.style.transform = `rotate(${rotation}deg)`;

            document.body.appendChild(popupElement);

            popupElement.animate([
                { transform: `scale(0) rotate(${rotation}deg)` },
                { transform: `scale(1) rotate(${rotation}deg)` }
            ], {
                duration: 400,
                easing: 'cubic-bezier(0.175, 0.885, 0.32, 1.275)',
                fill: 'forwards'
            });
        }

        // -------------------------------------
        // INITIAL TERMINAL SEQUENCE (DELAYED CHAOS)
        // -------------------------------------
        function startChaosSequence() {
            const overlay = document.getElementById('terminal-overlay');
            const lines = overlay.querySelectorAll('.term-line');
            
            // 1. Activate Overlay at T=6500ms (6.5s)
            setTimeout(() => { overlay.classList.add('active'); }, 6500);

            // 2. Reveal Lines sequentially (T=7000ms+)
            setTimeout(() => { lines[0].classList.add('visible'); }, 7000);
            setTimeout(() => { lines[1].classList.add('visible'); }, 7500);
            setTimeout(() => { lines[2].classList.add('visible'); }, 8000);
            setTimeout(() => { lines[3].classList.add('visible'); }, 8500);
            setTimeout(() => { lines[4].classList.add('visible'); }, 9000);

            // 3. Fade Out Overlay (T=10000ms)
            setTimeout(() => { overlay.classList.remove('active'); }, 10000);

            // 4. Start Spawning Popups at T=10500ms (10.5s)
            setTimeout(() => {
                setInterval(spawnPopup, 2500);
            }, 10500);

            // 5. GLITCH CURSOR (At 8 seconds)
            setTimeout(() => {
                const cursor = document.querySelector('[data-cursor-outline]');
                cursor.classList.add('cursor-poop-mode');
                cursor.innerHTML = '💩';
            }, 8000);
        }

        window.addEventListener('load', startChaosSequence);


        // 4. SPRITE-BASED CANVAS SPARKLE SYSTEM
        const spriteCanvas = document.createElement('canvas');
        spriteCanvas.width = 50;
        spriteCanvas.height = 50;
        const spriteCtx = spriteCanvas.getContext('2d');
        spriteCtx.font = '40px serif';
        spriteCtx.fillStyle = 'white';
        spriteCtx.textAlign = 'center';
        spriteCtx.textBaseline = 'middle';
        spriteCtx.shadowBlur = 10;
        spriteCtx.shadowColor = 'white';
        spriteCtx.fillText('✦', 25, 25); 

        class SparkleSystem {
            constructor(card) {
                this.card = card;
                this.canvas = document.createElement('canvas');
                this.canvas.classList.add('sparkle-canvas');
                this.card.appendChild(this.canvas);
                this.ctx = this.canvas.getContext('2d');
                this.particles = [];
                this.isActive = false;
                
                this.resize();
                this.animate = this.animate.bind(this);
            }

            resize() {
                const rect = this.card.getBoundingClientRect();
                this.canvas.width = rect.width;
                this.canvas.height = rect.height;
            }

            start() {
                if(!this.isActive) {
                    this.isActive = true;
                    this.animate();
                }
            }

            stop() {
                this.isActive = false;
                this.ctx.clearRect(0, 0, this.canvas.width, this.canvas.height);
                this.particles = [];
            }

            createParticle() {
                for(let i=0; i<3; i++) { 
                    this.particles.push({
                        x: Math.random() * this.canvas.width,
                        y: Math.random() * this.canvas.height,
                        size: (Math.random() * 20) + 10, 
                        alpha: 0,
                        velocity: 0.1, 
                        life: 1.0,
                        decay: Math.random() * 0.03 + 0.02
                    });
                }
            }

            animate() {
                if (!this.isActive) return;

                this.ctx.clearRect(0, 0, this.canvas.width, this.canvas.height);
                
                this.createParticle();

                for (let i = 0; i < this.particles.length; i++) {
                    const p = this.particles[i];
                    
                    if (p.life > 0.8) {
                        p.alpha += p.velocity;
                        if(p.alpha > 1) p.alpha = 1;
                    } else {
                        p.alpha -= p.decay;
                    }
                    
                    p.life -= p.decay;

                    if (p.life <= 0 || p.alpha <= 0) {
                        this.particles.splice(i, 1);
                        i--;
                        continue;
                    }

                    this.ctx.globalAlpha = p.alpha;
                    this.ctx.drawImage(spriteCanvas, p.x - p.size/2, p.y - p.size/2, p.size, p.size);
                }
                
                this.ctx.globalAlpha = 1;
                requestAnimationFrame(this.animate);
            }
        }

        const cards = document.querySelectorAll('.bento-card');
        cards.forEach(card => {
            const system = new SparkleSystem(card);
            card.addEventListener('mouseenter', () => { system.resize(); system.start(); });
            card.addEventListener('mouseleave', () => { system.stop(); });
        });

        // 5. Scroll Reveal & Tilt
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, { threshold: 0.1 });
        document.querySelectorAll('.fade-up').forEach(el => observer.observe(el));

        let isTicking = false;
        cards.forEach(card => {
            card.addEventListener('mousemove', (e) => {
                if(window.innerWidth < 900) return;
                if(!isTicking) {
                    window.requestAnimationFrame(() => {
                        const rect = card.getBoundingClientRect();
                        const x = e.clientX - rect.left;
                        const y = e.clientY - rect.top;
                        const centerX = rect.width / 2;
                        const centerY = rect.height / 2;
                        const rotateX = ((y - centerY) / centerY) * -4; 
                        const rotateY = ((x - centerX) / centerX) * 4;
                        card.style.transform = `perspective(1000px) rotateX(${rotateX}deg) rotateY(${rotateY}deg) scale(1.02)`;
                        isTicking = false;
                    });
                    isTicking = true;
                }
            });
            card.addEventListener('mouseleave', () => {
                card.style.transform = `perspective(1000px) rotateX(0) rotateY(0) scale(1)`;
            });
        });
    </script>
</body>
</html>
