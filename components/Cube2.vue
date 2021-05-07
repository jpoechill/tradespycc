<template>
    <div>
        <h1>Hover me:</h1>
        <div class="cube">
        <div class="cubeFace"></div>
        <div class="cubeFace face2"></div>
        </div>
    </div>
</template>

<script>
export default {}
</script>

<style>
 body{
  perspective-origin:50% -100%;
  perspective: 900px;
  overflow:hidden;
}
h1{position:absolute;font-family:sans-serif;}
.cube {
  position:relative;
  padding-bottom:20%;
  transform-style: preserve-3d;
  transform-origin: 50% 100%;
  transform:rotateY(45deg) rotateX(0);
  transition:transform 3s;
}
.cubeFace {
  position: absolute;
  left:40%;top:0;
  width: 20%;height:100%;
  margin: 0 auto;
  transform-style: inherit;
  background: #C52329;
  box-shadow:inset 0 0 0 5px #fff; 
  transform-origin:50% 50%;
  transform: rotateX(90deg);
  backface-visibility:hidden;
}
.face2{
  transform-origin:50% 50%;
  transform: rotatez(90deg) translateX(100%) rotateY(90deg);
}
.cubeFace:before, .cubeFace:after {
  content: '';
  position: absolute;
  width: 100%;
  height: 100%;
  transform-origin:0 0;
  background: inherit;
  box-shadow:inherit;
  backface-visibility:inherit;
}
.cubeFace:before {
  top: 100%; left: 0;
  transform: rotateX(-90deg);
}
.cubeFace:after {
  top: 0; left: 100%;
  transform: rotateY(90deg);
}

body:hover .cube{
  transform:rotateY(405deg) rotateX(360deg);
}

</style>
