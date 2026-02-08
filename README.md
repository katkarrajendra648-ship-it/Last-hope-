<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Last Hope ❤️</title>

<style>
body{
    margin:0;
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    font-family:Arial, sans-serif;
    overflow:hidden;
    background:#ff4d6d;
}

/* falling hearts */
.heart{
    position:absolute;
    font-size:20px;
    animation:fall 6s linear infinite;
}
@keyframes fall{
    0%{transform:translateY(-10vh);opacity:1;}
    100%{transform:translateY(110vh);opacity:0;}
}

.card{
    width:380px;
    background:white;
    padding:20px;
    border-radius:20px;
    box-shadow:0 15px 40px rgba(0,0,0,0.4);
    text-align:center;
    position:absolute;
    z-index:2;
}

.card img{
    width:100%;
    border-radius:15px;
}

#text{
    font-size:16px;
    margin:15px 0;
    line-height:1.6;
    min-height:220px;
}

.buttons{
    margin-top:10px;
}

button{
    padding:10px 25px;
    font-size:16px;
    border:none;
    border-radius:25px;
    cursor:pointer;
}

.yes{
    background:#28a745;
    color:white;
    animation:pulse 1.5s infinite;
}

@keyframes pulse{
    0%{transform:scale(1);}
    50%{transform:scale(1.08);}
    100%{transform:scale(1);}
}

.no{
    background:#dc3545;
    color:white;
    position:relative;
}
</style>
</head>

<body>

<div class="card" id="card">
    <img src="mine.jpg" alt="mine">
    <p id="text"></p>

    <div class="buttons">
        <button class="yes" onclick="yes()">YES</button>
        <button class="no" id="no">NO</button>
    </div>
</div>

<script>
/* EXACT TEXT – NO CHANGE */
const message = `Hlo mazhi kaju katli 💋 mla nahi mahiti ki mi tujhya sang yevadha attract kaskay zalo. But tula sangatoy mahiti nahi mla ki ks kay but mla tujhyavar prem zalay te pn khup jast aani mla mahitiy tujhya baddal sagal kahi tari pn mla tujhyavarach prem zalay. Tula mahity ka mi sagalyana sangitalay ki mi tujhyavar prem karato aani mla tuch havi tujhya sarkhi pn nako. Aani tu thambshil rahashil mla sodun jashil mla kahi ghen den nahi but I know ki tu pahije. I love you love you love you so much much more and ever 🌍💗😘 fakt tuch.khup prem zalay tujhyavar tuch aani tuch pahije majhya black and white zindagi madhi colourfull person tu 🧿
Mazhi special one mazhi kaju katli 💋 mazhi aaichyaa hatachi puranpoli 💕😘🌎 love you babydoll mazhi 💗🫂😘🌎.
.
.
.
 Anjali i love you yar 🥺🤌💕🫂🌎🧿`;

/* typing animation */
let i = 0;
function typeText(){
    if(i < message.length){
        document.getElementById("text").innerHTML +=
            message.charAt(i) === "\n" ? "<br>" : message.charAt(i);
        i++;
        setTimeout(typeText, 40);
    }
}
typeText();

/* YES action */
function yes(){
    document.body.innerHTML = `
    <div style="
        height:100vh;
        display:flex;
        justify-content:center;
        align-items:center;
        background:linear-gradient(135deg,#ff758c,#ff7eb3);
        font-family:Arial;
        text-align:center;
        color:white;
        flex-direction:column;">
        <h1>Anjali ❤️</h1>
        <p>You are my forever 🌍💗</p>
    </div>`;
}

/* NO trap */
const noBtn = document.getElementById("no");
noBtn.addEventListener("mouseover", ()=>{
    const x = Math.random()*300 - 150;
    const y = Math.random()*300 - 150;
    noBtn.style.transform = `translate(${x}px, ${y}px)`;
});

/* hearts */
setInterval(()=>{
    const heart = document.createElement("div");
    heart.className = "heart";
    heart.innerHTML = "❤️";
    heart.style.left = Math.random()*100 + "vw";
    heart.style.fontSize = (Math.random()*20+15)+"px";
    document.body.appendChild(heart);
    setTimeout(()=>heart.remove(),6000);
},250);
</script>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Last Hope 💖</title>

  <style>
    body {
      margin: 0;
      height: 100vh;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
      font-family: 'Arial', sans-serif;
    }

    .container {
      background: rgba(255, 255, 255, 0.25);
      backdrop-filter: blur(10px);
      padding: 30px;
      border-radius: 20px;
      text-align: center;
      box-shadow: 0 0 25px rgba(255,0,100,0.3);
      animation: fadeIn 2s ease;
    }

    h1 {
      color: #fff;
      margin-bottom: 20px;
      animation: heartbeat 1.5s infinite;
    }

    img {
      width: 200px;
      border-radius: 15px;
      box-shadow: 0 0 15px rgba(255,255,255,0.6);
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: scale(0.9); }
      to { opacity: 1; transform: scale(1); }
    }

    @keyframes heartbeat {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.1); }
    }

    /* Floating hearts */
    .heart {
      position: absolute;
      bottom: -20px;
      font-size: 20px;
      animation: floatUp 6s linear infinite;
      opacity: 0.7;
    }

    @keyframes floatUp {
      0% { transform: translateY(0); opacity: 0; }
      10% { opacity: 1; }
      100% { transform: translateY(-110vh); opacity: 0; }
    }
  </style>
</head>

<body>

  <div class="container">
    <h1>Mine 💖</h1>
    <img src="photo.jpg" alt="Love Photo">
  </div>

  <script>
    setInterval(() => {
      const heart = document.createElement("div");
      heart.className = "heart";
      heart.innerHTML = "💖";
      heart.style.left = Math.random() * 100 + "vw";
      heart.style.animationDuration = (Math.random() * 3 + 4) + "s";
      document.body.appendChild(heart);

      setTimeout(() => heart.remove(), 6000);
    }, 400);
  </script>

</body>
</html>
