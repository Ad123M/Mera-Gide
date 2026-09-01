<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">

<title>Mera-Gide | Green Ayurveda</title>
<meta name="description" content="Mera-Gide Green Ayurveda and Natural Products Marketplace">

<style>
*{box-sizing:border-box}
body{
margin:0;
font-family:Arial,sans-serif;
background:#f5faf6;
color:#173b25
}
header{
position:sticky;
top:0;
z-index:99;
background:#fff;
box-shadow:0 2px 12px #0002
}
.nav{
max-width:1200px;
margin:auto;
padding:12px 18px;
display:flex;
align-items:center;
justify-content:space-between
}
.logo{
display:flex;
align-items:center;
gap:9px;
font-size:25px;
font-weight:bold;
color:#15733b
}
.logo span{
width:43px;
height:43px;
border-radius:50%;
background:#15733b;
display:flex;
align-items:center;
justify-content:center;
color:white
}
nav{
display:flex;
gap:18px;
align-items:center
}
nav a{
cursor:pointer;
font-weight:bold
}
nav a:hover{color:#15733b}
.btn{
border:0;
border-radius:7px;
padding:11px 18px;
cursor:pointer;
font-weight:bold
}
.green{
background:#15733b;
color:white
}
.outline{
border:2px solid #15733b;
background:white;
color:#15733b
}

.hero{
background:linear-gradient(120deg,#dff5e5,#fff);
padding:80px 20px
}
.hero-inner{
max-width:1200px;
margin:auto
}
.hero h1{
font-size:52px;
margin:0 0 18px;
color:#0d4c27
}
.hero p{
font-size:19px;
max-width:650px;
line-height:1.7
}
.hero button{margin:7px}

section{
max-width:1200px;
margin:auto;
padding:55px 20px
}
.title{
text-align:center;
font-size:31px;
margin-bottom:30px
}

.categories{
display:grid;
grid-template-columns:repeat(6,1fr);
gap:15px
}
.cat{
background:white;
padding:25px 10px;
text-align:center;
border-radius:12px;
box-shadow:0 3px 15px #0001;
cursor:pointer
}
.cat div{font-size:35px;margin-bottom:8px}

.products{
display:grid;
grid-template-columns:repeat(4,1fr);
gap:20px
}
.card{
background:white;
border-radius:12px;
overflow:hidden;
box-shadow:0 3px 15px #0001
}
.card img{
width:100%;
height:220px;
object-fit:cover;
background:#e5f2e7
}
.card-body{padding:17px}
.card h3{margin:0 0 8px}
.card p{
font-size:14px;
color:#65736a;
line-height:1.5
}
.price{
font-size:21px;
font-weight:bold;
color:#15733b;
margin:12px 0
}
.actions{
display:flex;
gap:7px
}
.actions button{
flex:1;
padding:10px;
border-radius:6px;
cursor:pointer;
font-weight:bold
}

.why{
background:#e8f5eb;
max-width:none
}
.why-grid{
max-width:1200px;
margin:auto;
padding:0 20px;
display:grid;
grid-template-columns:repeat(4,1fr);
gap:18px
}
.box{
background:white;
padding:25px;
border-radius:12px;
text-align:center
}
.box-icon{font-size:35px}

.seller{
background:linear-gradient(135deg,#0b4424,#238047);
color:white;
border-radius:18px;
padding:45px;
text-align:center
}
.seller h2{font-size:32px}

footer{
background:#0b2c19;
color:white;
margin-top:40px
}
.footer{
max-width:1200px;
margin:auto;
padding:40px 20px;
display:grid;
grid-template-columns:2fr 1fr 1fr 1fr;
gap:30px
}
.footer a{
display:block;
color:#c9dccf;
margin:9px 0;
cursor:pointer
}
.copy{
border-top:1px solid #345340;
text-align:center;
padding:17px;
color:#bdd0c3
}

.modal{
display:none;
position:fixed;
inset:0;
background:#0009;
z-index:999;
overflow:auto;
padding:20px
}
.modal-box{
background:white;
max-width:720px;
margin:40px auto;
padding:27px;
border-radius:14px;
position:relative
}
.close{
position:absolute;
right:15px;
top:10px;
border:0;
background:none;
font-size:30px;
cursor:pointer
}
.form{
margin:13px 0
}
.form label{
display:block;
font-weight:bold;
margin-bottom:5px
}
.form input,.form textarea,.form select{
width:100%;
padding:12px;
border:1px solid #ccd8cf;
border-radius:7px
}
.form textarea{min-height:100px}

.dashboard-stats{
display:grid;
grid-template-columns:repeat(4,1fr);
gap:12px;
margin:20px 0
}
.stat{
background:#eaf5ed;
padding:20px;
border-radius:10px;
border-left:4px solid #15733b
}
.stat b{
display:block;
font-size:25px;
margin-top:6px
}

.table{
width:100%;
border-collapse:collapse;
margin-top:15px
}
.table th,.table td{
padding:10px;
border-bottom:1px solid #ddd;
text-align:left
}

.search{
display:block;
width:100%;
max-width:600px;
margin:0 auto 25px;
padding:14px;
border:1px solid #ccd8cf;
border-radius:8px
}

@media(max-width:900px){
.categories{grid-template-columns:repeat(3,1fr)}
.products{grid-template-columns:repeat(2,1fr)}
.why-grid{grid-template-columns:repeat(2,1fr)}
.footer{grid-template-columns:repeat(2,1fr)}
.dashboard-stats{grid-template-columns:repeat(2,1fr)}
}

@media(max-width:600px){
nav{display:none}
.hero h1{font-size:37px}
.categories{grid-template-columns:repeat(2,1fr)}
.products{grid-template-columns:1fr}
.why-grid{grid-template-columns:1fr}
.footer{grid-template-columns:1fr}
.dashboard-stats{grid-template-columns:1fr}
}
</style>
</head>

<body>

<header>
<div class="nav">

<div class="logo">
<span>🌿</span>
Mera-Gide
</div>

<nav>
<a onclick="home()">Home</a>
<a onclick="shop()">Shop</a>
<a onclick="about()">About Us</a>
<a onclick="contact()">Contact Us</a>
<a onclick="seller()">Seller</a>
<a onclick="admin()">Admin</a>
<button class="btn green" onclick="cart()">🛒 Cart (<b id="count">0</b>)</button>
</nav>

</div>
</header>

<!-- HOME -->

<div class="hero" id="home">

<div class="hero-inner">

<h1>Natural Wellness.<br>Trusted Ayurveda.</h1>

<p>
Discover Green Ayurveda, herbal and natural wellness products
from trusted sellers on Mera-Gide.
</p>

<button class="btn green" onclick="shop()">Shop Now</button>
<button class="btn outline" onclick="seller()">Become a Seller</button>

</div>
</div>

<!-- CATEGORY -->

<section>

<h2 class="title">Shop by Category</h2>

<div class="categories">

<div class="cat" onclick="filter('Ayurveda')">
<div>🌿</div>Ayurveda
</div>

<div class="cat" onclick="filter('Herbal')">
<div>🍃</div>Herbal
</div>

<div class="cat" onclick="filter('Beauty')">
<div>🌸</div>Natural Beauty
</div>

<div class="cat" onclick="filter('Personal Care')">
<div>🧴</div>Personal Care
</div>

<div class="cat" onclick="filter('Wellness')">
<div>🌱</div>Wellness
</div>

<div class="cat" onclick="filter('Organic')">
<div>🌾</div>Organic
</div>

</div>
</section>

<!-- SHOP -->

<section id="shop">

<h2 class="title">Green Ayurveda Products</h2>

<input
class="search"
id="search"
placeholder="🔎 Search products..."
onkeyup="searchProducts()">

<div class="products" id="products"></div>

</section>

<!-- WHY -->

<div class="why">

<section>

<h2 class="title">Why Choose Mera-Gide?</h2>

<div class="why-grid">

<div class="box">
<div class="box-icon">🌿</div>
<h3>Natural Products</h3>
<p>Green Ayurveda and natural wellness products.</p>
</div>

<div class="box">
<div class="box-icon">🤝</div>
<h3>Trusted Sellers</h3>
<p>Seller products can be reviewed before publishing.</p>
</div>

<div class="box">
<div class="box-icon">🔒</div>
<h3>Secure Shopping</h3>
<p>Simple and secure checkout experience.</p>
</div>

<div class="box">
<div class="box-icon">📦</div>
<h3>Easy Ordering</h3>
<p>Simple product and order management.</p>
</div>

</div>

</section>
</div>

<!-- SELLER CTA -->

<section>

<div class="seller">

<h2>Sell Your Green Ayurveda Products</h2>

<p>
Join Mera-Gide and showcase your herbal and natural products.
</p>

<button class="btn" style="background:white;color:#15733b"
onclick="seller()">
Become a Seller
</button>

</div>

</section>

<!-- FOOTER -->

<footer>

<div class="footer">

<div>
<h2>🌿 Mera-Gide</h2>
<p>Green Ayurveda & Natural Products Marketplace.</p>
</div>

<div>
<h3>Quick Links</h3>
<a onclick="home()">Home</a>
<a onclick="shop()">Shop</a>
<a onclick="about()">About Us</a>
<a onclick="contact()">Contact Us</a>
</div>

<div>
<h3>Seller</h3>
<a onclick="seller()">Seller Registration</a>
<a onclick="seller()">Seller Login</a>
<a onclick="admin()">Admin Login</a>
</div>

<div>
<h3>Legal</h3>
<a onclick="terms()">Terms & Conditions</a>
<a onclick="privacy()">Privacy Policy</a>
<a onclick="refund()">Return & Refund</a>
<a onclick="shipping()">Shipping Policy</a>
</div>

</div>

<div class="copy">
© 2026 Mera-Gide. All Rights Reserved.
</div>

</footer>

<!-- SELLER MODAL -->

<div class="modal" id="sellerModal">

<div class="modal-box">

<button class="close" onclick="closeModal('sellerModal')">×</button>

<h2>🌿 Seller Registration</h2>

<p>
Seller registration के बाद product Admin approval के लिए जाएगा।
</p>

<div class="form">
<label>Seller Name</label>
<input id="sname">
</div>

<div class="form">
<label>Business / Brand Name</label>
<input id="brand">
</div>

<div class="form">
<label>Email</label>
<input type="email" id="semail">
</div>

<div class="form">
<label>Mobile</label>
<input id="smobile">
</div>

<div class="form">
<label>Password</label>
<input type="password" id="spassword">
</div>

<button class="btn green" onclick="registerSeller()">
Register Seller
</button>

<hr>

<h3>Seller Login</h3>

<div class="form">
<input id="lemail" type="email" placeholder="Seller Email">
</div>

<div class="form">
<input id="lpassword" type="password" placeholder="Password">
</div>

<button class="btn green" onclick="sellerLogin()">
Seller Login
</button>

</div>
</div>

<!-- ADMIN LOGIN -->

<div class="modal" id="adminModal">

<div class="modal-box">

<button class="close" onclick="closeModal('adminModal')">×</button>

<h2>🔐 Admin Login</h2>

<div style="background:#fff8d9;padding:15px;border-left:4px solid #d89a1d">
Demo Login:<br>
Email: <b>admin@mera-gide.com</b><br>
Password: <b>admin123</b>
</div>

<div class="form">
<label>Email</label>
<input type="email" id="aemail">
</div>

<div class="form">
<label>Password</label>
<input type="password" id="apassword">
</div>

<button class="btn green" onclick="adminLogin()">
Admin Login
</button>

</div>
</div>

<!-- ADMIN DASHBOARD -->

<div class="modal" id="adminPanel">

<div class="modal-box" style="max-width:1000px">

<button class="close" onclick="closeModal('adminPanel')">×</button>

<h2>⚙️ Mera-Gide Admin Dashboard</h2>

<div class="dashboard-stats">

<div class="stat">
Sellers
<b id="sellerCount">0</b>
</div>

<div class="stat">
Products
<b id="productCount">0</b>
</div>

<div class="stat">
Pending
<b id="pendingCount">0</b>
</div>

<div class="stat">
Orders
<b id="orderCount">0</b>
</div>

</div>

<button class="btn green" onclick="adminProducts()">
Product Management
</button>

<button class="btn outline" onclick="addProduct()">
+ Add Product
</button>

<button class="btn outline" onclick="orders()">
Orders
</button>

<div id="adminContent" style="margin-top:25px"></div>

</div>
</div>

<!-- ADD PRODUCT -->

<div class="modal" id="productModal">

<div class="modal-box">

<button class="close" onclick="closeModal('productModal')">×</button>

<h2>📦 Upload Product</h2>

<div class="form">
<label>Product Name</label>
<input id="pname">
</div>

<div class="form">
<label>Category</label>
<select id="pcat">
<option>Ayurveda</option>
<option>Herbal</option>
<option>Beauty</option>
<option>Personal Care</option>
<option>Wellness</option>
<option>Organic</option>
</select>
</div>

<div class="form">
<label>Product Image</label>
<input type="file" id="pimage" accept="image/*">
</div>

<div class="form">
<label>Description</label>
<textarea id="pdesc"></textarea>
</div>

<div class="form">
<label>Ingredients</label>
<textarea id="ping"></textarea>
</div>

<div class="form">
<label>Benefits</label>
<textarea id="pbenefits"></textarea>
</div>

<div class="form">
<label>Price ₹</label>
<input type="number" id="pprice">
</div>

<div class="form">
<label>Stock</label>
<input type="number" id="pstock">
</div>

<button class="btn green" onclick="saveProduct()">
Submit Product for Approval
</button>

</div>
</div>

<!-- GENERAL MODAL -->

<div class="modal" id="infoModal">

<div class="modal-box">

<button class="close" onclick="closeModal('infoModal')">×</button>

<div id="info"></div>

</div>
</div>


<script>

/* PRODUCT DATABASE */

let productsData =
JSON.parse(localStorage.getItem("meraGideProducts")) || [

{
id:1,
name:"Green Herbal Wellness",
category:"Herbal",
price:499,
stock:20,
image:"https://images.unsplash.com/photo-1611073764950-0b8b1b4a3c7d?auto=format&fit=crop&w=800&q=80",
description:"Natural herbal wellness product.",
status:"approved"
},

{
id:2,
name:"Ayurvedic Herbal Care",
category:"Ayurveda",
price:699,
stock:15,
image:"https://images.unsplash.com/photo-1608571423902-eed4a5ad8108?auto=format&fit=crop&w=800&q=80",
description:"Ayurvedic inspired natural care product.",
status:"approved"
},

{
id:3,
name:"Natural Beauty Care",
category:"Beauty",
price:399,
stock:30,
image:"https://images.unsplash.com/photo-1556228720-195a672e8a03?auto=format&fit=crop&w=800&q=80",
description:"Natural beauty care product.",
status:"approved"
}

];

let cartData =
JSON.parse(localStorage.getItem("meraGideCart")) || [];


/* DISPLAY */

function displayProducts(list=productsData){

let box=document.getElementById("products");

let approved=list.filter(p=>p.status==="approved");

if(!approved.length){
box.innerHTML="<p>No products found.</p>";
return;
}

box.innerHTML=approved.map(p=>`

<div class="card">

<img src="${p.image}" alt="${p.name}">

<div class="card-body">

<h3>${safe(p.name)}</h3>

<p>${safe(p.description)}</p>

<div class="price">₹${p.price}</div>

<div class="actions">

<button class="outline"
onclick="addCart(${p.id})">
Add Cart
</button>

<button class="green"
onclick="buy(${p.id})">
Buy Now
</button>

</div>

</div>

</div>

`).join("");

}


/* SEARCH */

function searchProducts(){

let q=document.getElementById("search").value.toLowerCase();

displayProducts(
productsData.filter(p=>
p.name.toLowerCase().includes(q) ||
p.category.toLowerCase().includes(q)
)
);

}


/* CATEGORY */

function filter(cat){

displayProducts(
productsData.filter(p=>
p.category===cat &&
p.status==="approved"
)
);

shop();

}


/* CART */

function addCart(id){

let p=productsData.find(x=>x.id===id);

if(!p)return;

cartData.push(p);

localStorage.setItem(
"meraGideCart",
JSON.stringify(cartData)
);

updateCart();

alert("Product added to cart.");

}


function buy(id){

cartData=[];

addCart(id);

checkout();

}


function updateCart(){

document.getElementById("count").innerText=
cartData.length;

}


function cart(){

let html="";

if(!cartData.length){

html="<p>Your cart is empty.</p>";

}else{

html=cartData.map((p,i)=>`

<div style="padding:12px;border-bottom:1px solid #ddd">

<b>${safe(p.name)}</b>

<span style="float:right">₹${p.price}</span>

<button
style="margin-top:7px"
onclick="removeCart(${i})">
Remove
</button>

</div>

`).join("");

}

showInfo(`
<h2>🛒 Shopping Cart</h2>

${html}

<hr>

<h3>
Total: ₹${cartData.reduce((a,p)=>a+Number(p.price),0)}
</h3>

<button class="btn green"
onclick="checkout()">
Proceed to Payment
</button>
`);

}


function removeCart(i){

cartData.splice(i,1);

localStorage.setItem(
"meraGideCart",
JSON.stringify(cartData)
);

updateCart();

cart();

}


/* CHECKOUT */

function checkout(){

if(!cartData.length){

alert("Cart is empty.");
return;

}

let total=cartData.reduce(
(a,p)=>a+Number(p.price),0
);

showInfo(`

<h2>💳 Checkout</h2>

<div class="form">
<label>Customer Name</label>
<input id="customer">
</div>

<div class="form">
<label>Mobile Number</label>
<input id="mobile">
</div>

<div class="form">
<label>Delivery Address</label>
<textarea id="address"></textarea>
</div>

<div style="
background:#eaf5ed;
padding:20px;
border-radius:10px;
text-align:center">

<h3>Payment</h3>

<p>UPI / QR Payment</p>

<div style="font-size:65px">▦</div>

<p>
Admin can replace this demo QR
with the official payment QR.
</p>

<h3>Total: ₹${total}</h3>

</div>

<button class="btn green"
style="width:100%;margin-top:20px"
onclick="placeOrder()">
Proceed to Payment
</button>

`);

}


function placeOrder(){

let name=document.getElementById("customer").value;
let mobile=document.getElementById("mobile").value;
let address=document.getElementById("address").value;

if(!name||!mobile||!address){

alert("Please complete all details.");
return;

}

let ordersData =
JSON.parse(localStorage.getItem("meraGideOrders")) || [];

let total=cartData.reduce(
(a,p)=>a+Number(p.price),0
);

let id="MG"+Date.now();

ordersData.push({

id:id,
customer:name,
mobile:mobile,
address:address,
products:cartData.map(p=>p.name),
total:total,
status:"Payment Pending",
date:new Date().toLocaleString()

});

localStorage.setItem(
"meraGideOrders",
JSON.stringify(ordersData)
);

cartData=[];

localStorage.setItem(
"meraGideCart",
JSON.stringify(cartData)
);

updateCart();

showInfo(`

<div style="text-align:center">

<div style="font-size:60px">✅</div>

<h2>Order Created Successfully</h2>

<p>Order ID: <b>${id}</b></p>

<p>Payment Status: <b>Pending</b></p>

<p>
Please complete payment using the configured
UPI/payment method.
</p>

</div>

`);

}


/* SELLER */

function seller(){

document.getElementById("sellerModal").style.display="block";

}


function registerSeller(){

let sellers=
JSON.parse(localStorage.getItem("meraGideSellers"))||[];

sellers.push({

name:document.getElementById("sname").value,
brand:document.getElementById("brand").value,
email:document.getElementById("semail").value,
mobile:document.getElementById("smobile").value,
password:document.getElementById("spassword").value,
status:"Pending"

});

localStorage.setItem(
"meraGideSellers",
JSON.stringify(sellers)
);

alert(
"Seller registration submitted. Admin approval required."
);

closeModal("sellerModal");

}


function sellerLogin(){

let email=document.getElementById("lemail").value;
let password=document.getElementById("lpassword").value;

let sellers=
JSON.parse(localStorage.getItem("meraGideSellers"))||[];

let s=sellers.find(x=>
x.email===email &&
x.password===password
);

if(!s){

alert("Invalid seller login.");
return;

}

if(s.status!=="Approved"){

alert("Seller account is waiting for Admin approval.");
return;

}

alert("Seller login successful.");

}


/* ADMIN */

function admin(){

document.getElementById("adminModal").style.display="block";

}


function adminLogin(){

let email=document.getElementById("aemail").value;
let password=document.getElementById("apassword").value;

if(
email==="admin@mera-gide.com" &&
password==="admin123"
){

closeModal("adminModal");

document.getElementById("adminPanel").style.display="block";

refreshAdmin();

}else{

alert("Invalid Admin Login.");

}

}


function refreshAdmin(){

let sellers=
JSON.parse(localStorage.getItem("meraGideSellers"))||[];

let ordersData=
JSON.parse(localStorage.getItem("meraGideOrders"))||[];

document.getElementById("sellerCount").innerText=sellers.length;

document.getElementById("productCount").innerText=
productsData.length;

document.getElementById("pendingCount").innerText=
productsData.filter(p=>p.status==="pending").length;

document.getElementById("orderCount").innerText=
ordersData.length;

adminProducts();

}


/* ADMIN PRODUCT */

function adminProducts(){

let html=`

<h3>Product Management</h3>

<table class="table">

<tr>
<th>Product</th>
<th>Price</th>
<th>Status</th>
<th>Action</th>
</tr>

`;

productsData.forEach(p=>{

html+=`

<tr>

<td>${safe(p.name)}</td>

<td>₹${p.price}</td>

<td>${p.status}</td>

<td>

${
p.status==="pending"

?

`
<button class="btn green"
onclick="approve(${p.id})">
Approve
</button>

<button class="btn"
onclick="reject(${p.id})">
Reject
</button>
`

:

`
<button class="btn"
onclick="deleteProduct(${p.id})">
Delete
</button>
`
}

</td>

</tr>

`;

});

html+="</table>";

document.getElementById("adminContent").innerHTML=html;

}


function approve(id){

let p=productsData.find(x=>x.id===id);

if(p){

p.status="approved";

saveProducts();

alert("Product Approved.");

refreshAdmin();

displayProducts();

}

}


function reject(id){

let p=productsData.find(x=>x.id===id);

if(p){

p.status="rejected";

saveProducts();

alert("Product Rejected.");

refreshAdmin();

}

}


function deleteProduct(id){

if(!confirm("Delete product?"))return;

productsData=
productsData.filter(p=>p.id!==id);

saveProducts();

refreshAdmin();

displayProducts();

}


/* ADD PRODUCT */

function addProduct(){

closeModal("adminPanel");

document.getElementById("productModal").style.display="block";

}


function saveProduct(){

let file=document.getElementById("pimage").files[0];

if(!file){

alert("Please upload product image.");
return;

}

let reader=new FileReader();

reader.onload=function(){

let p={

id:Date.now(),

name:document.getElementById("pname").value,

category:document.getElementById("pcat").value,

image:reader.result,

description:document.getElementById("pdesc").value,

ingredients:document.getElementById("ping").value,

benefits:document.getElementById("pbenefits").value,

price:Number(document.getElementById("pprice").value),

stock:Number(document.getElementById("pstock").value),

status:"pending"

};

productsData.push(p);

saveProducts();

alert(
"Product uploaded successfully and sent for Admin approval."
);

closeModal("productModal");

document.getElementById("adminPanel").style.display="block";

refreshAdmin();

};

reader.readAsDataURL(file);

}


function saveProducts(){

localStorage.setItem(
"meraGideProducts",
JSON.stringify(productsData)
);

}


/* ORDERS */

function orders(){

let data=
JSON.parse(localStorage.getItem("meraGideOrders"))||[];

let html="<h3>Orders</h3>";

if(!data.length){

html+="<p>No orders yet.</p>";

}else{

data.forEach(o=>{

html+=`

<div style="
padding:15px;
border:1px solid #ddd;
border-radius:8px;
margin:10px 0">

<b>${o.id}</b><br>
Customer: ${safe(o.customer)}<br>
Total: ₹${o.total}<br>
Status: <b>${o.status}</b>

</div>

`;

});

}

document.getElementById("adminContent").innerHTML=html;

}


/* INFORMATION */

function about(){

showInfo(`

<h2>About Mera-Gide</h2>

<p style="line-height:1.8">

Mera-Gide is a Green Ayurveda marketplace designed
to connect customers with sellers of herbal,
natural and wellness products.

Our goal is to provide a simple and convenient
online shopping experience.

</p>

`);

}


function contact(){

showInfo(`

<h2>Contact Us</h2>

<div class="form">
<label>Name</label>
<input placeholder="Your Name">
</div>

<div class="form">
<label>Email</label>
<input type="email" placeholder="Your Email">
</div>

<div class="form">
<label>Message</label>
<textarea placeholder="Your Message"></textarea>
</div>

<button class="btn green"
onclick="alert('Message submitted.')">
Send Message
</button>

`);

}


function terms(){

showInfo(`
<h2>Terms and Conditions</h2>
<p style="line-height:1.8">
Users must provide accurate information.
Sellers are responsible for the products they list.
Mera-Gide may review, approve, reject or remove
product listings.
</p>
`);

}


function privacy(){

showInfo(`
<h2>Privacy Policy</h2>
<p style="line-height:1.8">
Mera-Gide respects user privacy.
Information should be used only for legitimate
shopping, seller, order and support purposes.
</p>
`);

}


function refund(){

showInfo(`
<h2>Return & Refund Policy</h2>
<p style="line-height:1.8">
Returns and refunds are subject to the applicable
seller policy and applicable consumer rules.
</p>
`);

}


function shipping(){

showInfo(`
<h2>Shipping Policy</h2>
<p style="line-height:1.8">
Shipping charges and delivery times may vary
according to seller and delivery location.
</p>
`);

}


/* HELPERS */

function showInfo(content){

document.getElementById("info").innerHTML=content;

document.getElementById("infoModal").style.display="block";

}


function closeModal(id){

document.getElementById(id).style.display="none";

}


function shop(){

document.getElementById("shop").scrollIntoView({
behavior:"smooth"
});

}


function home(){

window.scrollTo({
top:0,
behavior:"smooth"
});

}


function safe(t){

return String(t)
.replace(/&/g,"&amp;")
.replace(/</g,"&lt;")
.replace(/>/g,"&gt;")
.replace(/"/g,"&quot;")
.replace(/'/g,"&#039;");

}


/* START */

displayProducts();
updateCart();

</script>

</body>
</html>
