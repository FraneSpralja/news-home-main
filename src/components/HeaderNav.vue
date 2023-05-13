<template>
    <div class="nav-menu">
        <img src="@/assets/img/logo.svg" alt="logo" class="logo">

        <div class="overlay">
            <!--  -->
        </div>
        <div class="btn-bg">
            <div @click="btnToggleMenu" class="nav-menu__btn">
                <!--  -->
            </div>
        </div>

        <ul class="nav-menu__list">
            <li class="nav-menu__item">
                <a href="#" class="menu-link">Home</a>
            </li>
            <li class="nav-menu__item">
                <a href="#" class="menu-link">New</a>
            </li>
            <li class="nav-menu__item">
                <a href="#" class="menu-link">Popular</a>
            </li>
            <li class="nav-menu__item">
                <a href="#" class="menu-link">Trending</a>
            </li>
            <li class="nav-menu__item">
                <a href="#" class="menu-link">Categories</a>
            </li>
        </ul>
    </div>
</template>

<script>

export default {
    name: 'HeaderNav',

    data() {
        return {

        }
    },

    methods: {
        btnToggleMenu(e) {
            let btn = e.target;

            btn.classList.toggle('active');
            
            btn.parentElement.nextElementSibling.classList.toggle('active')

            btn.parentElement.previousElementSibling.classList.toggle('active')
        }
    }
}

</script>

<style>

</style>