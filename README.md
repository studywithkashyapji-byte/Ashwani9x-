<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ashwani9x  Profile</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    
    <style>
        /* --- RESET & BASIC SETUP --- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        body {
            background-color: #050505;
            color: white;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow-x: hidden;
            position: relative;
        }

        /* --- BACKGROUND EFFECTS (Stars & Grid) --- */
        .bg-effects {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            background: radial-gradient(circle at center, #1a1a2e 0%, #000000 100%);
        }

        /* Retro Grid Floor Effect */
        .grid-floor {
            position: absolute;
            bottom: -100px;
            left: -50%;
            width: 200%;
            height: 50vh;
            background-image: 
                linear-gradient(rgba(0, 255, 213, 0.1) 1px, transparent 1px),
                linear-gradient(90deg, rgba(0, 255, 213, 0.1) 1px, transparent 1px);
            background-size: 50px 50px;
            transform: perspective(500px) rotateX(60deg);
            mask-image: linear-gradient(to top, rgba(0,0,0,1) 0%, transparent 100%);
            pointer-events: none;
        }

        /* --- MAIN CARD CONTAINER --- */
        .card {
            background: rgba(20, 20, 25, 0.6);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 40px 20px;
            width: 90%;
            max-width: 400px;
            text-align: center;
            box-shadow: 0 0 30px rgba(0, 255, 213, 0.1);
            position: relative;
            z-index: 1;
            margin: 20px 0;
        }

        /* --- PROFILE IMAGE --- */
        .profile-container {
            position: relative;
            width: 120px;
            height: 120px;
            margin: 0 auto 20px;
        }

        .profile-img {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            object-fit: cover;
            /* Gradient Border Effect */
            border: 3px solid transparent;
            background: linear-gradient(#141419, #141419) padding-box,
                        linear-gradient(45deg, #00f3ff, #bc13fe) border-box;
            box-shadow: 0 0 20px rgba(0, 243, 255, 0.4);
        }

        /* --- TYPOGRAPHY --- */
        h1 {
            font-size: 24px;
            font-weight: 700;
            margin-bottom: 5px;
            color: #fff;
        }

        h1 span {
            color: #00f3ff; /* Cyan color for 'Trader' */
            text-shadow: 0 0 10px rgba(0, 243, 255, 0.5);
        }

        .subtitle {
            font-size: 12px;
            color: #a0a0a0;
            letter-spacing: 2px;
            font-weight: 600;
            margin-bottom: 20px;
            text-transform: uppercase;
        }

        /* --- STATUS BADGE --- */
        .status-badge {
            display: inline-block;
            background: #000;
            border: 1px solid #00f3ff;
            color: #00f3ff;
            padding: 8px 20px;
            border-radius: 50px;
            font-size: 12px;
            font-weight: 700;
            box-shadow: 0 0 10px rgba(0, 243, 255, 0.2);
            margin-bottom: 30px;
        }

        .status-dot {
            display: inline-block;
            width: 8px;
            height: 8px;
            background-color: #00f3ff;
            border-radius: 50%;
            margin-right: 5px;
            box-shadow: 0 0 5px #00f3ff;
        }

        /* --- FREE FIRE ID BOX --- */
        .id-box {
            background: linear-gradient(180deg, rgba(40, 30, 20, 0.8) 0%, rgba(20, 20, 20, 0.8) 100%);
            border: 1px solid #c48a3c;
            border-radius: 12px;
            padding: 15px;
            margin-bottom: 25px;
            cursor: pointer;
            transition: transform 0.2s, box-shadow 0.2s;
            position: relative;
            overflow: hidden;
        }

        .id-box:active {
            transform: scale(0.98);
        }

        .id-label {
            color: #ffb700;
            font-size: 12px;
            font-weight: 700;
            display: block;
            margin-bottom: 5px;
            text-transform: uppercase;
        }

        .id-number {
            font-size: 28px;
            font-weight: 700;
            color: #fff;
            letter-spacing: 3px;
            display: block;
            text-shadow: 0 0 10px rgba(196, 138, 60, 0.5);
        }

        .tap-hint {
            font-size: 10px;
            color: #aaa;
            margin-top: 5px;
            display: block;
        }

        /* --- SOCIAL BUTTONS --- */
        .social-btn {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 100%;
            padding: 15px;
            border-radius: 10px;
            margin-bottom: 12px;
            text-decoration: none;
            color: white;
            font-weight: 600;
            font-size: 14px;
            transition: transform 0.2s;
            border: 1px solid rgba(255,255,255,0.1);
        }

        .social-btn:hover {
            transform: translateY(-2px);
        }

        .social-btn i {
            margin-right: 10px;
            font-size: 18px;
        }

        /* Button Specific Colors */
        .btn-insta {
            background: linear-gradient(45deg, #400b2e, #581238);
            border-color: #8a2387;
            box-shadow: 0 4px 15px rgba(138, 35, 135, 0.2);
        }
        
        .btn-telegram {
            background: linear-gradient(45deg, #0e2a47, #12365c);
            border-color: #1e5a96;
            box-shadow: 0 4px 15px rgba(30, 90, 150, 0.2);
        }

        .btn-youtube {
            background: linear-gradient(45deg, #4a0e0e, #6e1212);
            border-color: #b31217;
            box-shadow: 0 4px 15px rgba(179, 18, 23, 0.2);
        }

        .btn-whatsapp {
            background: linear-gradient(45deg, #0b3a24, #0f4d2f);
            border-color: #25d366;
            color: #aaa; /* Grayed out style per image */
            box-shadow: 0 4px 15px rgba(37, 211, 102, 0.1);
            cursor: not-allowed;
        }

        /* --- TOAST NOTIFICATION (Pop up) --- */
        #toast {
            visibility: hidden;
            min-width: 250px;
            background-color: #333;
            color: #fff;
            text-align: center;
            border-radius: 5px;
            padding: 16px;
            position: fixed;
            z-index: 10;
            bottom: 30px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 14px;
            border: 1px solid #00f3ff;
            box-shadow: 0 0 20px rgba(0, 243, 255, 0.3);
        }

        #toast.show {
            visibility: visible;
            animation: fadein 0.5s, fadeout 0.5s 2.5s;
        }

        @keyframes fadein {
            from {bottom: 0; opacity: 0;}
            to {bottom: 30px; opacity: 1;}
        }
        @keyframes fadeout {
            from {bottom: 30px; opacity: 1;}
            to {bottom: 0; opacity: 0;}
        }

    </style>
</head>
<body>

    <div class="bg-effects"></div>
    <div class="grid-floor"></div>

    <div class="card">
        <div class="profile-container">
            <img src="https://i.pinimg.com/736x/2b/a2/45/2ba2455ca817f7659e9ebfe9d494c5db.jpg" alt="Profile" class="profile-img">
        </div>

        <h1>Abhishek <span>Trader</span></h1>
        <p class="subtitle">PRO GAMER • CREATOR</p>

        <div class="status-badge">
            <span class="status-dot"></span> SYSTEM ONLINE
        </div>

        <div class="id-box" onclick="copyId()">
            <span class="id-label">FREE FIRE ID</span>
            <span class="id-number" id="ff-id-text">3376520212</span>
            <span class="tap-hint">TAP TO COPY</span>
        </div>

        <a href="https://instagram.com" target="_blank" class="social-btn btn-insta">
            <i class="fab fa-instagram"></i> Insta
        </a>

        <a href="https://telegram.org" target="_blank" class="social-btn btn-telegram">
            <i class="fab fa-telegram-plane"></i> Telegram
        </a>

        <a href="https://youtube.com" target="_blank" class="social-btn btn-youtube">
            <i class="fab fa-youtube"></i> Subscribe YouTube
        </a>

        <div class="social-btn btn-whatsapp">
            <i class="fab fa-whatsapp"></i> WhatsApp (Soon)
        </div>
    </div>

    <div id="toast">ID Copied to Clipboard!</div>

    <script>
        function copyId() {
            // Get the text field
            var copyText = document.getElementById("ff-id-text").innerText;

            // Copy the text inside the text field
            navigator.clipboard.writeText(copyText).then(function() {
                // Show the toast notification
                var x = document.getElementById("toast");
                x.className = "show";
                setTimeout(function(){ x.className = x.className.replace("show", ""); }, 3000);
            }, function(err) {
                console.error('Async: Could not copy text: ', err);
            });
        }
    </script>

</body>
</html>
