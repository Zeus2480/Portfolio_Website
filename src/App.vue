<template>
   <div>
      <div app fixed class=" tw-bg-black tw-top-0 tw-z-10 " >
         <div
            class=" tw-p-3 tw-flex tw-h-full tw-justify-around tw-w-full"
         >
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
               <div><h2 class="tw-font-semibold pill-shaped-btn tw-text-white">HOME</h2></div>
               <div class="tw-mx-12 tw-font-semibold tw-text-white">
                  <h2 class="pill-shaped-btn">RESUME</h2>
               </div>
               <div>
                  <h2 class="tw-font-semibold pill-shaped-btn tw-text-white">CONTACT</h2>
               </div>
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
export default {
   name: "App",

   data: () => ({
      //
   }),
};
</script>
<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap");
* {
   font-family: "Poppins", sans-serif;
}
</style>
<style scoped>

.pill-shaped-btn{
    background-color: transparent;
    border: 2px solid white;
    border-radius: 50px;
    padding: 8px 16px;
}
   
.bg-transparent-black {
   /* background-color: rgba(0, 0, 0, .75) !important; */
   /*make background a little transparent*/
   background-color: rgba(0, 0, 0, 0.5) !important;
}
</style>
