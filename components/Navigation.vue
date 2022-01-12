<template>
  <div>
      <nav class="w-full top-0 left-0 lg:absolute">
          <div class="nav-container py-6 xl:py-8 px-5 xl:px-14 flex justify-between items-center">
              <div class="left-container">
                  <nuxt-link to="/" class="logo space-x-3 xl:space-x-5 flex justify-center items-center">
                      <img class="w-10 xl:w-12" src="/svg/logo.svg" alt="Logo">

                      <div class="text xl:text-lg text-white font-medium">
                          Hostel
                      </div>
                  </nuxt-link>
              </div>

              <div class="right-container flex justify-center items-center space-x-3 xl:space-x-5">
                  <div class="avatar">
                      <img class="w-10 xl:w-12" src="/images/Avatar.png" alt="">
                  </div>

                <button class="register-btn px-6 lg:px-8 py-2 xl:py-3 text-white text-xs font-normal bg-[#03A86B] rounded-lg xl:rounded-xl">
                    Help
                </button>
              </div>
          </div>
      </nav>
  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>