<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sorry Panda ❤️</title>

<style>
*{margin:0;padding:0;box-sizing:border-box;}

body{
font-family:Arial,sans-serif;
overflow:hidden;
transition:background 2s ease;
background:linear-gradient(135deg,#ff9a9e,#fad0c4);
}

.page{
display:none;
height:100vh;
text-align:center;
padding:20px;
position:relative;
}

.active{display:block;}

.panda{
font-size:130px;
animation:bounce 1.5s infinite;
cursor:pointer;
}

@keyframes bounce{
0%,100%{transform:translateY(0);}
50%{transform:translateY(-25px);}
}

h1,h2,p{color:#fff;text-shadow:0 0 10px rgba(0,0,0,0.2);}

button{
padding:12px 25px;
font-size:20px;
border:none;
border-radius:30px;
margin:10px;
cursor:pointer;
font-weight:bold;
transition:.3s;
}

#yesBtn{background:#ff4081;color:white;}
#noBtn{background:#888;color:white;}

button:hover{transform:scale(1.08);}

.frame{
display:flex;
justify-content:center;
gap:20px;
flex-wrap:wrap;
margin-top:20px;
}

.card{
width:300px;
background:white;
border-radius:20px;
padding:10px;
box-shadow:0 0 15px rgba(0,0,0,0.2);
border:3px solid #fff;
animation:glow 2s infinite alternate;
}

@keyframes glow{
0%{border-color:#ff9a9e;}
50%{border-color:#fad0c4;}
100%{border-color:#ff9a9e;}
}

.card img{
width:100%;
height:350px;
object-fit:cover;
border-radius:15px;
}

.lyric{
color:#ff4081;
font-weight:bold;
margin:5px 0;
}

.name{
font-size:20px;
font-weight:bold;
margin-top:5px;
}

.heart{
position:absolute;
color:red;
font-size:25px;
animation:float 6s linear forwards;
}

@keyframes float{
0%{transform:translateY(100vh) scale(0.5);opacity:1;}
100%{transform:translateY(-100px) scale(1.5);opacity:0;}
}

.sparkle{
position:absolute;
color:white;
font-size:18px;
animation:sparkle 3s linear forwards;
}

@keyframes sparkle{
0%{opacity:0;transform:scale(0);}
50%{opacity:1;transform:scale(1);}
100%{opacity:0;transform:scale(0);}
}

.final{
text-align:center;
}

.final img{
width:350px;
height:400px;
border-radius:20px;
box-shadow:0 0 20px rgba(0,0,0,0.3);
margin-top:20px;
}

.final-text{
color:#ff4081;
font-size:24px;
font-weight:bold;
margin-top:20px;
}

</style>
</head>

<body>

<!-- PAGE 1 -->
<div class="page active" id="page1">

<div class="panda">🐼</div>

<h1>Sorry My Love ❤️</h1>
<p>Panda is saying sorry 🥺</p>

<button id="yesBtn" onclick="openPage2()">It's OK 💗</button>
<button id="noBtn" onclick="grow()">No 😒</button>

</div>

<!-- PAGE 2 -->
<div class="page" id="page2">

<h2>Our Love Story ❤️</h2>

<div class="frame">

<div class="card">
<div class="lyric">Hukum aapka tha jo maine na maana 🙄😘💞</div>
<img src="jpg">
<div class="name">You: 💗</div>
<div class="lyric">Sazaa jo bhi dogi woh manzoor hogi 🎀</div>
</div>

<div class="card">
<div class="lyric">Khatavaar hoon main na aaya nibhaana 😚</div>
<img src=jpg">
<div class="name">Me: ❤️</div>
<div class="lyric">Aji meri mushkil tabhi door hogi 🙇‍♂️🤌🫂🙏</div>
</div>

</div>

<h2>Do You Love Me? 🥺</h2>
<button onclick="openPage3()">YES 💘</button>

</div>

<!-- PAGE 3 -->
<div class="page final" id="page3">

<h1>Mine ❤️</h1>

<img src="YOUR jpg">
  


jpg">

<div class="final-text">
I Love You Mazhi WiFi More And More And Ever 🌍🫂🧿😘
</div>

</div>

<script>

// auto background change every 2 sec
const bg=[
"linear-gradient(135deg,#ff9a9e,#fad0c4)",
"linear-gradient(135deg,#a18cd1,#fbc2eb)",
"linear-gradient(135deg,#84fab0,#8fd3f4)",
"linear-gradient(135deg,#f6d365,#fda085)",
"linear-gradient(135deg,#fccb90,#d57eeb)"
];

let i=0;
setInterval(()=>{
i=(i+1)%bg.length;
document.body.style.background=bg[i];
},2000);

// hearts
function heart(){
let h=document.createElement("div");
h.className="heart";
h.innerHTML="❤️";
h.style.left=Math.random()*100+"vw";
h.style.fontSize=(20+Math.random()*30)+"px";
document.body.appendChild(h);
setTimeout(()=>h.remove(),6000);
}
setInterval(heart,300);

// sparkles
function sparkle(){
let s=document.createElement("div");
s.className="sparkle";
s.innerHTML="✨";
s.style.left=Math.random()*100+"vw";
s.style.top=Math.random()*100+"vh";
document.body.appendChild(s);
setTimeout(()=>s.remove(),3000);
}
setInterval(sparkle,500);

// button grow effect
let yes=22,no=22;
function grow(){
yes+=8;
no=Math.max(no-3,10);
document.getElementById("yesBtn").style.fontSize=yes+"px";
document.getElementById("noBtn").style.fontSize=no+"px";
}

// pages
function openPage2(){
document.getElementById("page1").classList.remove("active");
document.getElementById("page2").classList.add("active");
}

function openPage3(){
document.getElementById("page2").classList.remove("active");
document.getElementById("page3").classList.add("active");
}

</script>

</body>
</html>
