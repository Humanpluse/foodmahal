
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Food Mahal - Pir Mahal</title>

<style>
body{
  margin:0;
  font-family:Arial;
  background:#fff8f0;
}
header{
  background:#c0192a;
  color:white;
  padding:15px;
  text-align:center;
}
.hero{
  padding:40px;
  text-align:center;
  background:#1a0a00;
  color:white;
}
.hero h1{font-size:40px}
.btn{
  background:#25D366;
  padding:10px 20px;
  color:white;
  text-decoration:none;
  border-radius:20px;
  display:inline-block;
  margin-top:10px;
}
.section{
  padding:30px;
}
.grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
  gap:15px;
}
.card{
  background:white;
  padding:15px;
  border-radius:10px;
  box-shadow:0 2px 10px rgba(0,0,0,0.1);
}
.card img{
  width:100%;
  border-radius:10px;
}
.price{
  color:#c0192a;
  font-weight:bold;
}
footer{
  background:black;
  color:white;
  text-align:center;
  padding:10px;
}
</style>
</head>

<body>

<header>
  <h2>🍕 Food Mahal</h2>
</header>

<div class="hero">
  <h1>Best Food in Pir Mahal</h1>
  <p>Pizza | Broast | BBQ | Fast Food</p>
  <a class="btn" href="https://wa.me/923242336663">Order on WhatsApp</a>
</div>

<!-- MENU -->
<div class="section">
  <h2>Menu</h2>

  <div class="grid">

    <div class="card">
      <img src="https://images.unsplash.com/photo-1601924638867-3ec6c2b53c5f">
      <h3>Pizza</h3>
      <p class="price">Rs 750+</p>
      <a class="btn" href="https://wa.me/923242336663?text=Pizza Order">Order</a>
    </div>

    <div class="card">
      <img src="https://images.unsplash.com/photo-1600891964599-f61ba0e24092">
      <h3>Chicken Broast</h3>
      <p class="price">Rs 599</p>
      <a class="btn" href="https://wa.me/923242336663?text=Broast Order">Order</a>
    </div>

    <div class="card">
      <img src="https://images.unsplash.com/photo-1550547660-d9450f859349">
      <h3>Zinger Burger</h3>
      <p class="price">Rs 300</p>
      <a class="btn" href="https://wa.me/923242336663?text=Burger Order">Order</a>
    </div>

  </div>
</div>

<!-- DEALS -->
<div class="section">
  <h2>Deals</h2>

  <div class="grid">
    <div class="card">
      <h3>Deal 1</h3>
      <p>Zinger + Fries + Drink</p>
      <p class="price">Rs 500</p>
    </div>

    <div class="card">
      <h3>Deal 5</h3>
      <p>Large Pizza + Wings + Drink</p>
      <p class="price">Rs 2100</p>
    </div>
  </div>
</div>

<!-- GALLERY -->
<div class="section">
  <h2>Gallery</h2>
  <div class="grid">
    <img src="https://images.unsplash.com/photo-1548365328-8b849e54a8c0">
    <img src="https://images.unsplash.com/photo-1604908176997-125f25cc6f3d">
  </div>
</div>

<!-- PAYMENT -->
<div class="section">
  <h2>Online Payment</h2>

  <p>Pay via JazzCash / Easypaisa</p>

  <a class="btn" href="https://payment-link.com">Pay Now</a>
</div>

<!-- MAP -->
<div class="section">
  <h2>Location</h2>

  <iframe width="100%" height="250"
  src="https://maps.google.com/maps?q=Pir%20Mahal&t=&z=13&ie=UTF8&iwloc=&output=embed">
  </iframe>
</div>

<footer>
  📞 0324-2336663 | Food Mahal Pir Mahal
</footer>

</body>
</html>
