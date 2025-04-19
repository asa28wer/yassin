<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>For Yassino</title>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script&display=swap" rel="stylesheet">
    <style>
        body {
            background-color: white;
            text-align: center;
            font-family: 'Dancing Script', cursive;
            margin: 0;
            padding: 0;
        }
        .hearts {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            overflow: hidden;
            z-index: -1;
        }
        .heart {
            width: 30px;
            height: 30px;
            background: yellow;
            position: absolute;
            transform: rotate(45deg);
            animation: float 10s infinite;
        }
        .heart::before,
        .heart::after {
            content: '';
            width: 30px;
            height: 30px;
            background: yellow;
            position: absolute;
            border-radius: 50%;
        }
        .heart::before {
            top: -15px;
            left: 0;
        }
        .heart::after {
            left: -15px;
            top: 0;
        }
        @keyframes float {
            0% {
                transform: translateY(100vh) rotate(45deg);
                opacity: 0;
            }
            50% {
                opacity: 1;
            }
            100% {
                transform: translateY(-10vh) rotate(45deg);
                opacity: 0;
            }
        }
        .cloud {
            display: inline-block;
            background: #ffc0cb; /* بيبي بينك */
            padding: 20px 40px;
            border-radius: 50px;
            position: relative;
            color: blue;
            font-size: 32px;
            margin: 40px auto 20px;
        }
        .cloud::before, .cloud::after {
            content: '';
            position: absolute;
            background: #ffc0cb; /* بيبي بينك */
            border-radius: 50%;
        }
        .cloud::before {
            width: 60px;
            height: 60px;
            top: -30px;
            left: 20px;
        }
        .cloud::after {
            width: 80px;
            height: 80px;
            top: -40px;
            right: 20px;
        }
        p {
            color: blue;
            margin: 20px;
            font-size: 30px;
        }
        button {
            padding: 15px 30px;
            font-size: 18px;
            background-color: blue;
            color: white;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            margin: 10px;
            font-family: 'Arial', sans-serif;
        }
        button:hover {
            background-color: darkblue;
        }
    </style>
</head>
<body>

<div class="hearts">
    <div class="heart" style="left:10%; animation-delay: 0s;"></div>
    <div class="heart" style="left:30%; animation-delay: 2s;"></div>
    <div class="heart" style="left:50%; animation-delay: 4s;"></div>
    <div class="heart" style="left:70%; animation-delay: 1s;"></div>
    <div class="heart" style="left:90%; animation-delay: 3s;"></div>
</div>

<div class="cloud">Hi yassino</div>
<p>I miss you</p>
<p>This site is for you</p>

<button onclick="playMusic()">Click Here</button>
<button onclick="showMessage()">Click Here</button>

<audio id="mySong" src="https://www.albumaty.com/n/download/53938" loop></audio>

<script>
    function playMusic() {
        var song = document.getElementById('mySong');
        song.play();
    }

    function showMessage() {
        alert("I love you");
    }
</script>

</body>
</html>
