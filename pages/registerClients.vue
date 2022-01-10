<template>
    <section class="login flex justify-center">
        <div class="login-container w-screen h-screen flex flex-col justify-center items-center bg-center bg-cover bg-no-repeat space-y-5" style="background-image: url(/images/Splash-bg.png);">
            <form class="w-80 px-8 py-8 bg-white rounded-3xl shadow-xl" action="">
                <h2 class="header font-sans font-bold text-[#2D3748] text-left text-xl">
                    Create new listing
                </h2>

                <div class="details space-y-5 mt-8">
                    <div class="flex items-center space-x-3" v-for="listing in listings" :key="listing">
                        <img class="" src="/svg/check.svg" alt="">
                        
                        <p class="id text-left text-xs text-[#52575C] font-medium ml-1">
                            {{ listing.listItem }}
                        </p>
                    </div>
                </div>
                
                <div class="terms mt-7">
                    <p class="text-xs text-[#A0AEC0]">
                        By continuing, you agree to let Booking.com email you regarding your property registration.
                    </p>
                </div>

                <button class="register-btn px-7 py-2.5 mt-5 text-white text-xs font-medium bg-[#03A86B] rounded-lg">
                    Get Started
                </button>
            </form>
        </div>
    </section>
</template>

<script>
export default {
    layout: 'clientRegistration',

    data() {
        return {
            listings: [
                {
                    listItem: 'Listing is totally free'
                },

                {
                    listItem: '24/7 costomer support'
                },

                {
                    listItem: 'Set rules on property'
                }
            ]
        }
    }
}
</script>

<style>

</style>