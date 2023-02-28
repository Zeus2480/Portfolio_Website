<template>
   <div class="tw-min-h-screen" >
      <div class="screen-1">
         <div class="tw-w-full tw-h-full tw-flex tw-p-6">
            <div class="tw-w-1/2 tw-h-full tw-flex">
               <div class="tw-p-4 tw-pt-0 tw-my-auto tw-ml-8">
                  <div class="tw-flex">
                     <h1 class="tw-text-6xl tw-font-bold">
                        Hello, I'm Faizan
                        <span class="tw-text-blue-400 tw-text-7xl">.</span>
                     </h1>
                  </div>
                  <div>
                     <vue-typer
                        :text="[
                           'a Student',
                           'a UI/UX designer',
                           'a full stack developer',
                        ]"
                        :repeat="Infinity"
                        :shuffle="false"
                        initial-action="typing"
                        :pre-type-delay="70"
                        :type-delay="100"
                        :pre-erase-delay="2000"
                        :erase-delay="100"
                        erase-style="backspace"
                        :erase-on-complete="true"
                        caret-animation="smooth"
                     ></vue-typer>
                  </div>
                 
               </div>
            </div>
            <div class="tw-w-1/2 tw-h-full">
               <img
                  src="../assets/images/Asset 1.svg"
                  class="tw-h-full float-animation"
                  alt=""
               />
            </div>
         </div>
      </div>
      <!-- <div class="tw-min-h-screen screen-2">
         <div class="parallex-effect parallex-effect-animation"></div>
      </div> -->
      <about-me></about-me>
      <tech-stack></tech-stack>
      <contact-me></contact-me>
    <!-- <screen-two></screen-two>
      <screen-three></screen-three> -->
   </div>
</template>
<script>
// import Typewriter from "typewriter-vue";
import { VueTyper } from "vue-typer";
// import ScreenTwo from "../components/ScreenTwo.vue";
// import ScreenThree from "../components/ScreenThree.vue"
import AboutMe from "../components/AboutMe.vue";
import TechStack from "../components/TechStack.vue";
import ContactMe from "../components/ContactMe.vue";
export default {
   components: {
    //   Typewriter,
      VueTyper,
      //   ScreenTwo,
      //   ScreenThree
      AboutMe,
      TechStack,
      ContactMe
   },
   data: () => ({
      replace: [
         { from: "UI/UX designer", to: "Full Stack Developer" },
         { from: "Full Stack Developer", to: "Student" },
         //  { from: "Typewriter React?", to: "Joking, it`s Vue!" },
      ],
   }),
};
</script>
<style>
.vue-typer .custom.char {
   /* color: red !important; */
   font-weight: 600;
   color: rgb(96 165 250);
   font-size: 30px;
   /* background-color: #1e1e1e; */
}
.vue-typer .custom.caret {
  width: 10px;
  background-color: rgb(96 165 250);
  margin-top: -10px;
}
</style>
<style scoped>
.screen-2{
    background-color: #55A67A;
    color: #fff;
}
.vue-typer {
   font-family: monospace;
}

.vue-typer .custom.caret {
   width: 10px;
   background-color: #3f51b5;
}
.about-me {
   font-size: 50px;
   font-weight: 700;
   color: #000;
   text-align: center;
   padding-top: 100px;
}
.screen-1 {
   height: 90vh;
   width: 100%;
   background-color: #000;
   color: #fff;
}

.float-animation {
   animation: float 6s ease-in-out infinite;
}

@keyframes float {
   0% {
      transform: translatey(0px);
   }
   50% {
      transform: translatey(-20px);
   }
   100% {
      transform: translatey(0px);
   }
}
.parallex-effect {
   background-image: url("../assets/images/globe-1849404.png");
   background-attachment: fixed;
   background-position: center;
   background-repeat: no-repeat;
   background-size: cover;
   height: 100vh;
   width: 100%;
}
</style>
