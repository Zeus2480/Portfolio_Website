<template>
   <div class="tw-h-screen tw-w-full tw-p-20">
      <div class="tw-flex tw-h-full">
         <div
            class="tw-w-1/2 tw-h-full tw-bg-slate-600 tw-flex tw-justify-center tw-items-center"
         ></div>
         <div
            class="tw-w-1/2 tw-h-full tw-flex tw-justify-center tw-items-center tw-relative"
         >
            <div class="main">
               <div class="inner-circle">
                  <div class="circle1"> <img src="../assets/images/adobe-illustrator-seeklogo.com.svg" alt=""></div>
                  <div class="circle2"><img src="../assets/images/figma-seeklogo.com.svg" alt=""></div>
                  <div class="circle3"><img src="../assets/images/htmlLogo.svg" alt=""></div>
                  <div class="circle4"><img src="../assets/images/cssLogo.svg" alt=""></div>
               </div>
               <div class="outer-circle">
                  <div class="circle6"><img src="../assets/images/vuejs-seeklogo.com.svg" alt=""></div>
                  <div class="circle5"><img src="../assets/images/JavascriptLogo.svg" alt=""></div>
                  <div class="circle7"><img src="../assets/images/tailwindLogo.svg" alt=""></div>
                  <div class="circle8"><img src="../assets/images/NodeJSLogo.svg" alt=""></div>
               </div>
            </div>
         </div>
        
      </div>
   </div>
</template>

<style>
.main{
    width: 100px;
    height:100px;
    border:1px solid #CCC;
    position:absolute;
    top:0; bottom:0; left:0;right:0;
    margin:auto;
    background-color: aquamarine;
    border-radius:50%; 
  }
  .inner-circle{
    width: 200px;
    height:200px;
    border:1px solid #CCC;
    /* position:absolute; */
    margin: 200px;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    margin:auto;
    border-radius:50%; 
    margin: -48px;
  }
  .outer-circle{
    width: 400px;
    height:400px;
    border:1px solid #CCC;
    position:absolute;
    bottom: -150%;
    right: -150%;
    margin:auto;
    border-radius:50%; 
  }
.circle1 {
    width: 30px;    
    height: 30px;
    object-fit: contain;
   position: absolute;
   top: 0;
   bottom: 0;
   left: 0;
   right: 0;
   overflow: hidden;
   margin: auto;
   animation: circle1 10s linear infinite;
}

@keyframes circle1 {
   0% {
      transform: rotate(0deg) translate(-100px) rotate(0deg);
   }
   100% {
      transform: rotate(360deg) translate(-100px) rotate(-360deg);
   }
}
/*4 circles each rotate at 90 degree apart*/
.circle2 {
   height: 30px;
   width: 20px;
   position: absolute;
   object-fit: contain;
   top: 0;
   bottom: 0;
   left: 0;
   right: 0;
   overflow: hidden;
   margin: auto;
   animation: circle2 10s linear infinite;
}
@keyframes circle2 {
   0% {
      transform: rotate(90deg) translate(-100px) rotate(-90deg);
   }
   100% {
      transform: rotate(450deg) translate(-100px) rotate(-450deg);
   }
}
.circle3 {
   width: 25px;
   height: 30px;
   position: absolute;
   top: 0;
   bottom: 0;
   left: 0;
   right: 0;
   overflow: hidden;
   margin: auto;
   animation: circle3 10s linear infinite;
}
@keyframes circle3 {
   0% {
      transform: rotate(180deg) translate(-100px) rotate(-180deg);
   }
   100% {
      transform: rotate(540deg) translate(-100px) rotate(-540deg);
   }
}
.circle4 {
   width: 25px;
   height: 30px;
   position: absolute;
   top: 0;
   bottom: 0;
   left: 0;
   right: 0;
   overflow: hidden;
   margin: auto;
   animation: circle4 10s linear infinite;
}
@keyframes circle4 {
   0% {
      transform: rotate(270deg) translate(-100px) rotate(-270deg);
   }
   100% {
      transform: rotate(630deg) translate(-100px) rotate(-630deg);
   }
}
/*2 rings one outer and one inner each ring has 4 circle separated at 90 degree apart*/
.circle5 {
   width: 30px;
   height: 30px;
   position: absolute;
   top: 0;
   bottom: 0;
   left: 0;
   right: 0;
   overflow: hidden;
   margin: auto;
   animation: circle5 10s linear infinite;
}
@keyframes circle5 {
   0% {
      transform: rotate(45deg) translate(-200px) rotate(45deg);
   }
   100% {
      transform: rotate(405deg) translate(-200px) rotate(-405deg);
   }
}
.circle6 {
   width: 30px;
   height: 30px;
   position: absolute;
   top: 0;
   bottom: 0;
   left: 0;
   right: 0;
   overflow: hidden;
   margin: auto;
   animation: circle6 10s linear infinite;
}
@keyframes circle6 {
   0% {
      transform: rotate(135deg) translate(-200px) rotate(-135deg);
   }
   100% {
      transform: rotate(495deg) translate(-200px) rotate(-495deg);
   }
}
.circle7 {
   width: 30px;
   height: 30px;
   position: absolute;
   top: 0;
   bottom: 0;
   left: 0;
   right: 0;
   overflow: hidden;
   margin: auto;
   animation: circle7 10s linear infinite;
}
@keyframes circle7 {
   0% {
      transform: rotate(225deg) translate(-200px) rotate(-225deg);
   }
   100% {
      transform: rotate(585deg) translate(-200px) rotate(-585deg);
   }
}
.circle8 {
   width: 30px;
   height: 30px;
   position: absolute;
   top: 0;
   bottom: 0;
   left: 0;
   right: 0;
   overflow: hidden;
   margin: auto;
   animation: circle8 10s linear infinite;
}
@keyframes circle8 {
   0% {
      transform: rotate(315deg) translate(-200px) rotate(-315deg);
   }
   100% {
      transform: rotate(675deg) translate(-200px) rotate(-675deg);
   }
}
</style>
