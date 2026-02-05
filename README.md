
<!DOCTYPE html>
<html>
<head>
<title>Happy Birthday Payal 🎂</title>

<style>
body{
  margin:0;
  padding:0;
  text-align:center;
  font-family: Arial;
  background: linear-gradient(to right,#ff758c,#ff7eb3);
  color:white;
}

.container{
  margin-top:30px;
}

img{
  width:250px;
  height:250px;
  border-radius:50%;
  border:5px solid white;
  object-fit:cover;
}

button{
  padding:12px 25px;
  font-size:18px;
  border:none;
  border-radius:20px;
  background:white;
  color:#ff4b7d;
  margin:10px;
}

.heart{
  position:absolute;
  color:red;
  animation: fall 5s linear infinite;
}

@keyframes fall{
  0%{top:-10%;}
  100%{top:100%;}
}

</style>

</head>

<body>

<div class="container">

<h1>Happy Birthday Payal 🎂</h1>

<h2>Captan 🫡 | Mendha 🐐</h2>

<img id="slideshow" src="photo1.jpg">

<br>

<button onclick="showMessage()">Birthday Message</button>

<p id="msg"></p>

<a href="https://wa.me/" target="_blank">
<button>Open WhatsApp</button>
</a>

</div>

<audio autoplay loop>
<source src="song.mp3" type="audio/mp3">
</audio>

<script>

let images = ["photo1.jpg","photo2.jpg"];
let i = 0;

setInterval(function(){
  i++;
  if(i >= images.length) i = 0;
  document.getElementById("slideshow").src = images[i];
}, 3000);

function showMessage(){
document.getElementById("msg").innerHTML =
"Have a wonderful birthday Payal 🎉";
}

function createHeart(){
const heart=document.createElement("div");
heart.classList.add("heart");
heart.innerHTML="❤️";
heart.style.left=Math.random()*100+"%";
heart.style.fontSize="20px";
document.body.appendChild(heart);
setTimeout(()=>heart.remove(),5000);
}

setInterval(createHeart,500);

</script>

</body>
</html>
