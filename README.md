<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Beyond The Limit Store</title>

<style>
body{
margin:0;
font-family:Arial;
background:linear-gradient(135deg,#0f172a,#1e3a8a,#6366f1);
background-attachment:fixed;
}

.navbar{
background:white;
border-bottom:1px solid #ddd;
padding:12px 20px;
display:flex;
justify-content:space-between;
align-items:center;
position:sticky;
top:0;
z-index:10;
}

.logo{font-size:20px;font-weight:bold;color:#e53238}

.nav-links a{
margin-left:12px;
text-decoration:none;
color:#333;
font-size:14px;
}

.section{display:none;padding:20px}
.active{display:block}

.products{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
gap:20px;
}

.card{
background:#3b82f6;
color:white;
padding:12px;
border-radius:12px;
text-align:center;
box-shadow:0 4px 10px rgba(0,0,0,0.1);
}

.card img{width:100%;border-radius:6px}

button{
background:#6366f1;
color:white;
border:none;
padding:8px;
width:100%;
margin-top:8px;
border-radius:5px;
cursor:pointer;
}

select{
width:100%;
padding:6px;
margin-top:5px;
}

.cart-box{
background:white;
padding:20px;
border-radius:10px;
max-width:500px;
margin:auto;
}

.badge{
background:red;
color:white;
border-radius:50%;
padding:2px 6px;
font-size:12px;
margin-left:5px;
}

#notif{
position:fixed;
bottom:20px;
left:50%;
transform:translateX(-50%);
background:#111;
color:white;
padding:10px 20px;
border-radius:8px;
font-size:14px;
display:none;
z-index:9999;
}
</style>
</head>

<body>

<div id="notif"></div>

<div class="navbar">
<div class="logo">Beyond The Limit</div>

<div class="nav-links">
<a href="#" onclick="showSection('home')">Home</a>
<a href="#" onclick="showSection('shirts')">Shirts</a>
<a href="#" onclick="showSection('shorts')">Shorts</a>
<a href="#" onclick="showSection('jackets')">Jackets</a>
<a href="#" onclick="showSection('cart')">Cart <span class="badge" id="cartCount">0</span></a>
</div>
</div>

<div id="home" class="section active" style="text-align:center;">
<img src="https://www.shutterstock.com/image-vector/beyond-limits-slogan-graphic-t-600nw-2004288302.jpg" style="width:220px">
<h1>Beyond The Limit</h1>
<p style="color:white;">Push your limits. Wear your story.</p>
<button onclick="showSection('shirts')">Shop Now</button>

<div style="background:white;margin-top:20px;padding:20px;border-radius:10px;max-width:800px;margin:auto">
<h2>About Us</h2>
<p>
Beyond The Limit represents pushing limits and chasing dreams.
<br><br>
Created by a first-year college student from Imus, Cavite.
</p>
<hr>
<p style="font-style:italic;">
“I can do all things through Christ who strengthens me.”<br>
— Philippians 4:13
</p>
</div>
</div>

<div id="shirts" class="section">
<h2 style="color:white;">Shirts</h2>
<div class="products">

<div class="card">
<img src="https://highabovesociety.com/cdn/shop/files/image.jpg?v=1684951865">
<div>Classic Shirt</div>
<div>₱450</div>
<select id="s1"><option>S</option><option>M</option><option>L</option><option>XL</option></select>
<button onclick="addToCart('Classic Shirt',450,'s1')">Add to Cart</button>
</div>

<div class="card">
<img src="https://thecrescendobrand.com/cdn/shop/files/RISEBEYONDLIMITSGLOBETEEBACKBLACKCPPR.png?v=1712864958">
<div>Street Tee</div>
<div>₱500</div>
<select id="s2"><option>S</option><option>M</option><option>L</option><option>XL</option></select>
<button onclick="addToCart('Street Tee',500,'s2')">Add to Cart</button>
</div>

<div class="card">
<img src="https://img.gem.app/1809161916/1t/1758866266/tailored-originals-beyond-the-limit-t-shirt.jpg">
<div>Minimal Tee</div>
<div>₱480</div>
<select id="s3"><option>S</option><option>M</option><option>L</option><option>XL</option></select>
<button onclick="addToCart('Minimal Tee',480,'s3')">Add to Cart</button>
</div>

</div>
</div>

<div id="shorts" class="section">
<h2 style="color:white;">Shorts</h2>
<div class="products">

<div class="card">
<img src="https://neweracap.ph/cdn/shop/files/14148834_01064834_grab_5.jpg?v=1716628262&width=2000">
<div>Sport Shorts</div>
<div>₱350</div>
<select id="s4"><option>S</option><option>M</option><option>L</option><option>XL</option></select>
<button onclick="addToCart('Sport Shorts',350,'s4')">Add to Cart</button>
</div>

<div class="card">
<img src="https://encrypted-tbn1.gstatic.com/shopping?q=tbn:ANd9GcR3TT2mUoedZOGHgJrrfeHxLgDjpDurG_XHRVWjHESVfXzK43BlSQkio-0zSOUPOMVgOaYc2rx-ZE46q7pZ5eBxc2MDOfJIx__nKXKkGIxu97RFQZhWwIt2VdM">
<div>Casual Shorts</div>
<div>₱380</div>
<select id="s5"><option>S</option><option>M</option><option>L</option><option>XL</option></select>
<button onclick="addToCart('Casual Shorts',380,'s5')">Add to Cart</button>
</div>

<div class="card">
<img src="https://encrypted-tbn3.gstatic.com/shopping?q=tbn:ANd9GcRO1E_Mk3_jDxvoQ9pcmmq1ZfiO-1uuzGJKC1DTVcVmYQObE0e87yU-gwTSB3RuMjSs5fJYK_stfWxJZJwn4IeivD523df1jLNkXYY1e5oloSvnoYY_gqQIBQ">
<div>Training Shorts</div>
<div>₱400</div>
<select id="s6"><option>S</option><option>M</option><option>L</option><option>XL</option></select>
<button onclick="addToCart('Training Shorts',400,'s6')">Add to Cart</button>
</div>

</div>
</div>

<div id="jackets" class="section">
<h2 style="color:white;">Jackets</h2>
<div class="products">

<div class="card">
<img src="https://i.ebayimg.com/images/g/gKcAAOSwKwNmCqsW/s-l1600.webp">
<div>Jacket 1</div>
<div>₱999</div>
<select id="s7"><option>S</option><option>M</option><option>L</option><option>XL</option></select>
<button onclick="addToCart('Jacket 1',999,'s7')">Add to Cart</button>
</div>

<div class="card">
<img src="https://i.ebayimg.com/images/g/AAUAAOSwLEljYFmv/s-l1600.webp">
<div>Jacket 2</div>
<div>₱1099</div>
<select id="s8"><option>S</option><option>M</option><option>L</option><option>XL</option></select>
<button onclick="addToCart('Jacket 2',1099,'s8')">Add to Cart</button>
</div>

<div class="card">
<img src="https://www.apetogentleman.com/wp-content/uploads/2021/09/CoolJacketsForMen9-420x420.jpg">
<div>Jacket 3</div>
<div>₱1199</div>
<select id="s9"><option>S</option><option>M</option><option>L</option><option>XL</option></select>
<button onclick="addToCart('Jacket 3',1199,'s9')">Add to Cart</button>
</div>

</div>
</div>

<div id="cart" class="section">
<div class="cart-box" id="cartBox">
<h2>Your Cart</h2>
<p>No items yet</p>
</div>
</div>

<script>
let cart=[];

function showSection(id){
document.querySelectorAll('.section').forEach(s=>s.classList.remove('active'));
document.getElementById(id).classList.add('active');
}

function addToCart(name,price,sizeId){
let size=document.getElementById(sizeId).value;
cart.push({name,price,size});
updateCart();
showNotif(name);
}

function updateCart(){
document.getElementById("cartCount").innerText=cart.length;

let box=document.getElementById("cartBox");

if(cart.length===0){
box.innerHTML="<h2>Your Cart</h2><p>No items yet</p>";
return;
}

box.innerHTML="<h2>Your Cart</h2>";

cart.forEach(c=>{
box.innerHTML+=`<div>${c.name} (${c.size}) ₱${c.price}</div>`;
});

box.innerHTML+=`
<h3>Total: ₱${cart.reduce((a,b)=>a+b.price,0)}</h3>
<input id="c_name" placeholder="Full Name" style="width:100%;padding:8px;margin:5px 0;">
<input id="c_number" placeholder="Contact Number" style="width:100%;padding:8px;margin:5px 0;">
<input id="c_address" placeholder="Address" style="width:100%;padding:8px;margin:5px 0;">
<button onclick="placeOrder()">Place Order</button>
`;
}

function placeOrder(){
let n=document.getElementById("c_name").value;
let num=document.getElementById("c_number").value;
let add=document.getElementById("c_address").value;

if(!n||!num||!add){
alert("Complete all details");
return;
}

alert("Order placed successfully!");
cart=[];
updateCart();
showSection("home");
}

function showNotif(name){
let n=document.getElementById("notif");
n.innerText=name+" added to cart ✓";
n.style.display="block";
setTimeout(()=>n.style.display="none",1500);
}
</script>

</body>
</html>
