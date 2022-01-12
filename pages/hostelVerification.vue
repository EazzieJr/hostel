<template>
  <div>
    <section class="login flex justify-center md:min-h-screen bg-[#F8F9FA]">
      <div
        class="login-container w-screen lg:w-[45%] bg-center bg-cover bg-no-repeat lg:flex flex-col justify-center items-center space-y-5"
        style="background-image: url(/images/Splash-bg.png)"
      >
        <Navigation />
        <div class="info py-10 space-y-4">
          <h1
            class="text-4xl lg:text-5xl font-semibold text-center lg:text-left text-white leading-tight xl:leading-snug px-10 lg:px-16 xl:px-20"
          >
            We need to verify your hostel.
          </h1>

          <div
            class="deats text-white font-semibold text-center lg:text-left px-10 lg:px-16 xl:px-20 xl:pr-28"
          >
            Kindly provide the necessary details in time to complete the
            verification.
          </div>
        </div>

        <div class="form lg:hidden flex justify-center items-center">
          <form
            class="w-80 lg:w-[400px] sm:w-96 px-8 py-8 bg-white rounded-2xl shadow-xl"
            action=""
          >
            <h2
              class="header font-sans font-bold text-[#2D3748] text-left text-xl lg:text-lg"
            >
              Upload Documents
            </h2>

            <div class="id mt-7 space-y-5">
              <div
                v-for="id in ids"
                :key="id.id"
                class="flex justify-between items-center"
              >
                <div class="left-container">
                  <p class="id-type text-sm font-medium">
                    {{ id.name }}
                  </p>
                </div>

                <div class="right-container">
                  <nuxt-link
                    to="/#"
                    class="flex justify-between items-center space-x-2"
                  >
                    <p class="upload-media text-xs text-[#03A86B] font-medium">
                      Upload Media
                    </p>

                    <img src="/svg/arrow.svg" alt="" />
                  </nuxt-link>
                </div>
              </div>
            </div>

            <div class="continue mt-7">
              <nuxt-link
                to="/hostelVerification"
                class="px-7 py-2.5 text-white text-xs font-medium bg-[#03A86B] rounded-lg"
              >
                Continue
              </nuxt-link>
            </div>
          </form>
        </div>
      </div>

      <div
        class="right-container lg:w-[55%] hidden lg:flex justify-center items-center"
      >
        <div class="form hidden lg:flex justify-center items-center">
          <form
            class="w-80 lg:w-[400px] sm:w-96 px-8 py-8 bg-white rounded-2xl shadow-xl"
            action=""
          >
            <h2
              class="header font-sans font-bold text-[#2D3748] text-left text-xl lg:text-lg"
            >
              Upload Documents
            </h2>

            <div class="id mt-7 space-y-5">
              <div
                v-for="id in ids"
                :key="id.id"
                class="flex justify-between items-center"
              >
                <div class="left-container">
                  <p class="id-type text-sm font-medium">
                    {{ id.name }}
                  </p>
                </div>

                <div class="right-container">
                  <nuxt-link
                    to="/#"
                    class="flex justify-between items-center space-x-2"
                  >
                    <p class="upload-media text-xs text-[#03A86B] font-medium">
                      Upload Media
                    </p>

                    <img src="/svg/arrow.svg" alt="" />
                  </nuxt-link>
                </div>
              </div>
            </div>

            <div class="continue mt-7">
              <nuxt-link
                to="/hostelVerification"
                class="px-7 py-2.5 text-white text-xs font-medium bg-[#03A86B] rounded-lg"
              >
                Continue
              </nuxt-link>
            </div>
          </form>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      ids: [
        {
          name: 'National ID',
        },

        {
          name: 'Drivers Licence',
        },

        {
          name: 'Passport',
        },

        {
          name: 'Proof of Ownership',
        },
      ],
    }
  },
}
</script>

<style></style>
