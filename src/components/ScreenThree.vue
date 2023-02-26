<template>
   <div>
      <div
         class="tw-min-h-screen tw-flex tw-items-center tw-w-full tw-relative"
      >
         <img
            src="../assets/images/rocket (1).svg"
            alt=""
            :class="{ 'animate-rocket': animate, 'fly-rocket': flyAnimate }"
         />
      </div>
      <div>
         <div class="next-element">
            <div class="tw-min-h-screen">
               <div>
                  <img
                     :class="{ 'fade-in': slideIn }"
                     class="tw-absolute tw-right-0 tw-top-12"
                     src="../assets/images/Subtract.svg"
                     alt=""
                  />
                  <img
                     :class="{ 'fade-in': slideIn }"
                     class="tw-absolute tw-left-0 tw-bottom-24"
                     src="../assets/images/Subtract (1).svg"
                     alt=""
                  />
               </div>
               <div
                  :class="{ 'fade-in': slideIn }"
                  class="blue-color tw-flex tw-h-full tw-items-center tw-ml-16 tw-rounded-3xl tw-mr-44"
               >
                  <div class="tw-w-1/2">
                     <div class="tw-px-16 tw-h-full">
                        <div class="tw-flex tw-h-full tw-items-center">
                           <div>
                              <img
                                 :class="{ 'fade-in': slideIn }"
                                 src="../assets/images/Group 93.svg"
                                 alt=""
                              />
                              <h1
                                 ref="heading"
                                 class="tw-my-6 tw-text-5xl tw-font-semibold yellow-text-color main-heading"
                                 :class="{
                                    'show-heading': slideIn,
                                    'reverse-heading': !slideIn,
                                 }"
                              >
                                 UI UX Designer
                              </h1>
                              <p
                                 :class="{ 'fade-in': slideIn }"
                                 class="tw-text-xl tw-font-medium sub-text"
                              >
                                 As a UI/UX designer, I create visually
                                 appealing and user-friendly digital experiences
                                 by leveraging my design skills and
                                 understanding of user behavior.
                              </p>
                           </div>
                        </div>
                     </div>
                  </div>
                  <div class="tw-w-1/2">
                     <div class="tw-py-24 tw-w-full">
                        <img
                           v-show="showImage"
                           class="tw-mx-auto ui-svg"
                           :class="{ 'fade-in': slideIn }"
                           src="../assets/images/amico.svg"
                           alt=""
                        />
                     </div>
                  </div>
               </div>
            </div>
         </div>
      </div>
   </div>
</template>

<script>
export default {
   data() {
      return {
         animate: false,
         flyAnimate: false,
         lastScrollPosition: 0,
      };
   },
   created() {
      window.addEventListener("scroll", this.handleScroll);
      setTimeout(() => {
         this.animate = true;
      }, 1000); // Delay for the rocket animation to start
   },
   destroyed() {
      window.removeEventListener("scroll", this.handleScroll);
   },
   methods: {
      handleScroll() {
         const rocket = document.querySelector(".animate-rocket");
         const rocketTop = rocket.getBoundingClientRect().top;
         const windowHeight = window.innerHeight;
         const documentHeight = document.documentElement.scrollHeight;
         const nextElement = document.querySelector(".next-element");
         const nextElementTop = nextElement.getBoundingClientRect().top;
         const animateRocket = rocketTop < windowHeight;

         if (
            animateRocket &&
            window.pageYOffset > this.lastScrollPosition &&
            documentHeight - (window.pageYOffset + windowHeight) > 0
         ) {
            rocket.classList.add("fly-rocket");
            this.reverseAnimate = false;
         } else if (
            window.pageYOffset < this.lastScrollPosition ||
            documentHeight - (window.pageYOffset + windowHeight) <= 0 ||
            nextElementTop < windowHeight
         ) {
            rocket.classList.remove("fly-rocket");
            this.reverseAnimate = true;
         }

         this.lastScrollPosition = window.pageYOffset;
      },
   },
};
</script>

<style scoped>
.blue-color {
   background-color: #f0fcff;
}

.animate-rocket {
   position: absolute;
   bottom: 0;
   left: 50%;
   transform: translate(-50%, -100%);
   transition: transform 1s ease-in-out, width 1s ease-in-out;
   width: 80px;
}

.fly-rocket {
   transform: translate(-50%, -200px);
   transition: transform 2s ease-in-out, width 2s ease-in-out;
   width: 120px;
}

@media only screen and (max-width: 600px) {
   .animate-rocket {
      width: 50px;
   }
   .fly-rocket {
      width: 80px;
   }
}
</style>
