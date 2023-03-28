<template>
  <div class="min-h-screen font-sans antialiased relative">
    <div class="relative">
      <!-- w-full h-[125vh] sm:h-[225vh] lg:h-[125vh] -->
      <div class="absolute top-0 left-0"></div>
      <BaseNavbar class="" />
      <main class="text-neutral-800">
        <Nuxt />
      </main>

      <BaseFooter />
    </div>
  </div>
</template>
<script>
export default {
  name: 'DefaultLayout',
}
</script>

<style>
.cover-gradient {
  background: linear-gradient(
    169.4deg,
    rgba(57, 132, 244, 0.04) -6.01%,
    rgba(12, 211, 255, 0.04) 36.87%,
    rgba(47, 124, 240, 0.04) 78.04%,
    rgba(14, 101, 232, 0.04) 103.77%
  );
}
.cover-gradient-2 {
  background: linear-gradient(
    169.4deg,
    rgba(57, 132, 244, 0.1) -6.01%,
    rgba(12, 211, 255, 0.1) 36.87%,
    rgba(47, 124, 240, 0.1) 78.04%,
    rgba(14, 101, 232, 0.1) 103.77%
  );
}
.bg-blue-gradient,
.text-gradient {
  background: linear-gradient(136.91deg, #468ef9 -12.5%, #0c66ee 107.5%);
}
.text-gradient {
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.slide-enter-active {
  -moz-transition-duration: 0.3s;
  -webkit-transition-duration: 0.3s;
  -o-transition-duration: 0.3s;
  transition-duration: 0.3s;
  -moz-transition-timing-function: ease-in;
  -webkit-transition-timing-function: ease-in;
  -o-transition-timing-function: ease-in;
  transition-timing-function: ease-in;
}

.slide-leave-active {
  -moz-transition-duration: 0.3s;
  -webkit-transition-duration: 0.3s;
  -o-transition-duration: 0.3s;
  transition-duration: 0.3s;
  -moz-transition-timing-function: cubic-bezier(0, 1, 0.5, 1);
  -webkit-transition-timing-function: cubic-bezier(0, 1, 0.5, 1);
  -o-transition-timing-function: cubic-bezier(0, 1, 0.5, 1);
  transition-timing-function: cubic-bezier(0, 1, 0.5, 1);
}

.slide-enter-to,
.slide-leave {
  max-height: 100px;
  overflow: hidden;
}

.slide-enter,
.slide-leave-to {
  overflow: hidden;
  max-height: 0;
}
</style>
<style>
/* @import url('https://fonts.googleapis.com/css2?family=Delicious+Handrawn&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300&display=swap'); */
/* @import url('https://fonts.googleapis.com/css2?family=Kalam:wght@300&display=swap'); */
@import url('https://fonts.googleapis.com/css2?family=Nunito:wght@200&display=swap');
* {
    /* font-family: 'Delicious Handrawn', cursive; */
    /* font-family: 'Roboto', sans-serif; */
    /* font-family: 'Kalam', cursive; */
    /* font-family: "ZicletsW00"; src: url("//db.onlinewebfonts.com/t/2b948f6f0fb8790323463c31bfb0e87f.eot");
     */
     /*  */
     font-family: 'Nunito', sans-serif;
}
</style>
