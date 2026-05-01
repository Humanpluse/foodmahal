<!DOCTYPE html><html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Food Mahal - Pir Mahal</title>
<style>
body{margin:0;font-family:Arial;background:#0f172a;color:#fff}
header{background:#111827;padding:20px;text-align:center}
header h1{margin:0;color:#f59e0b}
nav{display:flex;justify-content:center;gap:20px;margin-top:10px}
nav a{color:#fff;text-decoration:none}
.hero{padding:40px;text-align:center;background:#1f2937}
.btn{background:#f59e0b;padding:12px 20px;border:none;color:#000;font-weight:bold;border-radius:5px;cursor:pointer}
.section{padding:30px}
.menu-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:20px}
.card{background:#1f2937;padding:20px;border-radius:10px}
.card h3{color:#f59e0b}
footer{background:#111827;padding:20px;text-align:center;margin-top:20px}
</style>
</head>
<body>
<header>
<h1>Food Mahal</h1>
<p>Pir Mahal - Fast Food | BBQ | Karahi</p>
<nav>
<a href="#menu">Menu</a>
<a href="#order">Order</a>
<a href="#contact">Contact</a>
</nav>
</header><section class="hero">
<h2>Delicious Food Delivered in 20-25 Minutes</h2>
<p>Free Delivery in Pir Mahal City | Village Extra Charges</p>
<button class="btn" onclick="orderNow()">Order Now</button>
</section><section id="menu" class="section">
<h2>Our Menu</h2>
<div class="menu-grid">
<div class="card">
<h3>Pizza</h3>
<p>Small: 500 | Medium: 1000 | Large: 1550 | XL: 2000</p>
</div>
<div class="card">
<h3>BBQ</h3>
<p>Malai Boti, Chicken Tikka, Kabab & more</p>
</div>
<div class="card">
<h3>Karahi</h3>
<p>Chicken, Beef, Mutton Karahi Available</p>
</div>
<div class="card">
<h3>Burgers & Wraps</h3>
<p>Zinger, Tower, Chicken Wraps</p>
</div>
<div class="card">
<h3>Rice & Handi</h3>
<p>Biryani, Pulao, Chicken Handi</p>
</div>
<div class="card">
<h3>Broast</h3>
<p>Full, Half & Family Deals Available</p>
</div>
</div>
</section><section id="order" class="section">
<h2>Place Your Order</h2>
<input type="text" id="name" placeholder="Your Name" style="padding:10px;width:100%;margin:10px 0">
<input type="text" id="phone" placeholder="Phone Number" style="padding:10px;width:100%;margin:10px 0">
<textarea id="order" placeholder="Your Order Details" style="padding:10px;width:100%;margin:10px 0"></textarea
