<template>
  <div>
   
    <!-- 4 -->
    <div class="loader loader--style4" title="3">
    <svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
        width="30px" height="24px" viewBox="0 0 24 24" style="enable-background:new 0 0 50 50;" xml:space="preserve">
        <rect x="0" y="0" width="6" height="7" fill="#B7FBFF">
        <animateTransform  attributeType="xml"
            attributeName="transform" type="scale"
            values="1,1; 1,3; 1,1"
            begin="0s" dur="1.45s" repeatCount="indefinite" />       
        </rect>

        <rect x="10" y="0" width="6" height="7" fill="#75E9FE">
        <animateTransform  attributeType="xml"
            attributeName="transform" type="scale"
            values="1,1; 1,3; 1,1"
            begin="0.2s" dur="1.45s" repeatCount="indefinite" />       
        </rect>
        <rect x="20" y="0" width="6" height="7" fill="#71DCF7">
        <animateTransform  attributeType="xml"
            attributeName="transform" type="scale"
            values="1,1; 1,3; 1,1"
            begin="0.4s" dur="1.45s" repeatCount="indefinite" />       
        </rect>
    </svg>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
.loader{
  margin: 0 0 1em;
  height: 100px;
  width: 20%;
  text-align: center;
  padding: .5em;
  margin: 0 auto 1em;
  display: inline-block;
  vertical-align: top;
}

/*
  Set the color of the icon
*/
/* svg path, */
/* svg rect{
  fill: orange;
} */
</style>
