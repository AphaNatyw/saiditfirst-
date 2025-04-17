<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>SaidItFirst - Entry Page</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: #f5f5f5;
    }

    .entry-container {
      text-align: center;
    }

    h1 {
      font-size: 3rem;
      margin-bottom: 20px;
      color: #222;
    }

    input[type="text"] {
      padding: 10px;
      font-size: 1.2rem;
      width: 300px;
      border: 2px solid #ddd;
      border-radius: 8px;
      margin-bottom: 20px;
    }

    button {
      padding: 10px 20px;
      font-size: 1rem;
      background-color: #007bff;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }

    button:hover {
      background-color: #0056b3;
    }
  </style>
</head>
<body>
  <div class="entry-container">
    <h1>SaidItFirst</h1>
    <input type="text" id="usernameInput" placeholder="Enter your username" />
    <br />
    <button onclick="goToHomePage()">Enter</button>
  </div>

  <script>
    function goToHomePage() {
      const username = document.getElementById('usernameInput').value;
      if (username.trim() !== '') {
        localStorage.setItem('username', username);
        window.location.href = 'homepage.html'; // Make sure homepage.html exists
      } else {
        alert('Please enter a username.');
      }
    }
  </script>
</body>
</html>
