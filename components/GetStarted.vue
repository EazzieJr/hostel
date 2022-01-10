<template>
  <div>
      <section class="splash w-screen h-screen flex justify-center items-center text-center bg-center bg-cover bg-no-repeat" style="background-image: url(/images/Splash-bg.png);">
        <div class="splash-container flex flex-col justify-center items-center text-center space-y-5">
            <img class="w-24" src="/svg/logo.svg" alt="">

            <p class="hostel text-4xl font-bold font-mono text-white text-center">
                Hostels
            </p>

            <nuxt-link to="/register" class="text-sm text-[#03A86B] hover:text-white font-medium py-2.5 px-7 bg-white hover:bg-[#03A86B] transition duration-700 rounded-full">
                Get started
            </nuxt-link>
        </div>
      </section>
  </div>
</template>

<script>
export default {
    name: 'GetStarted'
}
</script>

<style>
/* font-leckerli {
  font-family: 'Leckerli One', cursive;
} */
</style>