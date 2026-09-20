<!doctype html>
<html lang="hi"><head>
<meta charset="utf-8"><meta name="viewport" content="width=device-width,initial-scale=1">
<title>Shop Mini App</title>
<script src="https://telegram.org/js/telegram-web-app.js"></script>
<style>
*{box-sizing:border-box}body{margin:0;background:#f6f7fb;font-family:Arial;color:#171717}.app{max-width:480px;margin:auto;padding:14px 14px 90px}.top{display:flex;justify-content:space-between;align-items:center;margin-bottom:15px}.logo{font-size:22px;font-weight:800}.wallet,.card,.offer{background:#fff;border:1px solid #e8e8e8;border-radius:18px;padding:14px}.hero{background:linear-gradient(135deg,#111827,#374151);color:#fff;border-radius:22px;padding:20px}.hero h1{margin:7px 0;font-size:25px}.hero p,.muted{font-size:12px;line-height:1.45;color:#777}.hero p{color:#ddd}.search{background:#fff;color:#777;border-radius:12px;padding:12px;margin-top:14px}.grid{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin:14px 0}.big{font-size:23px;font-weight:800;margin:7px 0}.btn{width:100%;border:0;border-radius:12px;padding:13px;margin-top:10px;background:#111827;color:white;font-weight:700}.section{margin-top:14px}.offer{display:flex;justify-content:space-between;margin-top:9px}.badge{background:#eef2ff;border-radius:20px;padding:5px 8px;font-size:11px}nav{position:fixed;bottom:0;left:0;right:0;background:#fff;border-top:1px solid #ddd;display:flex;justify-content:space-around;padding:9px}nav button{border:0;background:none;font-size:12px}#message{margin-top:12px;font-size:13px}
</style></head><body>
<div class="app">
<div class="top"><div class="logo">🛍️ Shop</div><div class="wallet">₹<span id="wallet">0</span> Wallet</div></div>
<section class="hero"><small>NEW USER OFFERS</small><h1>Apna offer check karo</h1><p>Eligibility verify hone ke baad available offer yahan show hoga.</p><div class="search">🔎 Product ya offer search</div></section>
<div class="grid">
<div class="card"><b>🎁 Normal Offer</b><div class="big">₹120–₹150</div><div class="muted">Eligible new users ke liye.</div><button class="btn" id="check">Check Offer</button></div>
<div class="card"><b>⚡ High Offer</b><div class="big">Up to ₹200</div><div class="muted">High-offer check ke liye ₹10 service fee.</div><button class="btn" id="high">Check High Offer</button></div>
</div>
<div class="section"><b>Available Offers</b>
<div class="offer"><div><b>₹120 OFF</b><div class="muted">Configured offer</div></div><span class="badge">Check</span></div>
<div class="offer"><div><b>₹150 OFF</b><div class="muted">Configured offer</div></div><span class="badge">Check</span></div>
<div class="offer"><div><b>₹200 तक</b><div class="muted">High-offer analysis</div></div><span class="badge">₹10</span></div></div>
<div class="card section"><b>📦 Orders</b><div class="muted">Abhi koi order nahi hai.</div><button class="btn" id="orders">Order History</button></div>
<div id="message" aria-live="polite"></div>
</div>
<nav><button>🏠<br>Home</button><button id="navOffer">🎁<br>Offer</button><button id="navWallet">💰<br>Wallet</button><button id="navOrders">📦<br>Orders</button><button id="navProfile">👤<br>Profile</button></nav>
<script>
const tg=window.Telegram?.WebApp;if(tg){tg.ready();tg.expand()}const m=document.getElementById('message');
const show=t=>m.textContent=t;
document.getElementById('check').onclick=()=>show('Real eligibility ke liye authorized verification/backend connect karna hoga.');
document.getElementById('high').onclick=()=>show('High-offer analysis aur ₹10 payment flow backend se connect hoga.');
document.getElementById('orders').onclick=()=>show('Order history backend connect hone ke baad dikhegi.');
document.getElementById('navOffer').onclick=()=>document.getElementById('check').click();
document.getElementById('navWallet').onclick=()=>show('Wallet sirf service/order fee ke liye hai; withdrawal nahi.');
document.getElementById('navOrders').onclick=()=>document.getElementById('orders').click();
document.getElementById('navProfile').onclick=()=>show('Profile/backend connection next step mein add hoga.');
</script></body></html>
