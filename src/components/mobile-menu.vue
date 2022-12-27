<script setup>
import {ref} from 'vue'

const props = defineProps({
    openMenu: {
        type: Boolean,
        required: true,
        default: false,
    }
})

</script>

<template>
     <div :class="['displayNone', {mobileMenu: openMenu}]">
            <h3 class="text-hovered">Who we are</h3>
            <h3 class="text-hovered">What we do</h3>
            <h3 class="text-hovered">Travel with us</h3>
            <h3 class="text-hovered">Contact us</h3>
    </div>
</template>

<style scoped lang="scss">
.displayNone {
    position: absolute;
    top: 100%;
    right: 0;
    width: 40%;
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: #5372fdb1;
    color: white;
    font-family: Aleo;
    font-weight: 400;
    font-size: 14px;
    line-height: 20px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    padding: 10px;
    transform: translateX(100%);   
    transition: 1s;
    z-index: 1;

    & > h3 {
        padding: 10px;
    }
}

.mobileMenu {
    transform: translateX(0px);
}

</style>