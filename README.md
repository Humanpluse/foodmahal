<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Food Mahal | Pir Mahal</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&display=swap" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:Poppins;}
body{background:#0d0d0d;color:#fff;}

/* NAVBAR */
nav{
display:flex;justify-content:space-between;align-items:center;
padding:15px 30px;background:#000;position:sticky;top:0;z-index:1000;
}
nav h1{color:orange;}
nav a{color:white;margin-left:15px;text-decoration:none;}

/* HERO */
.hero{
text-align:center;padding:100px 20px;
}
.hero h2{font-size:40px;}
.btn{
background:orange;color:#fff;padding:12px 25px;border:none;border-radius:25px;
cursor:pointer;margin-top:20px;
}

/* SECTION */
section{padding:50px 20px;text-align:center;}

/* MENU */
.menu{
display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:20px;
}
.card{
background:#111;padding:15px;border-radius:10px;
}
.card img{width:100%;border-radius:10px;}
.card h3{margin:10px 0;color:orange;}

/* REVIEWS */
.review{
background:#111;margin:10px;padding:15px;border-radius:10px;
}

/* MAP */
iframe{width:100%;height:300px;border:0;border-radius:10px;}

/* FOOTER */
footer{background:#000;padding:20px;text-align:center;margin-top:30px;}

</style>
</head>

<body>

<!-- NAVBAR -->
<nav>
<h1>🍽 Food Mahal</h1>
<div>
<a href="#">Home</a>
<a href="#menu">Menu</a>
<a href="#reviews">Reviews</a>
<a href="#contact">Contact</a>
</div>
</nav>

<!-- HERO -->
<div class="hero">
<h2>Welcome to Food Mahal</h2>
<p>Best Taste in Pir Mahal</p>

<a href="https://wa.me/923242336663">
<button class="btn">Order on WhatsApp</button>
</a>
</div>

<!-- MENU -->
<section id="menu">
<h2>Our Menu</h2>

<div class="menu">

<div class="card">
<img src="https://source.unsplash.com/300x200/?biryani">
<h3>Biryani</h3>
<p>Rs 250</p>
</div>

<div class="card">
<img src="https://source.unsplash.com/300x200/?burger">
<h3>Burger</h3>
<p>Rs 300</p>
</div>

<div class="card">
<img src="https://source.unsplash.com/300x200/?pizza">
<h3>Pizza</h3>
<p>Rs 1200</p>
</div>

<div class="card">
<img src="https://source.unsplash.com/300x200/?bbq">
<h3>BBQ</h3>
<p>Rs 800</p>
</div>

</div>
</section>

<!-- REVIEWS -->
<section id="reviews">
<h2>Customer Reviews</h2>

<div class="review">⭐⭐⭐⭐⭐ Amazing taste!</div>
<div class="review">⭐⭐⭐⭐ Very good service</div>
<div class="review">⭐⭐⭐⭐⭐ Best in Pir Mahal!</div>

</section>

<!-- MAP -->
<section id="contact">
<h2>Our Location</h2>

<iframe src="https://maps.google.com/maps?q=Pir%20Mahal&t=&z=13&ie=UTF8&iwloc=&output=embed"></iframe>

</section>

<!-- FOOTER -->
<footer>
<p>© 2026 Food Mahal | All Rights Reserved</p>
</footer>

</body>
</html>
