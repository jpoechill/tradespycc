<template>
  <div class="wrapper">
    <div class="wrapper" id="cubewrapper">
        <div class="poswrap">
        <div class="floatwrap">
        <div class="spinwrap">
        <div class="tran1">
        <div class="tran2">
            <div class="cube">
                <div class="cube_face">
                </div>
                <div class="cube_face">
                </div>
                <div class="cube_face">
                </div>
                <div class="cube_face">
                </div>
                <div class="cube_face">
                </div>
                <div class="cube_face">
                </div>
            </div>
        </div>
        </div>
        </div>
        </div>
        </div>
  
</div>
  </div>
</template>

<script>
export default {}
</script>

<style>
  /*54.7 degrees.
35.3*/

/* - - - - - Wrappers - - - - - */

.wrapper{
    perspective: 100px;
    perspective-origin: 50% 50%;
    
    margin: 0 auto;
    width: 100%;
    height: 200px;
    z-index: -1;

    
        overflow: hidden;
}

.poswrap{
    transform-style: preserve-3d;
    position: absolute;
    left:50%;
    top: 5%;
}

.tran1{
    transform-style: preserve-3d;
    transform: rotateX(35.3deg);
}

.tran2{
    transform-style: preserve-3d;
    transform: rotateZ(45deg);
}




/* - - - - - Animation - - - - - */

.floatwrap{
    transform-style: preserve-3d;
    animation: float 10s infinite cubic-bezier(.5, 0, .5, 1);

}

.spinwrap{
    transform-style: preserve-3d;
    animation: spin 30s infinite linear;
}

@keyframes float{
    0% {transform: translateY(15px);}
    50% {transform: translateY(-15px);}
    100% {transform: translateY(15px);}
}

@keyframes spin {
       from{transform: rotateY(0deg);}
       to{transform: rotateY(-360deg);} 
    }




/* - - - - - Cube properties - - - - - */

.cube{
    position: absolute;
    transform-style: preserve-3d;
    transform: translateZ(-100px);
    top: 50%;
    left: 50%;
}

.cube_face{
    position: absolute;
    top: -40;
    left: -40;
    transform-origin: center;
    
    width: 50px;
    height: 50px;
    background-color: #333;
    box-shadow: 0px 0px 0px 2px #fff inset;
    
    text-align: center;
    font-size: 10px;
    line-height: 10px;
    color: RGBA(255, 255, 255, 0);

}


/* - - - - - Additional cube styling - - - - - */



.cube :nth-child(even){
    background: linear-gradient(to top left, #666, #222 );
    color: linear-gradient(to top left, #666, #222 );
}

.cube :nth-child (odd){
        
}



@keyframes facereflect{
    0%{background-color: #333;}
    10%{background-color: #666;}
    20%{background-color: #333;}
}



/* - - - - - Cube face transforms - - - - -
Front, Back, Left, Right, Top, Bottom*/

.cube :nth-child(1){
    animation: facereflect 30s infinite linear;
    animation-delay: 0s;
    transform:
        translateZ(40px);
}
.cube :nth-child(2){
    transform: rotateY(180deg)
        translateZ(40px)
         rotateZ(90deg);
}
.cube :nth-child(3){
    animation: facereflect 30s infinite linear;
    animation-delay: 20s;
    transform: rotateY(-90deg)
        translateZ(40px)
               rotateZ(90deg);
}
.cube :nth-child(4){
    transform: rotateY(90deg)
        translateZ(40px);
}
.cube :nth-child(5){
    animation: facereflect 30s infinite linear;
    animation-delay: 10s;
    transform: rotateX(90deg)
        translateZ(40px)
               rotateZ(-90deg);
}
.cube :nth-child(6){
    transform: rotateX(-90deg)
        translateZ(40px);
}

</style>
