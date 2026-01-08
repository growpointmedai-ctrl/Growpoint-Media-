# Growpoint-Media-
Digital marketing agency
<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Grow Point Media | Digital Marketing for Local Business</title>
<meta name="description" content="Grow Point Media helps local businesses grow using Google Maps, Social Media and Ads. Book free consultation.">
<style>
body{margin:0;font-family:Arial,Helvetica,sans-serif;background:#f4f6f8;color:#222}
header{background:#0d47a1;color:#fff;padding:20px}
header h1{margin:0}
nav a{color:#fff;margin-right:15px;text-decoration:none;font-weight:bold}
section{padding:30px}
.card{background:#fff;padding:20px;border-radius:8px;margin-bottom:20px;box-shadow:0 2px 6px rgba(0,0,0,.1)}
button{background:#0d47a1;color:#fff;border:none;padding:10px 16px;border-radius:6px;cursor:pointer}
button:hover{background:#08306b}
input,select{width:100%;padding:10px;margin:6px 0;border:1px solid #ccc;border-radius:5px}
.hidden{display:none}
.footer{background:#111;color:#fff;text-align:center;padding:15px}
.whatsapp{position:fixed;bottom:15px;right:15px;background:#25d366;color:#fff;padding:12px 18px;border-radius:50px;text-decoration:none;font-weight:bold}
table{width:100%;border-collapse:collapse}
th,td{border:1px solid #ccc;padding:8px;text-align:left}
th{background:#eee}
</style>
</head>

<body>

<header>
<h1>Grow Point Media</h1>
<p>Local Business Digital Growth Agency</p>
<nav>
<a href="#services">Services</a>
<a href="#book">Book</a>
<a href="#track">Track Order</a>
<a href="#admin">Admin</a>
</nav>
</header>

<section class="card">
<h2>Grow Your Local Business 🚀</h2>
<p>Hum local dukaan, school, service providers ko Google Map, Social Media aur Ads ke through real customers dilate hain.</p>
<p><b>Followers nahi, customers chahiye?</b> To Grow Point Media sahi choice hai.</p>
<button onclick="location.href='#book'">Book Free Consultation</button>
</section>

<section id="services">
<h2>Our Services & Pricing</h2>

<div class="card">
<h3>📍 Google Map Setup – ₹999 (One Time)</h3>
<p>Business Google Map par nahi hai to log aapko dhund hi nahi paayenge.</p>
<p><b>Nuksaan:</b> Calls, visits aur trust sab loss.</p>
</div>

<div class="card">
<h3>🚀 Google Map Growth Plan – ₹1999 / month</h3>
<p>Reviews, ranking aur local visibility badhane ke liye.</p>
<p><b>Nuksaan:</b> Competitors upar aa jaate hain.</p>
</div>

<div class="card">
<h3>📱 Social Media Management – ₹1499 / month</h3>
<p>Professional posts + brand presence.</p>
<p><b>Nuksaan:</b> Business outdated dikhta hai.</p>
</div>

<div class="card">
<h3>📢 Facebook / Instagram Ads – ₹2499 (One Time)</h3>
<p>Direct leads aur enquiries ke liye ads.</p>
<p><b>Nuksaan:</b> Paid reach miss hoti hai.</p>
</div>

<div class="card">
<h3>🌐 Complete Digital Presence – ₹3999 / month</h3>
<p>Google Map + Social Media + Ads support.</p>
<p><b>Best for serious business growth.</b></p>
</div>

<div class="card">
<h3>🆓 Free Consultation – ₹0</h3>
<p>Business analysis + growth suggestion.</p>
</div>
</section>

<section id="book" class="card">
<h2>Book Service</h2>
<form id="bookingForm">
<input required placeholder="Your Name" id="name">
<input required placeholder="Business Name" id="business">
<input required placeholder="Phone Number" id="phone">
<select id="service">
<option>Google Map Setup</option>
<option>Google Map Growth Plan</option>
<option>Social Media Management</option>
<option>Facebook / Instagram Ads</option>
<option>Complete Digital Presence</option>
<option>Free Consultation</option>
</select>
<button type="submit">Submit Booking</button>
</form>
<p id="successMsg" class="hidden">✅ Booking Successful! Thank you for choosing Grow Point Media.</p>
</section>

<section id="track" class="card">
<h2>Track Your Order</h2>
<input placeholder="Enter Order ID" id="trackId">
<button onclick="trackOrder()">Track</button>
<p id="trackResult"></p>
</section>

<section id="admin" class="card">
<h2>Admin Login</h2>
<input placeholder="Username" id="adminUser">
<input type="password" placeholder="Password" id="adminPass">
<button onclick="adminLogin()">Login</button>

<div id="dashboard" class="hidden">
<h3>Admin Dashboard</h3>
<p>Total Orders: <span id="totalOrders">0</span></p>
<p>Total Earnings: ₹<span id="totalEarnings">0</span></p>
<table>
<thead>
<tr><th>Order ID</th><th>Name</th><th>Service</th><th>Payment</th></tr>
</thead>
<tbody id="orderTable"></tbody>
</table>
</div>
</section>

<a class="whatsapp" target="_blank"
href="https://wa.me/918233803191?text=Hello%20Grow%20Point%20Media">
WhatsApp
</a>

<div class="footer">
© 2026 Grow Point Media | Founder: Sanjay Kumar
</div>

<script>
let orders = JSON.parse(localStorage.getItem("orders") || "[]");

document.getElementById("bookingForm").onsubmit = function(e){
e.preventDefault();
let id = "GPM" + Date.now();
let order = {
id:id,
name:name.value,
business:business.value,
phone:phone.value,
service:service.value,
payment:"Pending"
};
orders.push(order);
localStorage.setItem("orders",JSON.stringify(orders));
successMsg.classList.remove("hidden");

window.open(
`https://wa.me/918233803191?text=New%20Booking%0AName:%20${order.name}%0AService:%20${order.service}%0AOrderID:%20${id}`,
"_blank"
);
};

function trackOrder(){
let id = trackId.value;
let o = orders.find(x=>x.id===id);
trackResult.innerText = o ?
`Service: ${o.service}, Payment: ${o.payment}` :
"Order not found";
}

function adminLogin(){
if(adminUser.value==="admin" && adminPass.value==="1234"){
dashboard.classList.remove("hidden");
loadDashboard();
}else{alert("Invalid login");}
}

function loadDashboard(){
orderTable.innerHTML="";
totalOrders.innerText=orders.length;
let total=0;
orders.forEach(o=>{
let tr=document.createElement("tr");
tr.innerHTML=`<td>${o.id}</td><td>${o.name}</td><td>${o.service}</td><td>${o.payment}</td>`;
orderTable.appendChild(tr);
});
totalEarnings.innerText=total;
}
</script>

</body>
</html>
