<!DOCTYPE html>
<html>
<head>
<style>
    @import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap');

    body {
        background-color: #1a1a1a;
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
        margin: 0;
        font-family: 'Press+Start+2P', cursive;
        color: white;
    }

    /* Game Container */
    .game-screen {
        width: 600px;
        height: 450px;
        background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), 
                    url('https://images.unsplash.com/photo-1550745165-9bc0b252726f?auto=format&fit=crop&w=600&q=80'); /* Pixel Art Placeholder */
        background-size: cover;
        border: 8px solid #3d3d3d;
        position: relative;
        image-rendering: pixelated;
    }

    /* Dialogue Box */
    .text-box {
        position: absolute;
        bottom: 20px;
        left: 20px;
        right: 20px;
        background: rgba(40, 44, 52, 0.95);
        border: 4px solid #f1c40f;
        border-radius: 10px;
        padding: 20px;
        font-size: 12px;
        line-height: 1.8;
        box-shadow: 0 0 0 4px #282c34;
    }

    .cursor {
        display: inline-block;
        width: 10px;
        height: 15px;
        background: #f1c40f;
        animation: blink 0.8s infinite;
    }

    /* HUD Stats */
    .hud {
        position: absolute;
        top: 20px;
        left: 20px;
        display: flex;
        flex-direction: column;
        gap: 10px;
    }

    .stat-bar {
        width: 150px;
        height: 15px;
        background: #333;
        border: 2px solid #fff;
    }

    .hp-fill { width: 25%; background: #e74c3c; height: 100%; }
    .mp-fill { width: 60%; background: #3498db; height: 100%; }

    @keyframes blink { 0%, 100% { opacity: 1; } 50% { opacity: 0; } }

    /* Editable Text */
    [contenteditable]:focus { outline: none; }
</style>
</head>
<body>

<div class="game-screen">
    <div class="hud">
        <div>HP <div class="stat-bar"><div class="hp-fill"></div></div></div>
        <div>MP <div class="stat-bar"><div class="mp-fill"></div></div></div>
        <div style="font-size: 10px; color: #f1c40f; margin-top: 5px;">GOLD: ₱0.00</div>
    </div>

    <div class="text-box">
        <span contenteditable="true">
            The Hero CJ has been afflicted by the "SICKNESS" since January 13th! 
            <br><br>
            Her quest to celebrate her monthsary with LEXI is in peril! She must obtain the cure KISSPIRIN 💊 to recover.
        </span>
        <div class="cursor"></div>
    </div>
</div>

</body>
</html>
