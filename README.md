<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Sushma ❤️</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial,sans-serif;
}
body{
    background:linear-gradient(135deg,#ff9a9e,#fad0c4,#fad0c4);
    display:flex;
    justify-content:center;
    align-items:center;
    height:100vh;
    overflow:hidden;
}
.card{
    width:350px;
    background:#fff;
    padding:30px;
    border-radius:20px;
    text-align:center;
    box-shadow:0 10px 30px rgba(0,0,0,.2);
    position:relative;
}
h1{
    color:#ff3d7f;
    margin-bottom:15px;
}
p{
    margin-bottom:20px;
    color:#555;
}
button{
    padding:12px 28px;
    border:none;
    border-radius:10px;
    font-size:18px;
    cursor:pointer;
    transition:.3s;
}
#yes{
    background:#28a745;
    color:#fff;
}
#no{
    background:#ff4d4d;
    color:#fff;
    margin-left:10px;
    position:relative;
}
#message{
    margin-top:20px;
    font-size:20px;
    color:#ff3d7f;
    font-weight:bold;
}
#happy{
    position:fixed;
    inset:0;
    background:linear-gradient(135deg,#ff6ec4,#7873f5);
    display:none;
    justify-content:center;
    align-items:center;
    flex-direction:column;
    color:white;
    text-align:center;
}
#happy h1{
    color:white;
    font-size:42px;
}
#happy p{
    color:white;
    font-size:22px;
}
.heart{
    position:absolute;
    color:red;
    font-size:20px;
    animation:float 5s linear infinite;
}
@keyframes float{
from{
transform:translateY(100vh);
opacity:1;
}
to{
transform:translateY(-120vh);
opacity:0;
}
}
</style>
</head>
<body>

<div class="card">
<h1>Sushma, Will You Be Mine? ❤️</h1>
<p>Dear Sushma, You are very special to me. 💖</p>

<button id="yes">Yes 💕</button>
<button id="no">No 💔</button>

<div id="message"></div>
</div>

<div id="happy">
<h1>YAY!! ❤️🥳</h1>
<p>Thank You, Sushma! You made my day! 💕</p>
<h2>Sushma ❤️ Forever Starts Today 💍</h2>
</div>

<script>
let no=document.getElementById("no");
let msg=document.getElementById("message");
let count=0;

no.onclick=function(){

count++;

if(count==1){
msg.innerHTML="🥺 Please think again, Sushma... ❤️";
}
else{
no.style.position="fixed";
moveButton();

no.onmouseover=moveButton;
no.onclick=moveButton;
}
}

function moveButton(){
let x=Math.random()*(window.innerWidth-120);
let y=Math.random()*(window.innerHeight-60);

no.style.left=x+"px";
no.style.top=y+"px";
}

document.getElementById("yes").onclick=function(){

document.querySelector(".card").style.display="none";
document.getElementById("happy").style.display="flex";

for(let i=0;i<80;i++){
let h=document.createElement("div");
h.className="heart";
h.innerHTML="❤️";
h.style.left=Math.random()*100+"vw";
h.style.animationDuration=(3+Math.random()*3)+"s";
h.style.fontSize=(15+Math.random()*25)+"px";
document.body.appendChild(h);
}
}
</script>

</body>
</html>
