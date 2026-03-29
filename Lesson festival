<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Festivals Around the World | Interactive ESL Lesson</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #f5f7fa 0%, #e9edf2 100%);
            padding: 30px 20px;
            color: #1e2a3e;
        }

        .container {
            max-width: 1300px;
            margin: 0 auto;
        }

        /* Header / Title */
        .header {
            text-align: center;
            margin-bottom: 30px;
        }

        .header h1 {
            font-size: 2.2rem;
            background: linear-gradient(135deg, #d44c2f, #8b3c2c);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            margin-bottom: 8px;
        }

        .header p {
            color: #4a627a;
            font-size: 1.1rem;
        }

        .badge-timer {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 12px;
            flex-wrap: wrap;
        }

        .badge {
            background: #2c3e50;
            color: white;
            padding: 6px 16px;
            border-radius: 40px;
            font-size: 0.85rem;
            font-weight: 500;
        }

        /* Cards and sections */
        .section {
            background: white;
            border-radius: 32px;
            box-shadow: 0 12px 28px rgba(0,0,0,0.08);
            margin-bottom: 35px;
            overflow: hidden;
            transition: all 0.2s;
        }

        .section-title {
            background: #fef4e8;
            padding: 18px 28px;
            border-left: 8px solid #d44c2f;
            font-size: 1.5rem;
            font-weight: 700;
            display: flex;
            align-items: center;
            gap: 12px;
            flex-wrap: wrap;
        }

        .section-title span {
            background: #d44c2f20;
            border-radius: 60px;
            padding: 4px 12px;
            font-size: 0.85rem;
            font-weight: normal;
            color: #b33a1c;
        }

        .section-content {
            padding: 24px 28px;
        }

        /* Festival Gallery (Warm-up) */
        .festival-gallery {
            display: flex;
            flex-wrap: wrap;
            gap: 24px;
            justify-content: center;
            margin: 20px 0;
        }

        .festival-card {
            flex: 1;
            min-width: 240px;
            background: #fefaf5;
            border-radius: 28px;
            overflow: hidden;
            box-shadow: 0 6px 14px rgba(0,0,0,0.05);
            cursor: pointer;
            transition: transform 0.2s, box-shadow 0.2s;
            border: 2px solid transparent;
        }

        .festival-card.selected {
            border: 3px solid #d44c2f;
            background: #fff6ed;
            transform: scale(1.01);
        }

        .festival-img {
            width: 100%;
            height: 180px;
            object-fit: cover;
            background: #d9c7b0;
        }

        .festival-card h4 {
            padding: 16px 16px 8px;
            font-size: 1.2rem;
        }

        .festival-card p {
            padding: 0 16px 16px;
            color: #5d6e7e;
            font-size: 0.9rem;
        }

        /* Match game */
        .match-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            justify-content: space-between;
        }

        .match-col {
            flex: 1;
            min-width: 200px;
            background: #f8f9fc;
            border-radius: 24px;
            padding: 15px;
        }

        .match-item {
            background: white;
            border: 1px solid #e2e8f0;
            border-radius: 60px;
            padding: 12px 18px;
            margin-bottom: 12px;
            cursor: pointer;
            transition: all 0.2s;
            text-align: center;
            font-weight: 500;
            box-shadow: 0 1px 2px rgba(0,0,0,0.02);
        }

        .match-item:hover {
            background: #fff0e6;
            transform: translateX(4px);
        }

        .match-item.selected-match {
            background: #d44c2f;
            color: white;
            border-color: #d44c2f;
        }

        .match-feedback {
            margin-top: 20px;
            font-weight: bold;
            text-align: center;
            background: #eef2ff;
            padding: 12px;
            border-radius: 48px;
        }

        /* Reading + Jigsaw rooms */
        .jigsaw-row {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            margin: 20px 0;
        }

        .jigsaw-card {
            flex: 1;
            background: #fef7e0;
            border-radius: 24px;
            padding: 20px;
            border-top: 6px solid #e67e22;
        }

        .jigsaw-card h3 {
            margin-bottom: 12px;
            color: #a6512a;
        }

        .adj-input {
            margin-top: 16px;
            display: flex;
            gap: 8px;
            flex-wrap: wrap;
            align-items: center;
        }

        .adj-input input {
            flex: 1;
            padding: 10px;
            border-radius: 40px;
            border: 1px solid #ccc;
        }

        .adj-feedback {
            font-size: 0.8rem;
            margin-top: 8px;
            color: #2c6e2c;
        }

        /* Grammar interactive */
        .grammar-ex {
            background: #f1f5f9;
            border-radius: 24px;
            padding: 20px;
            margin: 15px 0;
        }

        .grammar-question {
            background: white;
            margin-bottom: 16px;
            padding: 16px;
            border-radius: 20px;
            box-shadow: 0 1px 3px rgba(0,0,0,0.05);
        }

        .grammar-question p {
            font-weight: 600;
            margin-bottom: 10px;
        }

        .grammar-options {
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
            align-items: center;
        }

        .grammar-options button {
            background: #edf2f7;
            border: none;
            padding: 8px 18px;
            border-radius: 40px;
            cursor: pointer;
            font-weight: 500;
            transition: 0.1s;
        }

        .grammar-options button.correct-choice {
            background: #2b9348;
            color: white;
        }

        .grammar-options button.wrong-choice {
            background: #d62828;
            color: white;
        }

        /* True or false game */
        .tf-grid {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
            justify-content: center;
            margin-bottom: 20px;
        }

        .tf-card {
            background: #f2f0e6;
            border-radius: 28px;
            padding: 20px;
            flex: 1;
            text-align: center;
        }

        .tf-buttons {
            display: flex;
            gap: 16px;
            justify-content: center;
            margin: 15px 0;
        }

        .tf-btn {
            font-size: 1.3rem;
            padding: 8px 24px;
            border: none;
            border-radius: 60px;
            font-weight: bold;
            cursor: pointer;
        }

        .tf-true {
            background: #2e7d32;
            color: white;
        }

        .tf-false {
            background: #c62828;
            color: white;
        }

        .tf-result {
            font-weight: bold;
            margin-top: 12px;
        }

        /* Spinner / My Perfect Festival */
        .spinner-area {
            text-align: center;
            background: #faeecd;
            border-radius: 32px;
            padding: 20px;
        }

        .wheel-options {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            margin: 20px 0;
        }

        .wheel-cat {
            background: white;
            border-radius: 28px;
            padding: 12px;
            width: 180px;
        }

        .spin-btn {
            background: #d44c2f;
            border: none;
            color: white;
            padding: 12px 28px;
            border-radius: 60px;
            font-size: 1.1rem;
            font-weight: bold;
            cursor: pointer;
            margin: 15px;
        }

        .festival-speech {
            background: #fff;
            border-radius: 28px;
            padding: 20px;
            margin-top: 20px;
            font-style: italic;
            border-left: 6px solid #d44c2f;
        }

        button {
            background: #2c3e50;
            color: white;
            border: none;
            border-radius: 60px;
            padding: 10px 20px;
            cursor: pointer;
            font-weight: 600;
        }

        .download-btn {
            background: #1e466e;
            display: inline-block;
            margin-top: 20px;
            text-align: center;
        }

        hr {
            margin: 20px 0;
        }

        @media (max-width: 700px) {
            .section-content {
                padding: 16px;
            }
        }
    </style>
</head>
<body>
<div class="container">
    <div class="header">
        <h1>🎭 Festivals Around the World 🌎</h1>
        <p>Interactive ESL Lesson | 50 minutes | Kukeri · Day of the Dead · La Tomatina</p>
        <div class="badge-timer">
            <div class="badge">⏱️ Online lesson</div>
            <div class="badge">📖 Based on authentic texts</div>
            <div class="badge">✨ Interactive tasks</div>
        </div>
    </div>

    <!-- 1. WARM-UP: Picture Detective -->
    <div class="section">
        <div class="section-title">
            🔍 1. WARM-UP: Picture Detective <span>speaking · 5 min</span>
        </div>
        <div class="section-content">
            <p><strong>👉 Click on a festival you find most exciting or scary!</strong> Share your guess with the class.</p>
            <div class="festival-gallery" id="festivalGallery">
                <div class="festival-card" data-fest="kukeri">
                    <img class="festival-img" src="https://placehold.co/400x200/e3b28c/5a3e2b?text=Kukeri+Mask+%26+Bells" alt="Kukeri Festival">
                    <h4>🎭 Kukeri (Bulgaria)</h4>
                    <p>Scary masks, bells, winter tradition</p>
                </div>
                <div class="festival-card" data-fest="daydead">
                    <img class="festival-img" src="https://placehold.co/400x200/f0c0a8/5a3e2b?text=Day+of+the+Dead+Altar" alt="Day of the Dead">
                    <h4>💀 Day of the Dead (Mexico)</h4>
                    <p>Altars, marigolds, skull face paint</p>
                </div>
                <div class="festival-card" data-fest="tomatina">
                    <img class="festival-img" src="https://placehold.co/400x200/e06648/ffffff?text=La+Tomatina+Tomato+Fight" alt="La Tomatina">
                    <h4>🍅 La Tomatina (Spain)</h4>
                    <p>Tomato fight, old clothes, last Wednesday of August</p>
                </div>
            </div>
            <div id="warmupMsg" style="margin-top: 12px; font-weight:500; text-align:center;"></div>
        </div>
    </div>

    <!-- 2. VOCABULARY: Match the word -->
    <div class="section">
        <div class="section-title">
            📖 2. MATCH THE WORD <span>vocabulary pre-teach</span>
        </div>
        <div class="section-content">
            <div class="match-grid">
                <div class="match-col">
                    <h4>🖼️ Pictures / Concepts</h4>
                    <div class="match-item" data-term="bell">🔔 A bell (loud noise)</div>
                    <div class="match-item" data-term="mask">🎭 Scary mask</div>
                    <div class="match-item" data-term="altar">🕯️ Altar with flowers</div>
                    <div class="match-item" data-term="spirit">👻 Spirit / ghost</div>
                    <div class="match-item" data-term="tomato">🍅 Tomato</div>
                    <div class="match-item" data-term="flower">🌼 Flower / marigold</div>
                </div>
                <div class="match-col">
                    <h4>📝 Words (click to match)</h4>
                    <div class="match-item" data-word="Spirits">Spirits</div>
                    <div class="match-item" data-word="Altar">Altar</div>
                    <div class="match-item" data-word="Bells">Bells</div>
                    <div class="match-item" data-word="Mask">Mask</div>
                    <div class="match-item" data-word="Tomatoes">Tomatoes</div>
                    <div class="match-item" data-word="Flowers">Flowers</div>
                </div>
            </div>
            <div class="match-feedback" id="matchFeedback">💡 Click a picture concept, then click a word to match.</div>
        </div>
    </div>

    <!-- 3. JIGSAW READING (3 texts + adjectives) -->
    <div class="section">
        <div class="section-title">
            📚 3. JIGSAW READING <span>breakout rooms style</span>
        </div>
        <div class="section-content">
            <div class="jigsaw-row">
                <div class="jigsaw-card">
                    <h3>🇧🇬 The Kukeri Festival</h3>
                    <p>The Kukeri Festival is one of the oldest traditions in Bulgaria. It happens every year in winter. Men wear special costumes and wear big, scary masks that look like animals. The men dance and make loud noises with bells. They do this to scare away bad spirits and bring good luck. Colourful and exciting.</p>
                    <div class="adj-input">
                        <input type="text" id="adjKukeri" placeholder="3 adjectives (e.g. scary, loud, colourful)" style="flex:2">
                        <button onclick="checkAdjectives('kukeri')">✅ Check</button>
                    </div>
                    <div id="feedbackKukeri" class="adj-feedback"></div>
                </div>
                <div class="jigsaw-card">
                    <h3>💀 The Day of the Dead (Mexico)</h3>
                    <p>November 1st & 2nd. People honour family members who died. Spirits come back to visit. Families make altars with photos, flowers, candles, food. Bread of the Dead is popular. Face painting like skeletons. Happy celebration, not sad.</p>
                    <div class="adj-input">
                        <input type="text" id="adjDead" placeholder="3 adjectives (e.g. colourful, happy, traditional)" style="flex:2">
                        <button onclick="checkAdjectives('dead')">✅ Check</button>
                    </div>
                    <div id="feedbackDead" class="adj-feedback"></div>
                </div>
                <div class="jigsaw-card">
                    <h3>🍅 La Tomatina (Spain)</h3>
                    <p>Last Wednesday of August in Buñol. Giant food fight with tomatoes. Lasts about 1 hour. Everyone wears old clothes. Before the fight: parades, music. Streets get covered in tomato juice, then cleaned.</p>
                    <div class="adj-input">
                        <input type="text" id="adjTomatina" placeholder="3 adjectives (fun, messy, loud...)" style="flex:2">
                        <button onclick="checkAdjectives('tomatina')">✅ Check</button>
                    </div>
                    <div id="feedbackTomatina" class="adj-feedback"></div>
                </div>
            </div>
            <p style="margin-top: 8px; font-size:0.85rem;">✨ Tip: share your adjectives with the group! Suggested answers: Kukeri: scary, noisy, colourful / Day of Dead: happy, colourful, traditional / Tomatina: messy, fun, wild.</p>
        </div>
    </div>

    <!-- 4. GRAMMAR: Present Simple vs Present Continuous -->
    <div class="section">
        <div class="section-title">
            ✍️ 4. GRAMMAR FOCUS <span>Present Simple / Continuous</span>
        </div>
        <div class="section-content">
            <div class="grammar-ex">
                <div class="grammar-question" id="gram1">
                    <p>1️⃣ Men __ (wear) scary masks <strong>every winter</strong>.</p>
                    <div class="grammar-options">
                        <button onclick="checkGrammar(this, 'wear')">wear</button>
                        <button onclick="checkGrammar(this, 'are wearing')">are wearing</button>
                        <button onclick="checkGrammar(this, 'wears')">wears</button>
                    </div>
                </div>
                <div class="grammar-question" id="gram2">
                    <p>2️⃣ Look at the photo! The men __ (dance) with bells <strong>right now</strong>.</p>
                    <div class="grammar-options">
                        <button onclick="checkGrammar(this, 'are dancing')">dance</button>
                        <button onclick="checkGrammar(this, 'are dancing')">are dancing</button>
                        <button onclick="checkGrammar(this, 'dances')">dances</button>
                    </div>
                </div>
                <div class="grammar-question" id="gram3">
                    <p>3️⃣ Families __ (make) altars <strong>every November</strong>.</p>
                    <div class="grammar-options">
                        <button onclick="checkGrammar(this, 'make')">make</button>
                        <button onclick="checkGrammar(this, 'are making')">are making</button>
                        <button onclick="checkGrammar(this, 'makes')">makes</button>
                    </div>
                </div>
                <div class="grammar-question" id="gram4">
                    <p>4️⃣ In this video, people __ (paint) their faces like skeletons.</p>
                    <div class="grammar-options">
                        <button onclick="checkGrammar(this, 'are painting')">paint</button>
                        <button onclick="checkGrammar(this, 'are painting')">are painting</button>
                        <button onclick="checkGrammar(this, 'paints')">paints</button>
                    </div>
                </div>
            </div>
            <div id="grammarGlobalMsg" style="text-align:center; font-weight:500;"></div>
        </div>
    </div>

    <!-- 5. TRUE OR FALSE GAME -->
    <div class="section">
        <div class="section-title">
            🎧 5. LISTENING: True or False? <span>thumbs up/down</span>
        </div>
        <div class="section-content">
            <div class="tf-grid">
                <div class="tf-card">
                    <p><strong>Statement 1:</strong> "The Kukeri Festival happens in summer to celebrate the sun."</p>
                    <div class="tf-buttons">
                        <button class="tf-btn tf-true" onclick="answerTF(1, false)">👍 TRUE</button>
                        <button class="tf-btn tf-false" onclick="answerTF(1, true)">👎 FALSE</button>
                    </div>
                    <div id="tf1Result" class="tf-result"></div>
                </div>
                <div class="tf-card">
                    <p><strong>Statement 2:</strong> "During The Day of the Dead, people in Mexico are sad because they remember their family."</p>
                    <div class="tf-buttons">
                        <button class="tf-btn tf-true" onclick="answerTF(2, false)">👍 TRUE</button>
                        <button class="tf-btn tf-false" onclick="answerTF(2, true)">👎 FALSE</button>
                    </div>
                    <div id="tf2Result" class="tf-result"></div>
                </div>
                <div class="tf-card">
                    <p><strong>Statement 3:</strong> "La Tomatina lasts for three days, and people wear new expensive clothes."</p>
                    <div class="tf-buttons">
                        <button class="tf-btn tf-true" onclick="answerTF(3, false)">👍 TRUE</button>
                        <button class="tf-btn tf-false" onclick="answerTF(3, true)">👎 FALSE</button>
                    </div>
                    <div id="tf3Result" class="tf-result"></div>
                </div>
            </div>
        </div>
    </div>

    <!-- 6. PRODUCTION: My Perfect Festival (Spinner style) -->
    <div class="section">
        <div class="section-title">
            🎡 6. MY PERFECT FESTIVAL <span>speaking & creativity</span>
        </div>
        <div class="section-content spinner-area">
            <div class="wheel-options">
                <div class="wheel-cat"><strong>📍 Where?</strong><br> 🏖️ Beach<br> 🌳 Park<br> 🏙️ City Streets</div>
                <div class="wheel-cat"><strong>🍅 What do we throw?</strong><br> 🍅 Tomatoes<br> 🌸 Flower petals<br> 💧 Colored powder</div>
                <div class="wheel-cat"><strong>✨ Why?</strong><br> 😈 Scare bad luck<br> 👨‍👩‍👧 Celebrate family<br> 🎉 Just for fun</div>
            </div>
            <button class="spin-btn" id="spinFestivalBtn">✨ Spin my unique festival ✨</button>
            <div id="festivalOutput" class="festival-speech">
                🎤 Click SPIN to create your festival! Then describe it: "My festival is at the beach. We throw flowers. We celebrate to bring happiness."
            </div>
        </div>
    </div>

    <!-- Download button for the whole interactive PDF/HTML -->
    <div style="text-align: center; margin: 30px 0 20px;">
        <button id="downloadPageBtn" style="background: #1f5e3a; padding: 12px 32px;">📥 Download this lesson as HTML (save & use offline)</button>
        <p style="margin-top: 10px; font-size: 0.75rem;">💡 Save as .html and open in browser — all interactive tasks work!</p>
    </div>
</div>

<script>
    // ---------- 1. WARM-UP SELECTION ----------
    const cards = document.querySelectorAll('.festival-card');
    const warmupMsg = document.getElementById('warmupMsg');
    cards.forEach(card => {
        card.addEventListener('click', () => {
            cards.forEach(c => c.classList.remove('selected'));
            card.classList.add('selected');
            const fest = card.getAttribute('data-fest');
            if(fest === 'kukeri') warmupMsg.innerHTML = '🎭 Great choice! Kukeri: scary masks, bells, winter in Bulgaria.';
            else if(fest === 'daydead') warmupMsg.innerHTML = '💀 Day of the Dead: colorful altars, happy remembrance.';
            else warmupMsg.innerHTML = '🍅 La Tomatina: tomato fight in Spain, very messy!';
        });
    });

    // ---------- 2. MATCHING GAME (picture-concept + word) ----------
    let selectedTerm = null;
    const termItems = document.querySelectorAll('[data-term]');
    const wordItems = document.querySelectorAll('[data-word]');
    const matchFeedback = document.getElementById('matchFeedback');
    let matchesMade = {};

    function resetMatchSelection() {
        termItems.forEach(t => t.classList.remove('selected-match'));
        wordItems.forEach(w => w.classList.remove('selected-match'));
    }

    termItems.forEach(term => {
        term.addEventListener('click', () => {
            resetMatchSelection();
            selectedTerm = term.getAttribute('data-term');
            term.classList.add('selected-match');
            matchFeedback.innerText = `✅ Selected: ${term.innerText}. Now click a matching word.`;
        });
    });

    wordItems.forEach(wordEl => {
        wordEl.addEventListener('click', () => {
            if (!selectedTerm) {
                matchFeedback.innerText = '⚠️ First click on a picture/concept (left side), then match with a word.';
                return;
            }
            const word = wordEl.getAttribute('data-word').toLowerCase();
            let correct = false;
            if (selectedTerm === 'bell' && word === 'bells') correct = true;
            else if (selectedTerm === 'mask' && word === 'mask') correct = true;
            else if (selectedTerm === 'altar' && word === 'altar') correct = true;
            else if (selectedTerm === 'spirit' && word === 'spirits') correct = true;
            else if (selectedTerm === 'tomato' && word === 'tomatoes') correct = true;
            else if (selectedTerm === 'flower' && word === 'flowers') correct = true;
            
            if (correct) {
                if (!matchesMade[selectedTerm+word]) {
                    matchesMade[selectedTerm+word] = true;
                    matchFeedback.innerHTML = `🎉 Correct match! "${wordEl.innerText}" ↔ "${document.querySelector('[data-term="'+selectedTerm+'"]').innerText}". Great!`;
                    wordEl.style.opacity = '0.6';
                    wordEl.style.textDecoration = 'line-through';
                } else {
                    matchFeedback.innerHTML = `🔄 Already matched! Try another pair.`;
                }
                resetMatchSelection();
                selectedTerm = null;
            } else {
                matchFeedback.innerHTML = `❌ Wrong! "${wordEl.innerText}" does not match "${document.querySelector('[data-term="'+selectedTerm+'"]').innerText}". Try again.`;
                resetMatchSelection();
                selectedTerm = null;
            }
        });
    });

    // 3. ADJECTIVES CHECK
    window.checkAdjectives = function(festival) {
        let input, feedback, expected = [];
        if(festival === 'kukeri') {
            input = document.getElementById('adjKukeri').value.toLowerCase();
            feedback = document.getElementById('feedbackKukeri');
            expected = ['scary', 'loud', 'colourful', 'noisy', 'exciting', 'traditional'];
        } else if(festival === 'dead') {
            input = document.getElementById('adjDead').value.toLowerCase();
            feedback = document.getElementById('feedbackDead');
            expected = ['happy', 'colourful', 'traditional', 'special', 'celebratory'];
        } else {
            input = document.getElementById('adjTomatina').value.toLowerCase();
            feedback = document.getElementById('feedbackTomatina');
            expected = ['fun', 'messy', 'loud', 'exciting', 'dirty', 'busy'];
        }
        let words = input.split(/[ ,]+/).filter(w => w.length>2);
        let found = words.filter(w => expected.includes(w));
        if(found.length >= 2) {
            feedback.innerHTML = `✅ Great adjectives! You have: ${found.slice(0,3).join(', ')}. Perfect!`;
        } else {
            feedback.innerHTML = `💡 Try to include adjectives like: ${expected.slice(0,4).join(', ')}. Re-read the text!`;
        }
    };

    // 4. GRAMMAR checker
    window.checkGrammar = function(btn, correctAnswer) {
        const parentDiv = btn.closest('.grammar-question');
        const btns = parentDiv.querySelectorAll('button');
        btns.forEach(b => {
            const btnText = b.innerText.toLowerCase().trim();
            const correctText = correctAnswer.toLowerCase().trim();
            if(btnText === correctText) {
                b.classList.add('correct-choice');
            } else {
                b.classList.add('wrong-choice');
            }
        });
        const globalMsg = document.getElementById('grammarGlobalMsg');
        globalMsg.innerHTML = '✅ Great! Present Simple = facts / habits; Present Continuous = now.';
        setTimeout(() => globalMsg.innerHTML = '', 2500);
    };

    // 5. TRUE OR FALSE
    window.answerTF = function(statementId, isCorrectFalse) {
        const resultDiv = document.getElementById(`tf${statementId}Result`);
        if(isCorrectFalse) {
            resultDiv.innerHTML = '✅ Correct! The statement is FALSE.';
            resultDiv.style.color = 'green';
        } else {
            resultDiv.innerHTML = '❌ Oops! That was incorrect. Check the texts again.';
            resultDiv.style.color = 'red';
        }
    };

    // 6. SPIN FESTIVAL
    const spinBtn = document.getElementById('spinFestivalBtn');
    const outputDiv = document.getElementById('festivalOutput');
    const whereOpts = ['at the beach', 'in a park', 'in city streets'];
    const throwOpts = ['throw tomatoes', 'throw flower petals', 'throw colored powder'];
    const whyOpts = ['to scare away bad luck', 'to celebrate family', 'just for fun'];
    
    spinBtn.addEventListener('click', () => {
        const randWhere = whereOpts[Math.floor(Math.random() * whereOpts.length)];
        const randThrow = throwOpts[Math.floor(Math.random() * throwOpts.length)];
        const randWhy = whyOpts[Math.floor(Math.random() * whyOpts.length)];
        outputDiv.innerHTML = `🎉 MY FESTIVAL: It happens ${randWhere}. People ${randThrow}. They do it ${randWhy}. <br>✨ Now say: "My festival is ${randWhere}. We ${randThrow}. We do it ${randWhy}."`;
    });

    // DOWNLOAD AS HTML (full interactive snapshot)
    document.getElementById('downloadPageBtn').addEventListener('click', function() {
        const htmlContent = document.documentElement.outerHTML;
        const blob = new Blob([htmlContent], {type: 'text/html'});
        const a = document.createElement('a');
        const url = URL.createObjectURL(blob);
        a.href = url;
        a.download = 'festivals_interactive_lesson.html';
        document.body.appendChild(a);
        a.click();
        document.body.removeChild(a);
        URL.revokeObjectURL(url);
    });
</script>
</body>
</html>
