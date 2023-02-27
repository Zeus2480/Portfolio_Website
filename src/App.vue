<template>
   <div class="tw-relative">
      <div class="tw-bg-black tw-w-full tw-h-24 tw-absolute tw-top-0"></div>
      <div app fixed class="black bg-transparent-black tw-z-10 tw-sticky tw-top-0 ">
         <div class="tw-p-3 tw-flex tw-h-full tw-justify-around tw-w-full">
            <div class="tw-flex logo tw-my-auto">
               <div>
                  <img
                     src="./assets/images/profilepicture.jpg"
                     class="tw-rounded-full tw-h-12 tw-w-12"
                     alt=""
                  />
               </div>
               <div class="tw-mx-4">
                  <h1 class="tw-text-white tw-font-semibold tw-text-base">
                     Faizan Siddiqui
                  </h1>
                  <p class="tw-text-white tw-text-sm">Fullstack Developer</p>
               </div>
            </div>
            <div class="tw-my-auto tw-flex">
               <a href="#home-page">
                  <div
                     class="btn pill-shaped-btn tw-font-semibold tw-text-white"
                  >
                     <h2 class="">HOME</h2>
                  </div>
               </a>
               <div
                  @click="downloadResume"
                  class="tw-mx-12 btn tw-font-semibold pill-shaped-btn tw-text-white"
               >
                  <h2 class="">RESUME</h2>
               </div>
               <a href="#contact-me">
                  <div
                     class="btn pill-shaped-btn tw-font-semibold tw-text-white"
                  >
                     <h2 class="">CONTACT</h2>
                  </div>
               </a>
            </div>
         </div>
      </div>
      <v-app>
         <v-main>
            <router-view />
         </v-main>
      </v-app>
   </div>
</template>

<script>
// import axios from "axios";
export default {
   name: "App",

   data: () => ({
      //
   }),
   methods: {
      downloadResume() {
         // Download resume from public folder to user's device
         console.log(process.env.BASE_URL);

         const FILE_URL = "https://faizan.in.net" + "/resume.pdf";

         // Create a temporary anchor element to initiate the download
         const downloadLink = document.createElement("a");
         downloadLink.href = FILE_URL;
         downloadLink.setAttribute("download", "resume.pdf");
         downloadLink.setAttribute("target", "_blank");
         document.body.appendChild(downloadLink);
         downloadLink.click();
         document.body.removeChild(downloadLink);
      },
   },
};
</script>
<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap");
* {
   font-family: "Poppins", sans-serif;
   scroll-behavior: smooth;
}
</style>
<style scoped>
.pill-shaped-btn {
   background-color: transparent;
   border: 2px solid white;
   border-radius: 50px;
   padding: 8px 16px;
}
.pill-shaped-btn:hover {
   background-color: white;
   color: black;
}
.pill-shaped-btn h1:hover {
   color: black;
}
.btn {
   cursor: pointer;
}

.bg-transparent-black {
   /* background-color: rgba(0, 0, 0, .85) !important; */
   /*make background a little transparent*/
    backdrop-filter: blur(5px);
   background-color: rgba(0, 0, 0, 0.5) !important;
}
</style>
