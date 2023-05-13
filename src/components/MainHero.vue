<template>
    <div class="header-hero">
        <img v-if="!mobileScreen" src="@/assets/img/image-web-3-desktop.jpg" alt="hero image" class="hero">
        <img v-else src="@/assets/img/image-web-3-mobile.jpg" alt="hero image" class="hero">
        <h1 class="header-title">The Bright Future fo Web 3.0?</h1>
        <p class="header-text">  
            We dive into the next evolution of the web that claims to put the power of the platforms back into the hands of the people. But is it really fulfilling its promise?

            <button class="button header-hero__button header-hero__button--desktop">Read more</button>
        </p>
        <button class="button header-hero__button header-hero__button--mobile">Read more</button>
    </div>
</template>

<script>
export default {
    name: 'HeaderHero',
    data() {
        return {
            mobileScreen: 768,
        }
    },
    methods: {
        getMobileScreenOnLoad() {
            if(window.innerWidth < 768){
                this.mobileScreen = true;
            } else {
                this.mobileScreen = false;
            }
        },
        getMobileScreenOnResize() {
            window.addEventListener('resize', () => {
                if(window.innerWidth < 768) {
                    this.mobileScreen = true;
                } else {
                    this.mobileScreen = false;
                }
            })
        }
    },

    mounted() {
        this.getMobileScreenOnLoad()
    },
    created() {
        this.getMobileScreenOnResize()
    }

}
</script>

<style>

</style>