<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Love ❤️</title>

<style>

body{
margin:0;
height:100vh;
overflow:hidden;
display:flex;
justify-content:center;
align-items:center;
text-align:center;
font-family:cursive;
background: linear-gradient(135deg,#ff9a9e,#fad0c4);
color:white;
}

#countdown{
font-size:100px;
text-shadow:0 0 25px pink;
}

#message{
font-size:35px;
display:none;
white-space:pre-line;
text-shadow:0 0 15px #ff4da6;
}

.button{
position:absolute;
bottom:50px;
padding:12px 30px;
border:none;
border-radius:30px;
background:#ff4da6;
color:white;
font-size:18px;
cursor:pointer;
}

.heart{
position:absolute;
color:#ff3366;
pointer-events:none;
animation:float 5s linear forwards;
}

@keyframes float{
0%{transform:translateY(100vh) scale(0.5);opacity:1;}
100%{transform:translateY(-10vh) scale(1.5);opacity:0;}
}

</style>
</head>

<body>

<div id="countdown"></div>

<div id="message">
"To my problem" ❤️

ခုတလော အဆင်မပြေတာတွေရှိခဲ့ရင် တောင်းပန်ပါတယ်။
မင်းကို အရမ်းချစ်တယ် 💕
မင်းကို ဂရုစိုက်ပေးချင်တယ်။
နားလည်မူတွေ လွဲနေတာလေးတွေရှိရင်လည်း တောင်းပန်ပါတယ်။
ကို့မှာမင်းပဲ ရှိတာမို့ တခါတလေ ကိုက အစိုးရိမ်လွန် အတွေးလွန်ပြိး
ပြောမှားဆိုမှားတာလေးတွေရှိရင် နားလည်ပေးစေချင်တယ်...
ဒီစာက မင်းအတွက်သီးသန့်လုပ်ထားတာမို့ မင်းလေးကိုပဲ ဖတ်စေချင်တယ်။
ဒီနေ့လည်း မင်းကို အရမ်းလွမ်းတယ် သတိရတယ်.... အရမ်းချစ်ပါတယ်... ❤️
</div>

<button class="button" onclick="startLove()">For You Only ❤️</button>

<audio id="bgm" loop>
<source src="https://youtu.be/GxldQ9eX2wo" type="audio/mp3">
</audio>

<script>

function startLove(){

let count=3;
let cd=document.getElementById("countdown");
let msg=document.getElementById("message");

let timer=setInterval(()=>{

cd.innerHTML=count;

if(count===0){
clearInterval(timer);
cd.style.display="none";
msg.style.display="block";
setInterval(createHeart,120);

setTimeout(()=>{
document.getElementById("bgm").play().catch(()=>{});
},500);

}else{
count--;
}

},1000);

}

function createHeart(){
let heart=document.createElement("div");
heart.className="heart";
heart.innerHTML="💖";
heart.style.left=Math.random()*100+"vw";
heart.style.top="100vh";
heart.style.fontSize=(15+Math.random()*30)+"px";

document.body.appendChild(heart);
setTimeout(()=>heart.remove(),5000);
}

</script>

</body>
</html>
