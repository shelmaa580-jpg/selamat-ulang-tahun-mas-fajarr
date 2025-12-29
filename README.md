# selamat-ulang-tahun-mas-fajarr
ceamat ulang tahun cayang kuu 
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Mas Fajar!</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@400;700&family=Pacifico&display=swap');

        body {
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background: linear-gradient(135deg, #ff9a9e 0%, #fad0c4 99%, #fad0c4 100%);
            font-family: 'Quicksand', sans-serif;
            overflow: hidden;
            text-align: center;
        }

        /* Container Utama */
        .container {
            z-index: 10;
            background: rgba(255, 255, 255, 0.8);
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            max-width: 400px;
            border: 5px solid #ff6b6b;
        }

        h1 {
            color: #ff4757;
            font-family: 'Pacifico', cursive;
            font-size: 2.5em;
            margin-bottom: 10px;
        }

        .age {
            background: #ff6b6b;
            color: white;
            padding: 5px 15px;
            border-radius: 50px;
            font-weight: bold;
            display: inline-block;
            margin-bottom: 20px;
        }

        /* Animasi Amplop */
        .envelope-wrapper {
            cursor: pointer;
            transition: transform 0.3s;
        }

        .envelope-wrapper:hover {
            transform: scale(1.1);
        }

        .envelope-icon {
            font-size: 80px;
            color: #ff4757;
        }

        /* Modal Pesan */
        #message-box {
            display: none;
            animation: fadeIn 1s ease-in-out;
        }

        .heart {
            color: #ff4757;
            font-size: 20px;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Hiasan Latar Belakang */
        .bg-dots {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            z-index: 1;
            pointer-events: none;
        }
    </style>
</head>
<body>

    <div class="bg-dots" id="dots"></div>

    <div class="container">
        <div id="initial-view">
            <h1>Halo, Mas Fajar!</h1>
            <div class="age">22nd Birthday</div>
            <p>Ada surat manis untukmu di bawah ini...</p>
            <div class="envelope-wrapper" onclick="showMessage()">
                <div class="envelope-icon">✉️</div>
                <p><strong>Klik untuk buka</strong></p>
            </div>
        </div>

        <div id="message-box">
            <h1>Happy Birthday! 🎂</h1>
            <p style="font-size: 1.1em; line-height: 1.6; color: #444;">
                Selamat ulang tahun yang ke-22, <strong>Mas Fajar</strong> sayang! <span class="heart">❤️</span>
                <br><br>
                Harapanku, semoga Mas Fajar bisa mencapai semua cita-cita yang diimpikan. Aku berdoa semoga kamu bisa menjadi manusia yang 
                <strong>paling bahagia</strong> yang pernah aku kenal. 
                <br><br>
                Terima kasih sudah menjadi manusia baik hati yang selalu berhasil menyenangkan hati orang lain, terutama hatiku. 
                Tetaplah bersinar, ya!
            </p>
            <p style="font-family: 'Pacifico'; color: #ff4757;">- Dari Favoritmu ✨</p>
            <button onclick="location.reload()" style="border:none; background:#747d8c; color:white; padding:5px 10px; border-radius:5px; cursor:pointer;">Baca lagi</button>
        </div>
    </div>

    <script>
        function showMessage() {
            document.getElementById('initial-view').style.display = 'none';
            document.getElementById('message-box').style.display = 'block';
            createHearts();
        }

        // Efek hujan hati saat surat dibuka
        function createHearts() {
            for (let i = 0; i < 30; i++) {
                const heart = document.createElement('div');
                heart.innerHTML = '❤️';
                heart.style.position = 'fixed';
                heart.style.left = Math.random() * 100 + 'vw';
                heart.style.top = '-20px';
                heart.style.fontSize = (Math.random() * 20 + 10) + 'px';
                heart.style.animation = `fall ${Math.random() * 3 + 2}s linear forwards`;
                document.body.appendChild(heart);
            }
        }

        // CSS tambahan untuk animasi jatuh
        const style = document.createElement('style');
        style.innerHTML = `
            @keyframes fall {
                to { transform: translateY(110vh) rotate(360deg); }
            }
        `;
        document.head.appendChild(style);
    </script>
</body>
</html>
