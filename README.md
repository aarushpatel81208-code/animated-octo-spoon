<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Airport Service Center</title>

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Segoe UI',sans-serif;
}

html{
scroll-behavior:smooth;
}

body{
background:#f5f7fa;
color:#333;
line-height:1.6;
}

/* Header */

header{
position:sticky;
top:0;
z-index:1000;
background:#003366;
padding:18px 8%;
display:flex;
justify-content:space-between;
align-items:center;
box-shadow:0 4px 15px rgba(0,0,0,.15);
animation:slideDown .8s ease;
}

.logo{
font-size:28px;
font-weight:700;
color:white;
}

nav a{
color:white;
text-decoration:none;
margin-left:25px;
position:relative;
font-weight:500;
}

nav a::after{
content:'';
position:absolute;
left:0;
bottom:-5px;
width:0;
height:2px;
background:#ff9800;
transition:.4s;
}

nav a:hover::after{
width:100%;
}

@keyframes slideDown{
from{
transform:translateY(-100%);
}
to{
transform:translateY(0);
}
}

/* Hero */

.hero{
height:90vh;
background:
linear-gradient(rgba(0,0,0,.45),rgba(0,0,0,.45)),
url('https://images.unsplash.com/photo-1436491865332-7a61a109cc05?w=1600');
background-size:cover;
background-position:center;
background-attachment:fixed;
display:flex;
justify-content:center;
align-items:center;
text-align:center;
padding:20px;
color:white;
}

.hero-content{
max-width:800px;
animation:fadeUp 1.2s ease;
}

.hero h1{
font-size:60px;
margin-bottom:20px;
}

.hero p{
font-size:22px;
margin-bottom:30px;
}

@keyframes fadeUp{
from{
opacity:0;
transform:translateY(50px);
}
to{
opacity:1;
transform:translateY(0);
}
}

.btn{
display:inline-block;
background:#ff9800;
color:white;
padding:15px 35px;
border-radius:5px;
text-decoration:none;
transition:.3s;
}

.btn:hover{
background:#ffb300;
transform:translateY(-4px);
}

/* Sections */

section{
padding:80px 8%;
}

.title{
text-align:center;
font-size:40px;
margin-bottom:50px;
color:#003366;
}

/* Services */

.services{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
gap:25px;
}

.service{
background:white;
padding:25px;
border-radius:12px;
box-shadow:0 5px 15px rgba(0,0,0,.08);
opacity:0;
transform:translateY(40px);
transition:.6s;
}

.service.show{
opacity:1;
transform:translateY(0);
}

.service:hover{
transform:translateY(-10px);
box-shadow:0 15px 25px rgba(0,0,0,.15);
}

.service h3{
margin-bottom:10px;
color:#003366;
}

/* Stats */

.stats{
background:#003366;
padding:60px 8%;
display:grid;
grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
gap:20px;
text-align:center;
color:white;
}

.stats div{
transition:.3s;
}

.stats div:hover{
transform:scale(1.08);
}

.stats h2{
font-size:45px;
color:#ff9800;
}

/* Contact */

.contact{
max-width:700px;
margin:auto;
opacity:0;
transform:translateY(40px);
transition:1s;
}

.contact.show{
opacity:1;
transform:translateY(0);
}

.contact input,
.contact textarea{
width:100%;
padding:15px;
margin-bottom:15px;
border:1px solid #ddd;
border-radius:6px;
font-size:16px;
}

.contact button{
width:100%;
padding:15px;
background:#003366;
color:white;
border:none;
border-radius:6px;
font-size:18px;
cursor:pointer;
transition:.3s;
}

.contact button:hover{
background:#004c99;
}

/* Footer */

footer{
background:#001f3f;
color:white;
text-align:center;
padding:20px;
}

/* Mobile */

@media(max-width:768px){

.hero h1{
font-size:40px;
}

.hero p{
font-size:18px;
}

nav{
display:none;
}

}

</style>
</head>
<body>

<header>
<div class="logo">Airport Service Center</div>

<nav>
<a href="#home">Home</a>
<a href="#services">Services</a>
<a href="#contact">Contact</a>
</nav>
</header>

<section class="hero" id="home">

<div class="hero-content">
<h1>Welcome To Airport Service Center</h1>

<p>
24/7 Airport Assistance, Flight Information,
Baggage Support and Premium Passenger Services
</p>

<a href="#services" class="btn">Book Service</a>
</div>

</section>

<section id="services">

<h2 class="title">Our Services</h2>

<div class="services">

<div class="service">
<h3>Flight Information</h3>
<p>Real-time flight schedules and live airport updates.</p>
</div>

<div class="service">
<h3>Baggage Support</h3>
<p>Lost baggage tracking and passenger assistance.</p>
</div>

<div class="service">
<h3>VIP Lounge Access</h3>
<p>Premium lounge booking and hospitality services.</p>
</div>

<div class="service">
<h3>Airport Transfer</h3>
<p>Safe and reliable transportation solutions.</p>
</div>

<div class="service">
<h3>Meet & Greet</h3>
<p>Professional arrival and departure assistance.</p>
</div>

<div class="service">
<h3>24/7 Support</h3>
<p>Dedicated customer support around the clock.</p>
</div>

</div>

</section>

<div class="stats">

<div>
<h2>10K+</h2>
<p>Passengers Served</p>
</div>

<div>
<h2>500+</h2>
<p>Daily Requests</p>
</div>

<div>
<h2>50+</h2>
<p>Airport Partners</p>
</div>

<div>
<h2>24/7</h2>
<p>Support Available</p>
</div>

</div>

<section id="contact">

<h2 class="title">Contact Us</h2>

<form class="contact">

<input type="text" placeholder="Full Name">

<input type="email" placeholder="Email Address">

<input type="tel" placeholder="Phone Number">

<textarea rows="5" placeholder="Your Message"></textarea>

<button type="submit">Submit Request</button>

</form>

</section>

<footer>
© 2026 Airport Service Center | All Rights Reserved
</footer>

<script>

const observer=new IntersectionObserver(entries=>{
entries.forEach(entry=>{
if(entry.isIntersecting){
entry.target.classList.add("show");
}
});
});

document.querySelectorAll('.service,.contact')
.forEach(el=>observer.observe(el));

</script>

</body>
</html>
