<template>
   <div>
      <div class="rocketAnimation">
         <!-- <img src="../assets/images/rocket (1).svg" alt=""> -->
         <div class="draw-container">
            <div class="tw-w-1/2">
               <h1 class="tw-text-white tw-font-semibold tw-text-6xl">
                  Launch your dreams to the stars
               </h1>
               <blockquote>
                  <p class="tw-text-white tw-font-semibold tw-text-xl">
                     "a portfolio for the stars by the rocket of your ambition"
                  </p>
               </blockquote>
            </div>
            <div class="draw tw-w-1/2">
               <!-- Rocket -->
               <div class="rocket">
                  <div class="window"></div>
               </div>

               <!-- Smoke -->
               <div class="smoke">
                  <div class="one"></div>
                  <div class="two"></div>
               </div>

               <!-- Stars -->
               <div class="stars">
                  <div class="star one"></div>
                  <div class="star two small"></div>
                  <div class="star three small"></div>
                  <div class="star four small"></div>
                  <div class="star five"></div>
                  <div class="star six samll"></div>
                  <div class="star seven"></div>
                  <div class="star eight small"></div>
               </div>
            </div>
         </div>
      </div>
      <div class="firstScreen tw-py-24 tw-pr-40 tw-pl-20 tw-relative">
         <img
            src="../assets/images/uiRIghtCIrcle.svg"
            class="tw-absolute tw-top-12 tw-right-0"
            alt=""
         />
         <img
            src="../assets/images/uiLeftCIrcle.svg"
            class="tw-absolute tw-bottom-24 tw-left-0"
            alt=""
         />
         <div class="cumston-Blue tw-shadow-sm	 tw-rounded-2xl tw-flex tw-h-full tw-p-14">
            <div class="tw-w-1/2 tw-flex tw-items-center">
               <div>
                  <img src="../assets/images/uiHeadingLogo.svg" alt="" />
                  <h1
                     class="tw-my-8 tw-text-5xl tw-font-semibold yellow-text-color main-heading"
                  >
                     UI UX Designer
                  </h1>
                  <p class="tw-text-xl tw-font-medium sub-text">
                     As a UI/UX designer, I create visually appealing and
                     user-friendly digital experiences by leveraging my design
                     skills and understanding of user behavior.
                  </p>
               </div>
            </div>
            <div class="tw-w-1/2 tw-flex tw-justify-center tw-items-center">
               <img src="../assets/images/uiIllustration.svg" alt="" />
            </div>
         </div>
      </div>
      <div class="firstScreen tw-py-24 tw-pr-20 tw-pl-40 tw-relative">
         <img
            src="../assets/images/SmallerCircle.svg"
            class="tw-absolute tw-bottom-24 tw--right-4"
            alt=""
         />
         <img
            src="../assets/images/BiggerCircle.svg"
            class="tw-absolute tw-top-12 tw--left-16"
            alt=""
         />
         <div class="cumston-Green tw-shadow-sm tw-rounded-2xl tw-flex tw-h-full tw-p-14">
            <div class="tw-w-1/2 tw-flex tw-justify-center tw-items-center">
               <img
                  src="../assets/images/WebDeveloperIllustration.svg"
                  alt=""
               />
            </div>
            <div class="tw-w-1/2 tw-flex tw-items-center">
               <div>
                  <img src="../assets/images/WebDeveloperLogo.svg" alt="" />
                  <h1
                     class="tw-my-8 tw-text-5xl tw-font-semibold green-text-color main-heading"
                  >
                     Web Developer
                  </h1>
                  <p class="tw-text-xl tw-font-medium sub-text">
                     I'm a web developer with skills in front-end and back-end
                     development technologies. I specialize in HTML, CSS,
                     JavaScript, and responsive design, and I'm committed to
                     creating functional and engaging websites.
                  </p>
               </div>
            </div>
         </div>
      </div>
   </div>
</template>
<script>
export default {};
</script>
<style scoped>
.firstScreen {
   height: 100vh;
}
.cumston-Blue {
   background-color: #f0fcff;
}
.yellow-text-color {
   color: #f9b233;
}
.cumston-Green {
   background-color: #eaf9f8;
}
.green-text-color {
   color: #20c3c5;
}

* {
   margin: 0;
   padding: 0;
   box-sizing: border-box;
}

.draw-container {
   height: 100vh;
   /* width: 100vw; */
   overflow: hidden;
   display: flex;
   align-items: center;
   justify-content: center;
   background-image: linear-gradient(
      to bottom,
      #b4b2b3,
      #b4b2b3 70%,
      #b4b2b3 71%,
      #fff
   );
   /* background-color: #222; */
}

.draw-container .draw {
   height: 600px;
   width: 450px;
   position: relative;
}

/* Rocket */
.draw-container .rocket {
   position: absolute;
   height: 180px;
   width: 80px;
   top: 80px;
   left: 50%;
   transform: translateX(-50%);
   border-radius: 50% 50% 25% 25% / 50% 50% 40% 40%;
   background-color: #dadada;
   box-shadow: 0 -3px 0 #fff;
   transform-style: preserve-3d;
   z-index: 2;
   animation: animateRocket 1s linear alternate infinite;
}
.draw-container .rocket::before,
.draw-container .rocket:after {
   content: "";
   position: absolute;
   left: 50%;
   transform: translateX(-50%);
}
.draw-container .rocket::before {
   width: 55%;
   height: 10px;
   background-color: #d43e07;
   bottom: -10px;
   border-radius: 0% 0% 25% 25% / 50% 50% 40% 40%;
}
.draw-container .rocket:after {
   height: 55px;
   width: 155%;
   background-color: #9e554f;
   bottom: 0;
   z-index: -10;
   transform: translateX(-50%) translateZ(-1px);
   border-radius: 50% 50% 10% 10% / 90% 90% 20% 20%;
}
.draw-container .rocket .window {
   position: absolute;
   height: 30px;
   width: 30px;
   top: 40px;
   left: 50%;
   transform: translateX(-50%);
   border-radius: 50%;
   background-color: #9e554f;
   box-sizing: initial;
   border: 5px solid #adadad;
}

@keyframes animateRocket {
   to {
      transform: translateX(-50%) translateY(3px);
   }
}

/* Smoke */
.draw-container .smoke {
   height: 200px;
   width: 32px;
   top: 260px;
   left: 50%;
   transform: translateX(-50%);
   position: absolute;
   z-index: 1;
   background-image: linear-gradient(
      to bottom,
      rgba(255, 255, 255, 0.1),
      rgba(255, 255, 255, 0.9)
   );
}
.draw-container .smoke > div {
   position: absolute;
   border-radius: 50%;
}
.draw-container .smoke .one {
   height: 200px;
   width: 200px;
   background-color: rgba(255, 255, 255, 0.4);
   top: 80px;
   left: -180px;
   box-shadow: -50px 80px 0 -30px rgba(255, 255, 255, 0.4),
      160px 80px 0 0px rgba(255, 255, 255, 0.4),
      290px 80px 0 -50px rgba(255, 255, 255, 0.4);
   animation: animateSmoke 3s linear alternate infinite;
   opacity: 0.9;
}
.draw-container .smoke .two {
   height: 210px;
   width: 210px;
   top: 120px;
   left: -90px;
   background-color: rgba(255, 255, 255, 1);
   box-shadow: -90px 0px 0 -40px rgba(255, 255, 255, 1),
      90px 60px 0 -80px rgba(255, 255, 255, 1),
      80px -40px 0 -50px rgba(255, 255, 255, 1);
   animation: animateSmoke 1s linear alternate-reverse infinite;
   opacity: 1;
}

@keyframes animateSmoke {
   to {
      opacity: 1;
      transform: scale(0.98) translate(1px);
   }
}

/* Stars */
.draw-container .stars {
   top: 150px;
}
.draw-container .stars .star,
.draw-container .stars .star:before {
   position: absolute;
   background-color: #fff;
   border-radius: 50% 50% 50% 50% / 50% 50% 50% 50%;
   box-shadow: 0 0 7px rgba(255, 255, 255, 0.5);
}
.draw-container .stars .star {
   height: 15px;
   width: 2px;
}
.draw-container .stars .star:before {
   content: "";
   width: 100%;
   height: 100%;
   position: absolute;
   top: 0;
   left: 0;
   transform: rotate(90deg);
}
.draw-container .stars .star.small {
   height: 10px;
   width: 1px;
}
.draw-container .stars .star.one {
   top: 10%;
   left: 10%;
}
.draw-container .stars .star.two {
   top: 40%;
   height: 10px;
}
.draw-container .stars .star.three {
   top: 50%;
   left: 50%;
}
.draw-container .stars .star.four {
   top: 57%;
   left: 70%;
}
.draw-container .stars .star.five {
   top: 25%;
   left: 70%;
}
.draw-container .stars .star.six {
   top: 15%;
   left: 110%;
}
.draw-container .stars .star.seven {
   top: 60%;
   left: 120%;
}
.draw-container .stars .star.eight {
   top: 75%;
   left: -10%;
}
.draw-container .stars .star {
   position: absolute;
   border-radius: 50%;
   background-color: #fff;
}

.draw-container .stars .one {
   height: 3px;
   width: 3px;
   top: 70px;
   left: 110px;
   animation: animateStarOne 1.5s ease-in-out alternate infinite;
}

.draw-container .stars .two {
   height: 2px;
   width: 2px;
   top: 180px;
   left: 260px;
   animation: animateStarTwo 1.5s ease-in-out alternate infinite;
}

.draw-container .stars .three {
   height: 2px;
   width: 2px;
   top: 380px;
   left: 380px;
   animation: animateStarThree 1.5s ease-in-out alternate infinite;
}

.draw-container .stars .four {
   height: 2px;
   width: 2px;
   top: 280px;
   left: 180px;
   animation: animateStarFour 1.5s ease-in-out alternate infinite;
}

.draw-container .stars .five {
   height: 4px;
   width: 4px;
   top: 150px;
   left: 60px;
   animation: animateStarFive 1.5s ease-in-out alternate infinite;
}

.draw-container .stars .six {
   height: 2px;
   width: 2px;
   top: 260px;
   left: 60px;
   animation: animateStarSix 1.5s ease-in-out alternate infinite;
}

.draw-container .stars .seven {
   height: 4px;
   width: 4px;
   top: 340px;
   left: 260px;
   animation: animateStarSeven 1.5s ease-in-out alternate infinite;
}

.draw-container .stars .eight {
   height: 2px;
   width: 2px;
   top: 420px;
   left: 180px;
   animation: animateStarEight 1.5s ease-in-out alternate infinite;
}

@keyframes animateStarOne {
   to {
      transform: translate(-10px, -10px);
   }
}

@keyframes animateStarTwo {
   to {
      transform: translate(10px, 10px);
   }
}

@keyframes animateStarThree {
   to {
      transform: translate(-10px, 10px);
   }
}

@keyframes animateStarFour {
   to {
      transform: translate(10px, -10px);
   }
}

@keyframes animateStarFive {
   to {
      transform: translate(-5px, -5px);
   }
}

@keyframes animateStarSix {
   to {
      transform: translate(5px, -5px);
   }
}

@keyframes animateStarSeven {
   to {
      transform: translate(-5px, 5px);
   }
}

@keyframes animateStarEight {
   to {
      transform: translate(5px, 5px);
   }
}
</style>
