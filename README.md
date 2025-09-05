<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Phone Shop - Temeta Fozo</title>

  <!-- Mobile App Capable -->
  <meta name="apple-mobile-web-app-capable" content="yes">
  <meta name="mobile-web-app-capable" content="yes">
  <meta name="apple-mobile-web-app-title" content="Phone Shop">
  <link rel="apple-touch-icon" href="https://via.placeholder.com/180.png?text=AppIcon">

  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #111;
      color: #fff;
      scroll-behavior: smooth;
    }

    header {
      background-color: #222;
      padding: 20px 0;
      text-align: center;
      position: sticky;
      top: 0;
      z-index: 100;
    }

    header h1 {
      margin: 0;
      font-size: 28px;
      color: gold;
      text-shadow: 0 0 10px gold;
    }

    nav {
      margin-top: 10px;
    }

    nav a {
      color: #ff4500;
      margin: 0 10px;
      text-decoration: none;
      font-weight: bold;
      font-size: 16px;
      transition: 0.3s;
    }

    nav a:hover {
      color: gold;
    }

    .search-container {
      margin: 15px 0;
      text-align: center;
    }

    .search-container input {
      padding: 10px;
      font-size: 16px;
      width: 80%;
      max-width: 300px;
      border-radius: 5px;
      border: none;
    }

    .category {
      padding: 15px;
      max-width: 1000px;
      margin: 0 auto;
    }

    .category h2 {
      margin-bottom: 10px;
      font-size: 22px;
      color: #fff;
      border-bottom: 2px solid gold;
      display: inline-block;
      padding-bottom: 5px;
    }

    .gallery {
      display: flex;
      flex-wrap: wrap;
      gap: 15px;
      justify-content: center;
    }

    .phone-card {
      position: relative;
      width: 45%;
      max-width: 250px;
      border-radius: 10px;
      overflow: hidden;
      box-shadow: 0 4px 10px rgba(0,0,0,0.6);
      transition: transform 0.3s;
      cursor: pointer;
      background-color: #000;
    }

    .phone-card:hover {
      transform: scale(1.05);
    }

    .phone-card img {
      width: 100%;
      height: auto;
      display: block;
    }

    .name-overlay {
      position: absolute;
      bottom: 50px;
      width: 100%;
      text-align: center;
      font-weight: bold;
      font-size: 18px;
      color: #ff4500;
      animation: fireGlow 1s infinite alternate;
    }

    .buy-button {
      position: absolute;
      bottom: 10px;
      left: 50%;
      transform: translateX(-50%);
      background-color: #ff4500;
      border: none;
      padding: 8px 16px;
      font-size: 16px;
      font-weight: bold;
      color: #fff;
      border-radius: 5px;
      cursor: pointer;
      text-decoration: none;
      animation: fireGlow 1s infinite alternate;
      box-shadow: 0 0 10px #ff6347, 0 0 20px #ff4500, 0 0 30px #ffa500;
    }

    @keyframes fireGlow {
      0%   { text-shadow: 0 0 5px #ff4500, 0 0 10px #ff6347, 0 0 15px #ff0000; }
      50%  { text-shadow: 0 0 10px #ff6347, 0 0 20px #ff4500, 0 0 25px #ff8c00; }
      100% { text-shadow: 0 0 15px #ff0000, 0 0 25px #ff6347, 0 0 35px #ffa500; }
    }

    @media (max-width: 480px) {
      .phone-card { width: 90%; }
      .phone-card img { height: auto; }
      header h1 { font-size: 24px; }
    }
  </style>
</head>
<body>
  <header>
    <h1>Phone Shop by Temeta Fozo</h1>
    <nav>
      <a href="#iphones">iPhones</a>
      <a href="#samsung">Samsung</a>
    </nav>
  </header>

  <div class="search-container">
    <input type="text" id="searchInput" placeholder="Search phones..." onkeyup="filterPhones()">
  </div>

  <div class="category" id="iphones">
    <h2>iPhones</h2>
    <div class="gallery" id="phoneGallery">
      <div class="phone-card" data-name="iPhone 14">
        <img src="https://via.placeholder.com/250x400?text=iPhone+14" alt="iPhone 14">
        <div class="name-overlay">Temeta Fozo</div>
        <a href="#" class="buy-button">Buy Now</a>
      </div>
      <div class="phone-card" data-name="iPhone 13">
        <img src="https://via.placeholder.com/250x400?text=iPhone+13" alt="iPhone 13">
        <div class="name-overlay">Temeta Fozo</div>
        <a href="#" class="buy-button">Buy Now</a>
      </div>
      <div class="phone-card" data-name="iPhone 12">
        <img src="https://via.placeholder.com/250x400?text=iPhone+12" alt="iPhone 12">
        <div class="name-overlay">Temeta Fozo</div>
        <a href="#" class="buy-button">Buy Now</a>
      </div>
    </div>
  </div>

  <div class="category" id="samsung">
    <h2>Samsung Phones</h2>
    <div class="gallery" id="phoneGallerySamsung">
      <div class="phone-card" data-name="Samsung S23">
        <img src="https://via.placeholder.com/250x400?text=Samsung+S23" alt="Samsung S23">
        <div class="name-overlay">Temeta Fozo</div>
        <a href="#" class="buy-button">Buy Now</a>
      </div>
      <div class="phone-card" data-name="Samsung S22">
        <img src="https://via.placeholder.com/250x400?text=Samsung+S22" alt="Samsung S22">
        <div class="name-overlay">Temeta Fozo</div>
        <a href="#" class="buy-button">Buy Now</a>
      </div>
      <div class="phone-card" data-name="Samsung S21">
        <img src="https://via.placeholder.com/250x400?text=Samsung+S21" alt="Samsung S21">
        <div class="name-overlay">Temeta Fozo</div>
        <a href="#" class="buy-button">Buy Now</a>
      </div>
    </div>
  </div>

  <script>
    function filterPhones() {
      const input = document.getElementById('searchInput').value.toLowerCase();
      const phones = document.querySelectorAll('.phone-card');
      phones.forEach(phone => {
        const name = phone.getAttribute('data-name').toLowerCase();
        phone.style.display = name.includes(input) ? 'block' : 'none';
      });
    }
  </script>
</body>
</html>
