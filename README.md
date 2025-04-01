<!DOCTYPE html><html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Kalbi Güzelim</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to bottom, #3b2f2f, #1c1c1c);
      color: white;
      text-align: center;
      background-image: url('https://images.unsplash.com/photo-1603297632222-97c2a7fe9dc7?ixlib=rb-4.0.3&auto=format&fit=crop&w=1950&q=80');
      background-size: cover;
      background-position: center;
    }
    h1 {
      margin-top: 80px;
      font-size: 2.5em;
    }
    .emoji {
      font-size: 2em;
    }
    #countdown {
      font-size: 1.8em;
      margin-top: 20px;
    }
    #surprise {
      margin-top: 40px;
      padding: 15px 25px;
      background-color: #ffffff22;
      border: none;
      border-radius: 10px;
      color: white;
      font-size: 1.2em;
      cursor: pointer;
    }
    #messageBox {
      display: none;
      margin-top: 20px;
      font-size: 1.5em;
      color: #ffdddd;
    }
  </style>
</head>
<body>
  <div class="emoji">" 🌸 ❤ 🧸"</div>
  <h1>Doğum günün kutlu olsun Kalbi Güzelim</h1>
  <div id="countdown"></div>
  <button id="surprise">Mesaja bak</button>
  <div id="messageBox">Gönlü Güzel Kendi Güzel Sevdiğim</div>  <script>
    const countdownEl = document.getElementById('countdown');
    const now = new Date();
    const endOfDay = new Date();
    endOfDay.setHours(23, 59, 59, 999);

    function updateCountdown() {
      const now = new Date();
      const diff = endOfDay - now;

      if (diff <= 0) {
        countdownEl.textContent = 'Gün bitti ama sevgim sonsuz!';
        clearInterval(timer);
        return;
      }

      const hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
      const minutes = Math.floor((diff / (1000 * 60)) % 60);
      const seconds = Math.floor((diff / 1000) % 60);

      countdownEl.textContent = Günün bitmesine: ${hours} saat ${minutes} dakika ${seconds} saniye kaldı.;
    }

    const timer = setInterval(updateCountdown, 1000);
    updateCountdown();

    document.getElementById('surprise').addEventListener('click', () => {
      const msgBox = document.getElementById('messageBox');
      msgBox.style.display = 'block';
    });
  </script></body>
</html>
