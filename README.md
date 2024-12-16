#<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CrumblyBliss - Christmas Edition</title>
  <style>
    /* General Styles */
    body {
      font-family: 'Arial', sans-serif;
      margin: 0;
      background-color: #f8f9fa;
      overflow-x: hidden;
    }

    /* Snow Animation */
    .snow {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 10;
    }

    .snowflake {
      position: absolute;
      top: -10px;
      font-size: 1.5rem;
      color: white;
      animation: fall linear infinite;
    }

    @keyframes fall {
      to {
        transform: translateY(100vh);
      }
    }

    /* Christmas Header */
    .christmas-header {
      background: linear-gradient(to right, #ff0000, #ff5733);
      color: white;
      text-align: center;
      padding: 20px;
    }

    .christmas-header h1 {
      font-size: 2.5rem;
      margin: 0;
    }

    .christmas-header p {
      font-size: 1.2rem;
      margin: 10px 0 0;
    }

    /* Main Content */
    .content {
      padding: 20px;
      text-align: center;
    }

    .promo {
      background: #fff3e0;
      border: 2px solid #ffa726;
      border-radius: 10px;
      padding: 15px;
      margin-bottom: 20px;
    }

    .shop-btn {
      background-color: #ff5722;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-size: 1rem;
    }

    .shop-btn:hover {
      background-color: #e64a19;
    }

    /* Product Grid */
    .product-grid {
      display: flex;
      justify-content: center;
      gap: 20px;
      flex-wrap: wrap;
    }

    .product {
      background: white;
      border: 1px solid #ddd;
      border-radius: 10px;
      padding: 10px;
      max-width: 200px;
      text-align: center;
    }

    .product img {
      width: 100%;
      border-radius: 10px;
    }

    .product h3 {
      font-size: 1.2rem;
      margin: 10px 0 5px;
    }

    .product p {
      color: #e91e63;
      font-weight: bold;
    }

    /* Christmas Footer */
    .christmas-footer {
      background-color: #ff7043;
      color: white;
      text-align: center;
      padding: 15px;
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <div class="snow"></div>
  <header class="christmas-header">
    <h1>🎄 Merry Christmas from CrumblyBliss! 🎅</h1>
    <p>Delicious cookies to make your holidays brighter!</p>
  </header>

  <main class="content">
    <section class="promo">
      <h2>🎁 Holiday Special</h2>
      <p>Get 25% off on all Christmas cookie boxes! Use code <b>HOLIDAY25</b>.</p>
      <button class="shop-btn">Shop Now</button>
    </section>
    <section class="products">
      <h2>Our Christmas Cookies</h2>
      <div class="product-grid">
        <div class="product">
          <img src="christmas-cookie1.jpg" alt="Christmas Cookie 1">
          <h3>Gingerbread Delight</h3>
          <p>$15.99</p>
        </div>
        <div class="product">
          <img src="christmas-cookie2.jpg" alt="Christmas Cookie 2">
          <h3>Chocolate Snowflakes</h3>
          <p>$12.99</p>
        </div>
        <div class="product">
          <img src="christmas-cookie3.jpg" alt="Christmas Cookie 3">
          <h3>Peppermint Bliss</h3>
          <p>$14.99</p>
        </div>
      </div>
    </section>
  </main>

  <footer class="christmas-footer">
    <p>© 2024 CrumblyBliss. Wishing you a sweet and joyous Christmas!</p>
  </footer>

  <script>
    // Snow Animation
    const snowContainer = document.querySelector('.snow');

    function createSnowflake() {
      const snowflake = document.createElement('div');
      snowflake.classList.add('snowflake');
      snowflake.style.left = Math.random() * 100 + 'vw';
      snowflake.style.animationDuration = Math.random() * 3 + 2 + 's';
      snowflake.innerText = '❄';
      snowContainer.appendChild(snowflake);

      setTimeout(() => {
        snowflake.remove();
      }, 5000);
    }

    setInterval(createSnowflake, 100);
  </script>
</body>
</html>
