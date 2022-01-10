<template>
    <section class="login flex justify-center">
        <div class="login-container w-screen h-screen flex flex-col justify-center items-center bg-center bg-cover bg-no-repeat space-y-5" style="background-image: url(/images/Splash-bg.png);">
            <form class="w-80 px-8 py-8 bg-white rounded-3xl shadow-xl" action="">
                <h2 class="header font-sans font-bold text-[#2D3748] text-left text-xl">
                    Choose account type
                </h2>

                <div class="account-types space-y-5 mt-7">
                    <div v-for="accountType in accountTypes" :key="accountType">
                        <div class="w-full input-for-account-type p-3 border rounded-2xl flex justify-between items-center">
                            <p class="input-name text-sm text-[#52575C]">
                                {{ accountType.name }}
                            </p>

                            <input type="radio" name="decision" id="radio">
                        </div>
                    </div>
                </div>

                <div class="already-have-an-account mt-5">
                    <p class="text-xs text-[#A0AEC0]">
                        Already have an account? <nuxt-link to="/login" class="text-[#03A86B] font-medium">Login</nuxt-link>
                    </p>
                </div>
            </form>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            accountTypes: [
                {
                    name: 'Student'
                },

                {
                    name: 'House Owner'
                },
                
                {
                    name: 'Admin'
                },
            ]
        }
    }
}
</script>

<style></style>
