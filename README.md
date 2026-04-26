<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Verifying Pro Access</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      padding-top: 100px;
      background: #0f172a;
      color: white;
      margin: 0;
    }
   .loader {
      border: 4px solid #334155;
      border-top: 4px solid #3b82f6;
      border-radius: 50%;
      width: 40px;
      height: 40px;
      animation: spin 1s linear infinite;
      margin: 20px auto;
    }
    @keyframes spin {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }
   .container {
      max-width: 400px;
      margin: 0 auto;
      padding: 20px;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>Verifying Pro Access...</h2>
    <div class="loader"></div>
    <p>Please wait. Redirecting to Mileage Calculator</p>
    <p id="code" style="color:#64748b; font-size:12px; margin-top:30px;"></p>
  </div>

  <script>
    const path = window.location.pathname;
    const code = path.split('/')[1] || 'FREE-TRIAL';
    document.getElementById('code').innerText = 'License: ' + code;
    setTimeout(function() {
      window.location.href = 'https://mileage.artisandev.cloud?ref=' + code;
    }, 2500);
  </script>
</body>
</html>
