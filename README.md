<!DvPJEqupezflXnzZVcbrEMPvxSuLwFlbjvPJEqupezflXnzZVcbrEMPvxSuLwF html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cas by Jans</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, #ff00cc, #3333ff);
            font-family: 'Arial Black', sans-serif;
            overflow: hidden;
        }
        .container {
            text-align: center;
            color: white;
        }
        button {
            font-size: 2.5rem;
            padding: 2rem 4rem;
            background: #ffff00;
            color: #000;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
            text-transform: uppercase;
            letter-spacing: 4px;
            transition: all 0.3s;
        }
        button:hover {
            transform: scale(1.1);
            box-shadow: 0 15px 40px rgba(255,255,0,0.6);
        }
        h1 {
            font-size: 3rem;
            margin-bottom: 2rem;
            text-shadow: 0 0 20px rgba(255,255,255,0.8);
        }
        .warning {
            margin-top: 3rem;
            font-size: 1.2rem;
            opacity: 0.9;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>CAS BY JANS</h1>
        <button onclick="startVibration()">CLICK FOR CAS BY JANS</button>
        <p class="warning">Warning: This will vibrate your phone nonstop.<br>Close the tab or browser to stop.</p>
    </div>

    <script>
        let vibrationInterval = null;
        
        function startVibration() {
            const button = document.querySelector('button');
            button.textContent = "VIBRATING... CLOSE TAB TO STOP";
            button.style.background = "#ff0000";
            button.style.color = "#fff";
            button.disabled = true;

            // Start continuous vibration using the Vibration API
            if ("vibrate" in navigator) {
                // Initial strong vibration
                navigator.vibrate(200);
                
                // Continuous loop
                vibrationInterval = setInterval(() => {
                    // Vibrate in a strong pattern that feels almost nonstop
                    navigator.vibrate([100, 50, 100, 50, 150]);
                }, 350);
                
                // Also request a long vibration (some browsers support it)
                navigator.vibrate(10000);
            } else {
                alert("Your device doesn't support vibration or you're not on mobile.");
            }
            
            // Add a visual effect
            document.body.style.animation = "pulse 0.4s infinite";
            
            // Create CSS animation for pulsing background
            const style = document.createElement('style');
            style.innerHTML = `
                @keyframes pulse {
                    0% { background: linear-gradient(135deg, #ff00cc, #3333ff); }
                    50% { background: linear-gradient(135# 2nd-project.v12-