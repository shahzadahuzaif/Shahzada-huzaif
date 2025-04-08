<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Shahzada Huzaif - Personal Site</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f0f0f0;
      margin: 0;
    }

    header {
      background-color: #333;
      color: white;
      padding: 20px;
      text-align: center;
    }

    header p {
      margin-top: 5px;
      font-size: 1.1em;
      font-weight: bold;
      color: #ff3c3c;
    }

    nav a {
      color: white;
      margin: 0 15px;
      text-decoration: none;
      cursor: pointer;
    }

    .container {
      max-width: 600px;
      margin: 40px auto;
      background: white;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 0 10px #ccc;
      position: relative;
    }

    input, button {
      width: 100%;
      padding: 12px;
      margin-top: 10px;
      border-radius: 6px;
      border: 1px solid #ccc;
    }

    button {
      background: #333;
      color: white;
      border: none;
    }

    button:hover {
      background-color: #555;
    }

    .insta-btn {
      padding: 15px;
      font-size: 16px;
      background-color: #E1306C;
      color: white;
      border: none;
      border-radius: 8px;
      margin-top: 10px;
      cursor: pointer;
    }

    .hidden {
      display: none;
    }

    footer {
      background-color: #333;
      color: white;
      text-align: center;
      padding: 15px;
      position: fixed;
      width: 100%;
      bottom: 0;
    }

    .profile-img {
      width: 150px;
      height: 150px;
      object-fit: cover;
      display: block;
      margin: 0 auto 20px;
      box-shadow: 0 0 10px #aaa;
    }

    .arrow-nav {
      display: flex;
      justify-content: space-between;
      margin-top: 30px;
    }

    .arrow-btn {
      font-size: 24px;
      background: none;
      border: none;
      color: #333;
      cursor: pointer;
    }

    .arrow-btn:hover {
      color: #000;
    }
  </style>
  <script>
    let loggedIn = false;

    function showSection(sectionId) {
      if (!loggedIn && sectionId !== 'loginPage') {
        alert("Please login first");
        return;
      }
      document.querySelectorAll('.section').forEach(sec => sec.classList.add('hidden'));
      document.getElementById(sectionId).classList.remove('hidden');
    }

    function handleLogin(e) {
      e.preventDefault();
      loggedIn = true;
      showSection('profilePage');
    }
  </script>
</head>
<body>

  <header>
    <h1>Shahzada Huzaif</h1>
    <p>Shahzada Huzaif's Web — HACKER</p>
    <nav>
      <a onclick="showSection('loginPage')">Login</a>
      <a onclick="showSection('profilePage')">Profile</a>
      <a onclick="showSection('addressPage')">Address</a>
    </nav>
  </header>

  <div class="container section" id="loginPage">
    <h2>Login</h2>
    <form onsubmit="handleLogin(event)">
      <input type="text" placeholder="Username" required />
      <input type="password" placeholder="Password" required />
      <button type="submit">Login</button>
    </form>
    <div class="arrow-nav">
      <span></span>
      <button class="arrow-btn" onclick="showSection('profilePage')">→</button>
    </div>
  </div>

  <div class="container section hidden" id="profilePage">
    <img src="data:image/jpeg;base64,..." alt="Shahzada Huzaif" class="profile-img">
    <h2 style="text-align: center;">Welcome, Shahzada Huzaif</h2>
    <p><strong>Email:</strong> shahzadahuzaif4334@gmail.com</p>
    <p><strong>Profession:</strong> Web Developer</p>
    <p><strong>Bio:</strong> Passionate about coding, tech, and creativity.</p>
    <button onclick="showSection('addressPage')">View Address</button>
    <div class="arrow-nav">
      <button class="arrow-btn" onclick="showSection('loginPage')">←</button>
      <button class="arrow-btn" onclick="showSection('addressPage')">→</button>
    </div>
  </div>

  <div class="container section hidden" id="addressPage">
    <h2>Address & Personal Details</h2>
    <p><strong>Full Name:</strong> Shahzada Huzaif</p>
    <p><strong>House Number:</strong> 207</p>
    <p><strong>Village:</strong> Behibagh</p>
    <p><strong>District:</strong> Kulgam</p>
    <p><strong>State:</strong> Kashmir</p>
    <p><strong>Phone:</strong> 7006218862</p>
    <p><strong>Email:</strong> shahzadahuzaif4334@gmail.com</p>
    <p><strong>Hobbies:</strong><br>
      1. Hacking<br>
      2. Football<br>
      3. Online games and many more
    </p>
    <button class="insta-btn" onclick="window.location.href='https://www.instagram.com/_hacker__43_?igsh=OHh1cHZzb3A5NmI1'">
      Instagram Profile →
    </button>
    <div class="arrow-nav">
      <button class="arrow-btn" onclick="showSection('profilePage')">←</button>
      <span></span>
    </div>
  </div>

  <footer>
    <p>&copy; 2025 Shahzada Huzaif. All rights reserved.</p>
  </footer>

</body>
</html>
