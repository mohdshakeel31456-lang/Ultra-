<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AI Tools Ultimate</title>

<style>
body {margin:0;font-family:Arial;background:#020617;color:white;}
header {padding:15px;text-align:center;font-size:22px;background:#0f172a;}

.search {padding:10px;text-align:center;}
input {width:90%;padding:10px;border-radius:10px;border:none;}

.container {padding:15px;}

.card {
  background:#1e293b;
  padding:15px;
  margin:12px 0;
  border-radius:12px;
}

button {
  margin-top:10px;
  padding:8px 12px;
  border:none;
  border-radius:6px;
  background:#22c55e;
  color:white;
}

.locked {
  opacity:0.5;
}

.premium {
  background:#facc15;
  color:black;
}

.email-box {
  text-align:center;
  padding:20px;
  background:#0f172a;
}

footer {text-align:center;padding:15px;font-size:12px;}
</style>
</head>

<body>

<header>🚀 AI Tools Ultimate</header>

<div class="search">
<input type="text" id="search" placeholder="Search tools..." onkeyup="searchTools()">
</div>

<div class="email-box">
<h3>🔥 Get FREE AI Tools List</h3>
<input type="email" id="email" placeholder="Enter email">
<br><br>
<button onclick="saveEmail()">Get Access</button>
</div>

<div class="container" id="tools">

<div class="card" data-name="capcut video">
<h2>CapCut</h2>
<p>Best video editing tool</p>
<button onclick="go('https://www.capcut.com')">Use Now</button>
</div>

<div class="card locked" data-name="premium ai secret">
<h2>🔥 Secret AI Tool (Premium)</h2>
<p>Unlock after email</p>
<button class="premium" onclick="unlock()">Unlock</button>
</div>

</div>

<footer>💸 Affiliate + Digital Product Ready</footer>

<script>

function searchTools() {
  let val = document.getElementById("search").value.toLowerCase();
  document.querySelectorAll(".card").forEach(card=>{
    let name = card.getAttribute("data-name");
    card.style.display = name.includes(val) ? "block":"none";
  });
}

function go(url){
  window.open(url,"_blank");
}

function saveEmail(){
  let email = document.getElementById("email").value;
  if(email){
    localStorage.setItem("userEmail", email);
    alert("Access unlocked!");
  }
}

function unlock(){
  let email = localStorage.getItem("userEmail");
  if(email){
    alert("Premium unlocked!");
  } else {
    alert("Enter email first!");
  }
}

</script>

</body>
</html>
