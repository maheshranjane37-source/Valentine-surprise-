<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Happy Valentine's Day ❤️</title>

<style>
body{
  margin:0;
  font-family:Arial;
  text-align:center;
  background:#ffe6f0;
}

.page{
  height:100vh;
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items:center;
}

button{
  padding:15px 25px;
  font-size:18px;
  border:none;
  border-radius:10px;
  background:#ff4d88;
  color:white;
}

#balloonPage{
  display:none;
}

.grid{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:15px;
  padding:20px;
}

.balloon{
  font-size:60px;
  cursor:pointer;
}

.polaroid{
  display:none;
  background:white;
  padding:10px;
  box-shadow:0px 4px 10px rgba(0,0,0,0.2);
}

.polaroid img{
  width:100%;
}
</style>
</head>

<body>

<!-- 🎁 MUSIC -->
<audio id="music" src="music.mp3" loop></audio>

<!-- ❤️ FIRST PAGE -->
<div class="page" id="firstPage">
  <h1>Happy Valentine's Day ❤️</h1>
  <p>You mean the world to me...</p>
  <button onclick="startSurprise()">Tap For Your Surprise</button>
</div>

<!-- 🎈 BALLOON PAGE -->
<div class="page" id="balloonPage">
  <h2>Pop the balloons 🎈</h2>

  <div class="grid">

    <div onclick="pop(1)">
      <div class="balloon" id="b1">🎈</div>
      <div class="polaroid" id="p1"><img src="photo1.jpg"></div>
    </div>

    <div onclick="pop(2)">
      <div class="balloon" id="b2">🎈</div>
      <div class="polaroid" id="p2"><img src="photo2.jpg"></div>
    </div>

    <div onclick="pop(3)">
      <div class="balloon" id="b3">🎈</div>
      <div class="polaroid" id="p3"><img src="photo3.jpg"></div>
    </div>

    <div onclick="pop(4)">
      <div class="balloon" id="b4">🎈</div>
      <div class="polaroid" id="p4"><img src="photo4.jpg"></div>
    </div>

    <div onclick="pop(5)">
      <div class="balloon" id="b5">🎈</div>
      <div class="polaroid" id="p5"><img src="photo5.jpg"></div>
    </div>

    <div onclick="pop(6)">
      <div class="balloon" id="b6">🎈</div>
      <div class="polaroid" id="p6"><img src="photo6.jpg"></div>
    </div>

  </div>
</div>

<script>
function startSurprise(){
  document.getElementById("firstPage").style.display="none";
  document.getElementById("balloonPage").style.display="flex";

  // mobile autoplay works only after tap
  document.getElementById("music").play();
}

function pop(n){
  document.getElementById("b"+n).style.display="none";
  document.getElementById("p"+n).style.display="block";
}
</script>

</body>
</html>
