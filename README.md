<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Music Player</title>
    <style>
        .container {
            text-align: center;
            margin-top: 50px;
        }
        audio {
            width: 300px;
            margin-bottom: 20px;
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            background-color: #3498db;
            color: #fff;
            border: none;
            border-radius: 4px;
            transition: background-color 0.3s;
        }
        button:hover {
            background-color: #2980b9;
        }
    </style>
</head>
<body>

<div class="container">
    <audio id="audioPlayer" controls>
        <source src="your-song.mp3" type="audio/mpeg">
        Your browser does not support the audio element.
    </audio>
    <button id="playPauseBtn">Play</button>
</div>

<script>
    var audioPlayer = document.getElementById("audioPlayer");
    var playPauseBtn = document.getElementById("playPauseBtn");

    function togglePlay() {
        if (audioPlayer.paused) {
            audioPlayer.play();
            playPauseBtn.textContent = "Pause";
        } else {
            audioPlayer.pause();
            playPauseBtn.textContent = "Play";
        }
    }

    playPauseBtn.addEventListener("click", togglePlay);
</script>

</body>
</html>
