<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Half-Life Web</title>

<style>

body{
background:black;
color:#00ff99;
font-family:monospace;
text-align:center;
margin:0;
overflow:hidden;
}

#menu{
position:absolute;
top:40%;
width:100%;
}

button{
font-size:30px;
padding:20px 60px;
background:#111;
color:#00ff99;
border:2px solid #00ff99;
cursor:pointer;
}

#game{
display:none;
position:absolute;
top:0;
left:0;
width:100%;
height:100%;
background:black;
}

#hud{
position:absolute;
bottom:10px;
left:10px;
font-size:18px;
}

#ending{
display:none;
font-size:80px;
position:absolute;
top:40%;
width:100%;
color:white;
}

canvas{
background:#111;
margin-top:40px;
}

</style>
</head>

<body>

<div id="menu">
<h1>HALF-LIFE</h1>
<button onclick="startGame()">START</button>
</div>

<div id="game">

<canvas id="screen" width="800" height="450"></canvas>

<div id="hud">
HEALTH: 100<br>
SUIT: 100
</div>

</div>

<div id="ending">
bomoocpat
</div>

<script>

let canvas = document.getElementById("screen")
let ctx = canvas.getContext("2d")

let player = {x:400,y:225}
let keys = {}

document.addEventListener("keydown",e=>keys[e.key]=true)
document.addEventListener("keyup",e=>keys[e.key]=false)

function startGame(){

document.getElementById("menu").style.display="none"
document.getElementById("game").style.display="block"

gameLoop()

// simulate finishing the game
setTimeout(endGame,20000)

}

function gameLoop(){

update()
draw()

requestAnimationFrame(gameLoop)

}

function update(){

if(keys["w"]) player.y-=3
if(keys["s"]) player.y+=3
if(keys["a"]) player.x-=3
if(keys["d"]) player.x+=3

}

function draw(){

ctx.fillStyle="black"
ctx.fillRect(0,0,800,450)

ctx.fillStyle="#00ff99"
ctx.fillRect(player.x-10,player.y-10,20,20)

ctx.fillStyle="#00ff99"
ctx.fillText("Use WASD to move",10,20)

}

function endGame(){

document.getElementById("game").style.display="none"
document.getElementById("ending").style.display="block"

}

</script>

</body>
</html>
