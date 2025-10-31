<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Kyy Gntng | Login Sosial Media</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap');

    body {
      margin: 0;
      height: 100vh;
      font-family: 'Poppins', sans-serif;
      background: radial-gradient(circle at top, #0a0a0a 0%, #000 100%);
      color: white;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      overflow: hidden;
    }

    h1 {
      font-size: 3rem;
      text-shadow: 0 0 20px #00ffe0, 0 0 40px #00c8ff;
      animation: float 3s ease-in-out infinite;
    }

    @keyframes float {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-10px); }
    }

    .container {
      background: rgba(255,255,255,0.05);
      backdrop-filter: blur(10px);
      padding: 40px;
      border-radius: 20px;
      box-shadow: 0 0 20px rgba(0,255,255,0.3);
      text-align: center;
      animation: fadeIn 1s ease forwards;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: scale(0.9); }
      to { opacity: 1; transform: scale(1); }
    }

    button {
      margin: 10px;
      padding: 12px 30px;
      border: none;
      border-radius: 30px;
      font-size: 1.1rem;
      cursor: pointer;
      color: white;
      background: linear-gradient(90deg, #ff00cc, #3333ff);
      transition: transform 0.3s, box-shadow 0.3s;
    }

    button:hover {
      transform: scale(1.1) rotate(1deg);
      box-shadow: 0 0 20px #00fff2;
    }

    footer {
      position: absolute;
      bottom: 15px;
      font-size: 0.9rem;
      opacity: 0.6;
    }
  </style>
</head>
<body>
  <h1>Kyy Gntng</h1>

  <div class="container">
    <p>Login dengan sosial media kamu:</p>
    <button onclick="loginInstagram()">Login Instagram</button>
    <button onclick="loginTiktok()">Login TikTok</button>
  </div>

  <footer>© 2025 Kyy Gntng | Dark Elegan Edition</footer>

  <script>
    function loginInstagram() {
      const clientId = "YOUR_INSTAGRAM_CLIENT_ID";
      const redirectUri = window.location.origin + "/"; // arahkan balik ke halaman ini
      const scope = "user_profile,user_media";
      const authUrl = `https://www.instagram.com/kyy_546777?igsh=MTdlbHlwMWt5djh6Nw===${clientId}&redirect_uri=${encodeURIComponent(redirectUri)}&scope=${scope}&response_type=code`;
      window.location.href = authUrl;
    }

    function loginTiktok() {
      const clientKey = "YOUR_TIKTOK_CLIENT_KEY";
      const redirectUri = window.location.origin + "/";
      const scope = "user.info.basic";
      const state = Math.random().toString(36).substring(2);
      const authUrl = `https://vm.tiktok.com/ZSHcL3VsEFAyJ-UzMcJ/=${clientKey}&scope=${scope}&response_type=code&redirect_uri=${encodeURIComponent(redirectUri)}&state=${state}`;
      window.location.href = authUrl;
    }
  </script>
</body>
</html>
