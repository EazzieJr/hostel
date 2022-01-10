<template>
    <section class="login flex justify-center">
        <div class="login-container w-screen h-screen flex flex-col justify-center items-center bg-center bg-cover bg-no-repeat space-y-5" style="background-image: url(/images/Splash-bg.png);">
            <form class="w-80 px-8 py-8 bg-white rounded-3xl shadow-xl" action="">
                <h2 class="header font-sans font-bold text-[#2D3748] text-left text-xl">
                    Register With
                </h2>

                <div class="social-medias-container flex space-x-5 mt-5">
                    <button class="social-media p-4 border rounded-xl" v-for="socialCard in socialCards" :key="socialCard">
                        <img class="w-5" :src="socialCard.image" alt="Facebook">
                    </button>
                </div>

                <p class="or text-base text-[#A0AEC0] font-bold my-7">
                    or
                </p>

                <div class="details space-y-5">
                    <div v-for="input in inputs" :key="input">
                            <p class="id text-left text-xs text-[#52575C] font-medium mb-2 ml-1">
                                {{ input.name }}
                            </p>
                        
                            <input class="input w-full text-xs text-[#52575C] p-3 border rounded-2xl flex justify-between items-center" type="text" :placeholder="input.placeHolder" />
                    </div>
                </div>

                <div class="remember-me my-5 flex items-center space-x-3">
                    <div class="remember-me-button w-10 p-[3px] bg-gray-300 rounded-full focus:outline-none transition duration-500" @click="toggle">
                        <div class="control w-4 h-4 rounded-full bg-white transition duration-500"></div>
                    </div>

                    <p class="remember-me text-xs font-medium" @click="toggle">
                        Remember me
                    </p>
                </div>

                <button class="register-btn px-7 py-2.5 text-white text-xs font-medium bg-[#03A86B] rounded-lg">
                    Register
                </button>

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
    remembered: false,
    
    data() {
        return {
            inputs: [
                {
                    name: 'Name',
                    placeHolder: 'Your full name',
                    type: 'text'
                },

                {
                    name: 'Email',
                    placeHolder: 'Your email address',
                    type: 'email'
                },
            
                {
                    name: 'Password',
                    placeHolder: 'Your password',
                    type: 'password'
                },
            ],

            socialCards: [
                {
                    image: './svg/facebook.svg'
                },

                {
                    image: './svg/apple.svg'
                },

                {
                    image: './svg/google.svg'
                },
            ]
        }
    },

    methods: {
        toggle() {
            const control = document.querySelector('.control')
            const rememberBtn = document.querySelector('.remember-me-button')

            if(!this.remembered) {
                control.classList.add('move')
                rememberBtn.classList.add('invert-color')
                console.log('clickedIN')
                this.remembered = true
            } else {
                control.classList.remove('move')
                rememberBtn.classList.remove('invert-color')
                console.log('clickedOUT')
                this.remembered = false
            }
        }
    }
}
</script>

<style>
.move {
    transition: 0.5s ease-in-out;
    transform: translateX(18px);
}

.invert-color {
    transition: 0.5s ease-in-out;
    background-color: #03A86B;
}
</style>