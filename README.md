<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Foltech Solutions - Web Payment</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: #f4f9ff;
      margin: 0;
      padding: 0;
    }

    .container {
      max-width: 400px;
      margin: 50px auto;
      background: white;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    }

    h2 {
      color: #0056b3;
      text-align: center;
      margin-bottom: 25px;
    }

    label {
      display: block;
      margin-bottom: 6px;
      font-weight: 600;
      color: #333;
    }

    input[type="text"],
    input[type="email"],
    input[type="number"],
    input[type="tel"],
    input[type="month"] {
      width: 100%;
      padding: 10px;
      margin-bottom: 15px;
      border: 1px solid #ccc;
      border-radius: 8px;
      box-sizing: border-box;
      transition: border 0.3s;
    }

    input:focus {
      border-color: #007bff;
      outline: none;
    }

    .btn {
      background-color: #007bff;
      color: white;
      padding: 12px;
      width: 100%;
      border: none;
      border-radius: 8px;
      font-size: 16px;
      cursor: pointer;
      transition: background 0.3s;
    }

    .btn:hover {
      background-color: #0056b3;
    }

    .footer {
      text-align: center;
      margin-top: 20px;
      color: #777;
      font-size: 14px;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>Foltech Solutions Payment</h2>
    <form action="/submit-payment" method="POST">
      <label for="name">Full Name</label>
      <input type="text" id="name" name="name" required />

      <label for="email">Email Address</label>
      <input type="email" id="email" name="email" required />

      <label for="card">Card Number</label>
      <input type="tel" id="card" name="card" pattern="[0-9\s]{13,19}" inputmode="numeric" required placeholder="1234 5678 9012 3456"/>

      <label for="expiry">Expiry Date</label>
      <input type="month" id="expiry" name="expiry" required />

      <label for="cvv">CVV</label>
      <input type="text" id="cvv" name="cvv" maxlength="4" required />

      <button type="submit" class="btn">Pay Now</button>
    </form>
    <div class="footer">
      &copy; 2025 Foltech Solutions. All rights reserved.
    </div>
  </div>
</body>
</html>

