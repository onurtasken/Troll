# Troll
Trool.html
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Video Oynatıcı</title>
    <style>
        body, html {
            height: 100%;
            margin: 0;
            padding: 0;
            overflow: hidden; /* Sayfayı kaydırmamayı sağlar */
        }
        iframe {
            width: 100%;
            height: 100%;
            border: none;
            display: none; /* Başlangıçta iframe gizli */
        }
        #startButton {
            font-size: 20px;
            padding: 10px 20px;
            cursor: pointer;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
        }
    </style>
</head>
<body>

    <button id="startButton" onclick="playVideo()">Video Başlat</button>

    <iframe id="videoPlayer" 
            src="https://www.youtube.com/embed/FR8_3DWHA-8?autoplay=1&mute=0" 
            allow="autoplay; encrypted-media" 
            allowfullscreen>
    </iframe>

    <script>
        function playVideo() {
            document.getElementById("videoPlayer").style.display = "block"; // Video başlatılınca iframe görünür hale gelir
            document.getElementById("startButton").style.display = "none"; // Buton gizlenir
        }

        // Geri tuşuna basıldığında engelleme uyarısı
        window.onbeforeunload = function() {
            return "Video izlerken sayfadan çıkmak istemediğinize emin misiniz?";
        };

    </script>

</body>
</html>
