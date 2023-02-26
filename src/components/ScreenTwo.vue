<template>
   <div>
      <div
         class="tw-min-h-screen tw-flex tw-items-center tw-w-full tw-relative"
      >
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
                              'reverse-heading': !slideIn
                           }"
                        >
                           UI UX Designer
                        </h1>
                        <p
                           :class="{ 'fade-in': slideIn }"
                           class="tw-text-xl tw-font-medium sub-text"
                        >
                           As a UI/UX designer, I create visually appealing and
                           user-friendly digital experiences by leveraging my
                           design skills and understanding of user behavior.
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
</template>

<script>
export default {
   data() {
      return {
         showImage: false,
         slideIn: false,
         lastScrollPosition: 0,
      };
   },
   created() {
      window.addEventListener("scroll", this.handleScroll);
   },
   destroyed() {
      window.removeEventListener("scroll", this.handleScroll);
   },
   methods: {
      // handleScroll() {
      //    const heading = this.$refs.heading;
      //    const headingTop = heading.getBoundingClientRect().top;
      //    const windowHeight = window.innerHeight;
      //    const slideIn = headingTop < windowHeight / 1.1;
      //    this.slideIn = slideIn && window.pageYOffset > this.lastScrollPosition;
      //    this.showImage = slideIn;
      //    this.lastScrollPosition = window.pageYOffset;
      // },
      handleScroll() {
         const heading = this.$refs.heading;
         const headingTop = heading.getBoundingClientRect().top;
         const windowHeight = window.innerHeight;
         const slideIn = headingTop < windowHeight / 1.1;

         if (slideIn && window.pageYOffset > this.lastScrollPosition) {
            // User is scrolling down, show the image and slide in the heading
            this.slideIn = true;
            this.showImage = true;
            this.lastScrollPosition = window.pageYOffset;
         } else if (window.pageYOffset < this.lastScrollPosition) {
            // User is scrolling up, hide the image and slide out the heading
            this.slideIn = false;
            this.showImage = false;
            this.lastScrollPosition = window.pageYOffset;
         }
      },
   },
};
</script>

<style scoped>
.blue-color {
   background-color: #f0fcff;
}
.yellow-text-color {
   color: #ffc107;
}

.main-heading {
   transform: translateX(100%);
   transition: transform 1s ease-in-out;
}

.reverse-heading {
   transform: translateX(-101%);
}
.show-heading {
   transform: translateX(0%);
}
.ui-svg,
.sub-text {
   opacity: 0;
   transition: opacity 0.5s ease-in-out;
}

.ui-svg.fade-in,
.sub-text.fade-in {
   opacity: 1;
}
div img,
.sub-text {
   opacity: 0;
   transition: opacity 0.5s ease-in-out;
}

div img.fade-in,
.sub-text.fade-in {
   opacity: 1;
}
div img {
   opacity: 0;
   transition: opacity 0.5s ease-in-out;
}

div img.fade-in {
   opacity: 1;
}

</style>
