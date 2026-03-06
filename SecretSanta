<!DOCTYPE html>
<html>
<head>
    <title>Secret Santa 2026</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: linear-gradient(to bottom, #0f1a2b, #1c2e4a);
            color: white;
            text-align: center;
            overflow: hidden;
        }

        .container {
            margin-top: 120px;
        }

        h1 {
            font-size: 36px;
        }

        input {
            padding: 12px;
            font-size: 16px;
            border-radius: 10px;
            border: none;
            width: 260px;
        }

        button {
            padding: 12px 25px;
            font-size: 16px;
            border-radius: 10px;
            border: none;
            background-color: #e63946;
            color: white;
            cursor: pointer;
            margin-top: 15px;
        }

        button:hover {
            background-color: #c92f3c;
        }

        #result {
            margin-top: 30px;
            font-size: 24px;
            font-weight: bold;
            min-height: 60px;
        }

        .snowflake {
            position: fixed;
            top: -10px;
            color: white;
            font-size: 12px;
            animation: fall linear infinite;
        }

        @keyframes fall {
            to {
                transform: translateY(110vh);
            }
        }
    </style>
</head>
<body>

<div class="container">
    <h1>🎄 Secret Santa 🎁</h1>
    <p>Enter your FULL NAME to reveal your person:</p>

    <input type="text" id="nameInput" placeholder="Enter your name">
    <br>
    <button onclick="revealSanta()">Reveal</button>

    <div id="result"></div>
</div>

<script>
    const assignments = {
        "AISHWINNIE": "IZZATI",
        "ALDRICK": "SUHAINA",
        "ANIS": "SUREKHASHREE",
        "IWANA": "ALYSHA",
        "DANISH": "ZAHIRAH",
        "AFIF": "NURIN",
        "AIREL": "ALDRICK",
        "AMALINA": "NAFISAH",
        "IZZATI": "SUFRI",
        "NURIN": "MADAM FAHARINA",
        "ALYA": "DANISH",
        "NAFISAH": "AISHWINNIE",
        "ALYSHA": "SURIA",
        "SUFRI": "ALYA",
        "SUHAINA": "ANIS",
        "SUREKHASHREE": "IWANA",
        "SURIA": "ZULAIKHA",
        "ZAHIRAH": "AFIF",
        "ZULAIKHA": "AMALINA",
        "MADAM FAHARINA": "AIREL"
    };

    function revealSanta() {
        let name = document.getElementById("nameInput").value.toUpperCase().trim();
        let resultDiv = document.getElementById("result");

        if (!assignments[name]) {
            resultDiv.innerHTML = "⚠️ Name not found. Please enter exactly as given.";
            return;
        }

        // Check if already revealed
        if (localStorage.getItem("revealed_" + name)) {
            resultDiv.innerHTML = "🔒 You have already revealed your Secret Santa person!";
            return;
        }

        // Show result
        resultDiv.innerHTML = "🎁 You got:<br><br>" + assignments[name];
        confettiEffect();

        // Lock it
        localStorage.setItem("revealed_" + name, "true");
    }

    function confettiEffect() {
        for (let i = 0; i < 80; i++) {
            let confetti = document.createElement("div");
            confetti.innerHTML = "🎉";
            confetti.style.position = "fixed";
            confetti.style.left = Math.random() * 100 + "vw";
            confetti.style.top = "-10px";
            confetti.style.fontSize = "20px";
            confetti.style.animation = "fall 3s linear forwards";
            document.body.appendChild(confetti);

            setTimeout(() => {
                confetti.remove();
            }, 3000);
        }
    }

    function createSnow() {
        for (let i = 0; i < 40; i++) {
            let snow = document.createElement("div");
            snow.classList.add("snowflake");
            snow.innerHTML = "❄";
            snow.style.left = Math.random() * 100 + "vw";
            snow.style.animationDuration = (Math.random() * 5 + 5) + "s";
            snow.style.opacity = Math.random();
            document.body.appendChild(snow);
        }
    }

    createSnow();
</script>

</body>
</html>
