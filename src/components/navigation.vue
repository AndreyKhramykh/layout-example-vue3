<script setup>
import {ref} from 'vue';
import MobileMenu from '@/components/mobile-menu.vue'
let buttonIsActive = ref(false);

let hasMenuButton = ref(false);

let mobileMenu = ref(false);

let showMobileMenu = () => {
    buttonIsActive.value = !buttonIsActive.value;
    mobileMenu.value = !mobileMenu.value
}

if (window.innerWidth < 769) {
    hasMenuButton.value = !hasMenuButton.value
}

</script>

<template>
    <div id="BHROMAON" class="nav__container">
        <div class="h2">Bhromaon</div>
        <div v-if="!hasMenuButton" class="nav__h3-container">
            <h3 class="text-hovered">Who we are</h3>
            <h3 class="text-hovered">What we do</h3>
            <h3 class="text-hovered">Travel with us</h3>
            <h3 class="text-hovered">Contact us</h3>
        </div>
        <div v-else @click="showMobileMenu" :class="['menu-button', {active: buttonIsActive}]">
            <span></span>
            <span></span>
            <span></span>
        </div>
        <MobileMenu :openMenu="mobileMenu"/>
    </div>
  
</template>
<style scoped lang="scss">

@import url(@/assets/styles/menu-button.scss);

.nav {
    &__container {
        position: relative;
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        background-color: #5373FD;
        color: white;
        font-family: JosefinSans;
        padding: 30px;

        .h2 {
            font-weight: 700;
            font-size: 24px;
            line-height: 28px;
            letter-spacing: 0.1em;
            text-transform: uppercase;
        }
    }

    &__h3-container {
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        gap: 30px;
        font-family: Aleo;
        font-weight: 400;
        font-size: 14px;
        line-height: 20px;
        letter-spacing: 0.1em;
        text-transform: uppercase;
    }
}


@media screen and (max-width: 1024px) {
    .nav__container {
        flex-direction: column;
    }

    .h2 {
        text-align: center;
        margin-bottom: 20px;
    }
}
@media screen and (max-width: 768px) {
    .nav__container {
        flex-direction: row;
        justify-content: space-between;
    }
    .h2 {
        margin-bottom: 0;
    }
}

</style>