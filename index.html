<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ultimate Professional Cricket Scorecard Engine</title>
    <style>
        :root {
            --primary: #0f172a;
            --accent: #2563eb;
            --success: #10b981;
            --danger: #ef4444;
            --warning: #f59e0b;
            --light: #f8fafc;
            --dark: #1e293b;
        }
        body {
            font-family: 'Segoe UI', system-ui, sans-serif;
            background-color: #0f172a;
            margin: 0;
            padding: 20px;
            color: #f8fafc;
        }
        .container {
            max-width: 1100px;
            margin: 0 auto;
            background: #1e293b;
            padding: 25px;
            border-radius: 16px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.3);
        }
        h1, h2, h3 { text-align: center; color: #fff; margin-top: 0; }
        .grid-2 { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; margin-top: 20px; }
        @media (max-width: 768px) { .grid-2 { grid-template-columns: 1fr; } }
        
        /* 3D Coin Toss Styling */
        .toss-container {
            background: #334155;
            padding: 15px;
            border-radius: 12px;
            text-align: center;
            margin-bottom: 20px;
            border: 1px dashed #475569;
        }
        .coin-wrapper { display: inline-block; perspective: 1000px; margin-right: 15px; vertical-align: middle; }
        .coin {
            width: 45px; height: 45px;
            background: #eab308;
            border-radius: 50%;
            border: 3px solid #ca8a04;
            line-height: 39px;
            font-weight: bold;
            color: #fff;
            text-align: center;
            transform-style: preserve-3d;
            transition: transform 1.2s ease-out;
        }
        .spin-animation { animation: flip 1.2s ease-out forwards; }
        @keyframes flip {
            0% { transform: rotateY(0); }
            100% { transform: rotateY(1440deg); }
        }

        /* Config Bar */
        .config-bar {
            background: #334155;
            padding: 12px;
            border-radius: 8px;
            margin-bottom: 20px;
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            gap: 10px;
        }
        .config-bar input {
            background: #0f172a; border: 1px solid #475569; color: white; padding: 6px; border-radius: 4px; width: 80px; text-align: center;
        }

        /* Tabs Navigation for Innings */
        .innings-tabs { display: flex; margin-bottom: 15px; background: #334155; border-radius: 8px; padding: 5px; }
        .tab-btn { flex: 1; padding: 10px; border: none; background: transparent; color: #94a3b8; font-weight: bold; cursor: pointer; border-radius: 6px; }
        .tab-btn.active { background: var(--accent); color: white; }
        
        /* Score Dashboard */
        .dashboard {
            background: linear-gradient(135deg, var(--accent), #1d4ed8);
            color: white;
            padding: 25px;
            border-radius: 12px;
            text-align: center;
            position: relative;
        }
        .main-score { font-size: 3.5rem; font-weight: 800; letter-spacing: -1px; margin: 10px 0; }
        .dashboard-edit-grid { display: flex; justify-content: center; align-items: center; gap: 15px; margin: 10px 0; }
        .target-box { background: rgba(0,0,0,0.25); display: inline-block; padding: 6px 16px; border-radius: 20px; font-weight: bold; font-size: 1rem; margin-top: 8px; color: #fef08a; }
        .this-over-box { margin-top: 10px; font-size: 0.95rem; opacity: 0.9; background: rgba(255,255,255,0.1); padding: 5px; border-radius: 6px; }
        
        /* Current Players Highlight Strip */
        .current-matchup-strip {
            background: #334155;
            margin: 15px 0;
            padding: 12px;
            border-radius: 8px;
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            font-size: 1rem;
            border: 1px solid #475569;
        }
        .matchup-item { padding: 4px 10px; border-radius: 4px; }
        .matchup-item.active-status { background: #1e3a8a; border-left: 3px solid var(--success); font-weight: bold; }

        /* Tables layout design */
        table { width: 100%; border-collapse: collapse; margin-bottom: 15px; background: #334155; border-radius: 8px; overflow: hidden; }
        th, td { padding: 10px 12px; text-align: left; border-bottom: 1px solid #475569; color: #e2e8f0; }
        th { background-color: #475569; color: white; font-weight: 600; }
        tr.active-player { background-color: #1e3a8a; font-weight: bold; border-left: 4px solid var(--success); }
        
        /* Controls Grid */
        .controls { display: grid; grid-template-columns: repeat(auto-fit, minmax(120px, 1fr)); gap: 10px; margin: 20px 0; }
        button { padding: 12px 6px; border: none; border-radius: 8px; font-weight: bold; cursor: pointer; transition: all 0.2s; color: white; font-size: 0.9rem; }
        button:active { transform: scale(0.95); }
        .btn-run { background-color: var(--accent); }
        .btn-extra { background-color: var(--warning); color: #000; }
        .btn-wicket { background-color: var(--danger); }
        .btn-util { background-color: #64748b; }
        .btn-edit-mode { background-color: #10b981; width: 100%; margin-bottom: 15px; font-size: 1rem;}
        
        /* Scoreboard Inputs */
        .edit-input { width: 60px; background: #0f172a; border: 1px solid #64748b; color: white; padding: 4px; border-radius: 4px; text-align: center; font-size: 1rem; }
        .edit-input.name-input { width: 140px; text-align: left; padding: 4px 8px; background: #1e293b; border: 1px solid #475569; font-weight: inherit; color: #fff;}
        .edit-input.name-input:focus { border-color: var(--accent); outline: none; background: #0f172a; }

        /* Commentary Output timeline */
        .commentary-box {
            max-height: 180px;
            overflow-y: auto;
            background: #0f172a;
            color: #38bdf8;
            padding: 15px;
            border-radius: 8px;
            font-family: 'Courier New', Courier, monospace;
            border: 1px solid #334155;
            margin-bottom: 15px;
        }
        .commentary-line { margin-bottom: 8px; border-left: 3px solid var(--accent); padding-left: 10px; font-size: 0.95rem; }
        .btn-reset { background-color: #334155; width: 100%; opacity: 0.6; }

        /* Custom Modal Style for prompts */
        .modal { display: none; position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.7); justify-content: center; align-items: center; z-index: 100; }
        .modal-content { background: #1e293b; padding: 25px; border-radius: 12px; width: 320px; text-align: center; border: 1px solid #475569; }
        .modal-content input { width: 90%; padding: 8px; margin: 15px 0; background: #0f172a; border: 1px solid #475569; color: white; border-radius: 6px; text-align: center;}
    </style>
</head>
<body>

<div class="container">
    <h1>🏏 Ultimate Professional Cricket Scorecard</h1>

    <div class="toss-container">
        <div class="coin-wrapper"><div id="visual-coin" class="coin">🪙</div></div>
        <span id="toss-result" style="font-weight: bold; color: #60a5fa;">Awaiting Match Toss...</span>
        <button class="btn-util" style="margin-left:15px; padding: 6px 14px;" onclick="executeCoinFlip()">Flip Coin 🪙</button>
    </div>

    <div class="config-bar">
        <div>
            <label>Minimum Match Overs: </label>
            <input type="number" id="max-overs-input" min="1" max="50" value="5" onchange="updateOversLimit(this.value)">
        </div>
        <div>
            <span style="color:#cbd5e1;">Target System Status: </span><b id="overs-ceiling-status">5.0 Overs Match</b>
        </div>
    </div>

    <div class="innings-tabs">
        <button id="tab-inn1" class="tab-btn active" onclick="switchInningsTab(1)">Innings 1</button>
        <button id="tab-inn2" class="tab-btn" onclick="switchInningsTab(2)">Innings 2</button>
    </div>

    <div class="dashboard">
        <h2 id="match-title" onclick="editTeamNames()" style="cursor:pointer; text-decoration: underline dashed 1px;">Click to Set Team Names</h2>
        <div id="score-display-wrapper">
            </div>
        <div id="target-ui" class="target-box" style="display:none;"></div>
    </div>

    <div class="current-matchup-strip" id="matchup-strip-ui">
        </div>

    <div class="controls">
        <button class="btn-run" onclick="addBall(0)">0 Run</button>
        <button class="btn-run" onclick="addBall(1)">1 Run</button>
        <button class="btn-run" onclick="addBall(2)">2 Runs</button>
        <button class="btn-run" onclick="addBall(4)">4 Runs 🔥</button>
        <button class="btn-run" onclick="addBall(6)">6 Runs 🚀</button>
        <button class="btn-extra" onclick="addExtra('WD')">WD (0 R, 0 B)</button>
        <button class="btn-extra" onclick="addExtra('NB')">NB (0 R, 0 B)</button>
        <button class="btn-wicket" onclick="triggerWicketModal()">Wicket ❌</button>
        <button class="btn-util" onclick="swapStrike()">Swap Strike 🔄</button>
        <button class="btn-util" style="background-color: #b45309;" onclick="undoLastBall()">Undo Ball ↩️</button>
    </div>

    <button class="btn-edit-mode" id="edit-mode-btn" onclick="toggleEditMode()">🔓 Open Manual Runs/Balls Overwrite Editor</button>

    <div class="grid-2">
        <div>
            <h3>Batting Lineup Card <small style="font-weight:normal; color:#94a3b8;">(Click names to edit)</small></h3>
            <table>
                <thead>
                    <tr><th>Batsman Name</th><th>R</th><th>B</th><th>4s</th><th>6s</th><th>S/R</th></tr>
                </thead>
                <tbody id="batting-body"></tbody>
            </table>
        </div>

        <div>
            <h3>Bowling Attack Card <small style="font-weight:normal; color:#94a3b8;">(Click names to edit)</small></h3>
            <table>
                <thead>
                    <tr><th>Bowler Name</th><th>O</th><th>M</th><th>R</th><th>W</th><th>Econ</th></tr>
                </thead>
                <tbody id="bowling-body"></tbody>
            </table>
        </div>
    </div>

    <h3>🎤 Ball-by-Ball Live Commentary</h3>
    <div class="commentary-box" id="commentary-box"></div>
    
    <button class="btn-reset" onclick="resetMatch()">Reset Scorecard Engine 🔄</button>
</div>

<div id="wicket-modal" class="modal">
    <div class="modal-content">
        <h3>❌ Wicket Down!</h3>
        <p>Enter the name of the new incoming Batsman:</p>
        <input type="text" id="new-batsman-name" placeholder="Batsman Name...">
        <button class="btn-run" style="width:100%;" onclick="confirmWicket()">Bring to Crease 🏏</button>
    </div>
</div>

<div id="bowler-modal" class="modal">
    <div class="modal-content">
        <h3>🔚 Over Complete!</h3>
        <p>Enter the name of the new Bowler:</p>
        <input type="text" id="new-bowler-name" placeholder="Bowler Name...">
        <button class="btn-run" style="width:100%; background-color: var(--success);" onclick="confirmNewBowler()">Assign Attack 🍒</button>
    </div>
</div>

<script>
    function createBlankInningsProfile() {
        return {
            runs: 0, wickets: 0, balls: 0, widesInCurrentOver: 0, activeBowlersCount: 1,
            currentStriker: 0, currentNonStriker: 1, currentBowler: 0,
            currentOverBalls: [], 
            batsmen: Array.from({length: 11}, (_, i) => ({ name: `Batsman ${i+1}`, runs: 0, balls: 0, fours: 0, sixes: 0 })),
            bowlers: Array.from({length: 10}, (_, i) => ({ name: i === 0 ? "Bowler 1" : `Bowler ${i+1}`, currentBalls: 0, maidens: 0, runs: 0, wickets: 0 })),
            timeline: ["Innings database loaded. Ready to play!"], history: []
        };
    }

    let matchState = {
        team1: "Team 1 Warriors", team2: "Team 2 Titans", maxOvers: 5, activeInnings: 1, inn1: null, inn2: null
    };

    const CACHE_KEY = "cricket_master_engine_v7";
    let savedState = localStorage.getItem(CACHE_KEY);
    if(savedState) {
        matchState = JSON.parse(savedState);
    } else {
        matchState.inn1 = createBlankInningsProfile();
        matchState.inn2 = createBlankInningsProfile();
    }

    let editMode = false;
    const commPhrases = {
        0: ["Solid defensive shot back down the track.", "Beaten him completely! Outstanding line.", "Straight to the fielder at point, no run."],
        1: ["Tapped away gently into the gap for a quick single.", "Slices it away deep to third man for a run.", "Superb running between the wickets."],
        2: ["Pushed cleanly into deep midwicket, they hustle back for a couple.", "Excellent placement, easily picking up two runs."],
        4: ["SHOT! Beautifully timed cover drive, racing to the boundary fence!", "Four runs! Pierced the infield with pure class."],
        6: ["BOOM! That is massive! Sent miles deep into the stands!", "MONSTER HIT! Dispatched into orbit for a huge six!"]
    };

    function executeCoinFlip() {
        const coin = document.getElementById("visual-coin");
        coin.classList.add("spin-animation");
        document.getElementById('toss-result').innerText = "Flipping... 🪙";
        
        setTimeout(() => {
            coin.classList.remove("spin-animation");
            const side = Math.random() < 0.5 ? "Heads" : "Tails";
            const choice = Math.random() < 0.5 ? "BAT" : "BOWL";
            coin.innerText = side === "Heads" ? "H" : "T";
            document.getElementById('toss-result').innerText = `🪙 ${side}! Toss winner elects to ${choice} first!`;
        }, 1200);
    }

    function updateOversLimit(val) {
        matchState.maxOvers = parseInt(val) || 5;
        document.getElementById("overs-ceiling-status").innerText = `${matchState.maxOvers}.0 Overs Match`;
        syncSystemState();
    }

    function switchInningsTab(id) {
        matchState.activeInnings = id;
        document.getElementById("tab-inn1").classList.toggle("active", id === 1);
        document.getElementById("tab-inn2").classList.toggle("active", id === 2);
        renderViewDOM();
    }

    function saveUndoHistory(current) {
        if(current.history.length > 25) current.history.shift();
        current.history.push(JSON.stringify({
            runs: current.runs, wickets: current.wickets, balls: current.balls,
            currentStriker: current.currentStriker, currentNonStriker: current.currentNonStriker,
            currentBowler: current.currentBowler, currentOverBalls: [...current.currentOverBalls],
            widesInCurrentOver: current.widesInCurrentOver, activeBowlersCount: current.activeBowlersCount,
            batsmen: JSON.parse(JSON.stringify(current.batsmen)), 
            bowlers: JSON.parse(JSON.stringify(current.bowlers)), timeline: [...current.timeline]
        }));
    }

    function undoLastBall() {
        let current = matchState.activeInnings === 1 ? matchState.inn1 : matchState.inn2;
        if(!current.history || current.history.length === 0) {
            alert("No delivery history available to backtrack.");
            return;
        }
        let prevState = JSON.parse(current.history.pop());
        Object.assign(current, prevState);
        current.timeline.push("↩️ [System]: Last delivery event undone.");
        syncSystemState();
    }

    function syncSystemState() {
        localStorage.setItem(CACHE_KEY, JSON.stringify(matchState));
        renderViewDOM();
    }

    // --- GAME ACTIONS ENGINE ---

    function addBall(runs) {
        let current = matchState.activeInnings === 1 ? matchState.inn1 : matchState.inn2;
        if(current.balls >= matchState.maxOvers * 6) { alert("Overs threshold reached for this innings."); return; }

        saveUndoHistory(current);
        let striker = current.batsmen[current.currentStriker];
        let bowler = current.bowlers[current.currentBowler];

        current.runs += runs;
        current.balls += 1;
        striker.runs += runs;
        striker.balls += 1;
        
        if(runs === 4) striker.fours += 1;
        if(runs === 6) striker.sixes += 1;
        bowler.runs += runs;
        bowler.currentBalls += 1;

        current.currentOverBalls.push(runs);

        let trackingOver = Math.floor((current.balls - 1) / 6) + "." + (((current.balls - 1) % 6) + 1);
        let phrases = commPhrases[runs] || ["Ball played out smoothly."];
        current.timeline.push(`[Ovr ${trackingOver}] ${striker.name} hits ${runs} runs off ${bowler.name}. -> ${phrases[Math.floor(Math.random() * phrases.length)]}`);

        if(runs % 2 !== 0) swapStrikeImmediate(current);
        checkOverCycleEnd(current);
        syncSystemState();
    }

    function addExtra(type) {
        let current = matchState.activeInnings === 1 ? matchState.inn1 : matchState.inn2;
        if(current.balls >= matchState.maxOvers * 6) return;

        saveUndoHistory(current);
        let bowler = current.bowlers[current.currentBowler];

        current.currentOverBalls.push(type);
        if(type === 'WD') current.widesInCurrentOver += 1;

        let contextOver = Math.floor(current.balls / 6) + "." + (current.balls % 6);
        current.timeline.push(`[Ovr ${contextOver}] ${bowler.name} delivered an illegal ${type} (0 runs, 0 valid balls added).`);
        syncSystemState();
    }

    function triggerWicketModal() {
        let current = matchState.activeInnings === 1 ? matchState.inn1 : matchState.inn2;
        if(current.balls >= matchState.maxOvers * 6) return;
        document.getElementById("new-batsman-name").value = "";
        document.getElementById("wicket-modal").style.display = "flex";
    }

    function confirmWicket() {
        let current = matchState.activeInnings === 1 ? matchState.inn1 : matchState.inn2;
        let newName = document.getElementById("new-batsman-name").value.trim();
        if(!newName) newName = `Batsman ${current.wickets + 3}`;

        document.getElementById("wicket-modal").style.display = "none";
        saveUndoHistory(current);

        let striker = current.batsmen[current.currentStriker];
        let bowler = current.bowlers[current.currentBowler];

        current.wickets += 1;
        current.balls += 1;
        striker.balls += 1;
        bowler.currentBalls += 1;
        bowler.wickets += 1;

        current.currentOverBalls.push("W");

        let trackingOver = Math.floor((current.balls - 1) / 6) + "." + (((current.balls - 1) % 6) + 1);
        current.timeline.push(`[Ovr ${trackingOver}] ❌ OUT! Wicket falls! ${striker.name} is dismissed by ${bowler.name}.`);

        let maxActiveIdx = Math.max(current.currentStriker, current.currentNonStriker);
        let incomingIdx = maxActiveIdx + 1;

        if(incomingIdx < 11) {
            current.batsmen[incomingIdx].name = newName;
            current.currentStriker = incomingIdx;
        } else {
            current.timeline.push("🚨 Innings Over! Team is completely All Out!");
        }

        checkOverCycleEnd(current);
        syncSystemState();
    }

    function swapStrike() {
        let current = matchState.activeInnings === 1 ? matchState.inn1 : matchState.inn2;
        swapStrikeImmediate(current);
        current.timeline.push("🔄 Strike positions changed over manually.");
        syncSystemState();
    }

    function swapStrikeImmediate(current) {
        let temp = current.currentStriker;
        current.currentStriker = current.currentNonStriker;
        current.currentNonStriker = temp;
    }

    function checkOverCycleEnd(current) {
        if(current.balls % 6 === 0 && current.balls > 0 && current.balls < matchState.maxOvers * 6) {
            swapStrikeImmediate(current);
            document.getElementById("new-bowler-name").value = "";
            document.getElementById("bowler-modal").style.display = "flex";
        } else if (current.balls >= matchState.maxOvers * 6) {
            current.timeline.push("🏁 Innings fully completed!");
        }
    }

    function confirmNewBowler() {
        let current = matchState.activeInnings === 1 ? matchState.inn1 : matchState.inn2;
        let bowlerName = document.getElementById("new-bowler-name").value.trim();
        
        document.getElementById("bowler-modal").style.display = "none";
        if(!bowlerName) bowlerName = `Bowler ${current.activeBowlersCount + 1}`;

        let bowlerIndex = current.bowlers.findIndex(b => b.name.toLowerCase() === bowlerName.toLowerCase());
        
        if(bowlerIndex !== -1) {
            current.currentBowler = bowlerIndex;
        } else {
            let nextSlot = current.activeBowlersCount;
            if(nextSlot < current.bowlers.length) {
                current.bowlers[nextSlot].name = bowlerName;
                current.currentBowler = nextSlot;
                current.activeBowlersCount++;
            } else {
                current.currentBowler = 0; 
            }
        }

        current.currentOverBalls = []; 
        current.widesInCurrentOver = 0; 
        current.timeline.push(`🔚 Over complete. ${current.bowlers[current.currentBowler].name} steps up to bowl the next over.`);
        syncSystemState();
    }

    // --- SCOREBOARD PROFILE OVERWRITE ENGINE ---

    function toggleEditMode() {
        editMode = !editMode;
        const btn = document.getElementById('edit-mode-btn');
        btn.innerText = editMode ? "🔒 Save Changes & Lock Metrics" : "🔓 Open Manual Runs/Balls Overwrite Editor";
        btn.style.backgroundColor = editMode ? "#f59e0b" : "#10b981";
        syncSystemState();
    }

    function updatePlayerNameDirect(section, idx, newName) {
        let current = matchState.activeInnings === 1 ? matchState.inn1 : matchState.inn2;
        if(newName.trim() !== "") {
            current[section][idx].name = newName.trim();
            localStorage.setItem(CACHE_KEY, JSON.stringify(matchState));
            // Update matchup display banner instantly without tearing down focus inputs
            renderMatchupStrip(current);
        }
    }

    function directFieldUpdate(section, idx, metric, value) {
        let current = matchState.activeInnings === 1 ? matchState.inn1 : matchState.inn2;
        if(section === 'meta') {
            if(metric === 'balls') current.balls = parseInt(value) || 0;
            if(metric === 'runs') current.runs = parseInt(value) || 0;
            if(metric === 'wickets') current.wickets = parseInt(value) || 0;
            if(metric === 'widesInCurrentOver') current.widesInCurrentOver = parseInt(value) || 0;
        } else {
            current[section][idx][metric] = parseInt(value) || 0;
        }
        localStorage.setItem(CACHE_KEY, JSON.stringify(matchState));
    }

    function renderMatchupStrip(current) {
        let activeStrikerName = current.batsmen[current.currentStriker] ? current.batsmen[current.currentStriker].name : "None";
        let activeNonStrikerName = current.batsmen[current.currentNonStriker] ? current.batsmen[current.currentNonStriker].name : "None";
        let activeBowlerName = current.bowlers[current.currentBowler] ? current.bowlers[current.currentBowler].name : "None";
        
        document.getElementById('matchup-strip-ui').innerHTML = `
            <div class="matchup-item active-status">🏏 Striker: ${activeStrikerName}</div>
            <div class="matchup-item" style="background:#475569;">🛡️ Non-Striker: ${activeNonStrikerName}</div>
            <div class="matchup-item active-status" style="border-left: 3px solid #ef4444;">🍒 Bowler: ${activeBowlerName}</div>
        `;
    }

    // --- SYSTEM VIEW RENDERING ENGINE ---

    function renderViewDOM() {
        let current = matchState.activeInnings === 1 ? matchState.inn1 : matchState.inn2;
        
        document.getElementById('match-title').innerText = `${matchState.team1} vs ${matchState.team2}`;

        // Dynamic targets calculations
        const targetElement = document.getElementById('target-ui');
        if(matchState.activeInnings === 2) {
            targetElement.style.display = "inline-block";
            let diff = (matchState.inn1.runs + 1) - matchState.inn2.runs;
            targetElement.innerText = diff > 0 ? `CHASE TARGET: Innings 2 needs ${diff} runs off ${(matchState.maxOvers * 6 - current.balls)} balls to win.` : `💥 VICTORY! Target achieved successfully!`;
        } else {
            targetElement.style.display = "none";
        }

        let overSequence = current.currentOverBalls.length > 0 ? current.currentOverBalls.join(" | ") : "None yet";
        
        let scoreDisplayHTML = "";
        if(editMode) {
            scoreDisplayHTML = `
                <div class="dashboard-edit-grid">
                    <div>Runs: <input type="number" class="edit-input" value="${current.runs}" oninput="directFieldUpdate('meta',0,'runs',this.value)"></div>
                    <div>Wickets: <input type="number" class="edit-input" value="${current.wickets}" oninput="directFieldUpdate('meta',0,'wickets',this.value)"></div>
                    <div>Total Deliveries: <input type="number" class="edit-input" value="${current.balls}" oninput="directFieldUpdate('meta',0,'balls',this.value)"></div>
                </div>
                <div class="this-over-box">
                    <b>This Over:</b> [ ${overSequence} ] 
                    <span style="color:#cbd5e1; margin-left:15px;">Wides In Over: <input type="number" class="edit-input" style="width:45px;" value="${current.widesInCurrentOver}" oninput="directFieldUpdate('meta',0,'widesInCurrentOver',this.value)"></span>
                </div>`;
        } else {
            let parsedOvers = Math.floor(current.balls / 6) + "." + (current.balls % 6);
            scoreDisplayHTML = `
                <div class="main-score">${current.runs} / ${current.wickets}</div>
                <div style="font-size: 1.2rem; font-weight: 600;">Overs: ${parsedOvers}</div>
                <div class="this-over-box"><b>This Over History:</b> [ ${overSequence} ] <span style="color:#f59e0b; margin-left:15px;"><b>Wides In Over:</b> ${current.widesInCurrentOver}</span></div>`;
        }
        document.getElementById('score-display-wrapper').innerHTML = scoreDisplayHTML;

        // Render Matchup Banner Panel strip
        renderMatchupStrip(current);

        // Process Batting Lists
        let batHTML = "";
        current.batsmen.forEach((b, idx) => {
            let rowStyle = (idx === current.currentStriker && !editMode) ? 'class="active-player"' : '';
            if (idx === current.currentNonStriker && !editMode) rowStyle = 'style="background-color: #2a3a52;"';
            let strikeRate = b.balls > 0 ? ((b.runs / b.balls) * 100).toFixed(2) : "0.00";

            let nameField = `<input type="text" class="edit-input name-input" value="${b.name}" oninput="updatePlayerNameDirect('batsmen', ${idx}, this.value)">`;

            if(editMode) {
                batHTML += `<tr>
                    <td>${nameField}</td>
                    <td><input type="number" class="edit-input" value="${b.runs}" oninput="directFieldUpdate('batsmen', ${idx}, 'runs', this.value)"></td>
                    <td><input type="number" class="edit-input" value="${b.balls}" oninput="directFieldUpdate('batsmen', ${idx}, 'balls', this.value)"></td>
                    <td><input type="number" class="edit-input" value="${b.fours}" oninput="directFieldUpdate('batsmen', ${idx}, 'fours', this.value)"></td>
                    <td><input type="number" class="edit-input" value="${b.sixes}" oninput="directFieldUpdate('batsmen', ${idx}, 'sixes', this.value)"></td>
                    <td>${strikeRate}</td>
                </tr>`;
            } else {
                batHTML += `<tr ${rowStyle}>
                    <td>${nameField} ${idx === current.currentStriker ? '🏏' : ''}</td>
                    <td>${b.runs}</td><td>${b.balls}</td><td>${b.fours}</td><td>${b.sixes}</td><td>${strikeRate}</td>
                </tr>`;
            }
        });
        document.getElementById('batting-body').innerHTML = batHTML;

        // Process Bowling Attack Cards with Economy
        let bowlHTML = "";
        current.bowlers.forEach((b, idx) => {
            if(idx >= current.activeBowlersCount && idx !== current.currentBowler && !editMode) return;
            
            let rowStyle = (idx === current.currentBowler && !editMode) ? 'class="active-player"' : '';
            let oversCount = Math.floor(b.currentBalls / 6) + "." + (b.currentBalls % 6);
            let economy = b.currentBalls > 0 ? ((b.runs / b.currentBalls) * 6).toFixed(2) : "0.00";

            let nameField = `<input type="text" class="edit-input name-input" value="${b.name}" oninput="updatePlayerNameDirect('bowlers', ${idx}, this.value)">`;

            if(editMode) {
                bowlHTML += `<tr>
                    <td>${nameField}</td>
                    <td><input type="number" class="edit-input" value="${b.currentBalls}" oninput="directFieldUpdate('bowlers', ${idx}, 'currentBalls', this.value)"></td>
                    <td><input type="number" class="edit-input" value="${b.runs}" oninput="directFieldUpdate('bowlers', ${idx}, 'runs', this.value)"></td>
                    <td><input type="number" class="edit-input" value="${b.wickets}" oninput="directFieldUpdate('bowlers', ${idx}, 'wickets', this.value)"></td>
                    <td>${economy}</td>
                </tr>`;
            } else {
                bowlHTML += `<tr ${rowStyle}>
                    <td>${nameField} ${idx === current.currentBowler ? '🍒' : ''}</td>
                    <td>${oversCount}</td><td>${b.runs}</td><td>${b.wickets}</td><td>${economy}</td>
                </tr>`;
            }
        });
        document.getElementById('bowling-body').innerHTML = bowlHTML;

        // Build commentary timelines
        let timelineHTML = "";
        current.timeline.slice().reverse().forEach(entry => {
            timelineHTML += `<div class="commentary-line">${entry}</div>`;
        });
        document.getElementById('commentary-box').innerHTML = timelineHTML;
    }

    function editTeamNames() {
        let t1 = prompt("Set Title for Team 1:", matchState.team1);
        let t2 = prompt("Set Title for Team 2:", matchState.team2);
        if(t1) matchState.team1 = t1;
        if(t2) matchState.team2 = t2;
        syncSystemState();
    }

    function resetMatch() {
        if(confirm("Completely wipe match metadata clean?")) {
            matchState.inn1 = createBlankInningsProfile();
            matchState.inn2 = createBlankInningsProfile();
            matchState.activeInnings = 1;
            syncSystemState();
        }
    }

    renderViewDOM();
</script>

</body>
</html>
