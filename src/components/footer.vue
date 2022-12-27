<script setup>
import Facebook from '@/assets/socials/facebook.vue'
import Twitter from '@/assets/socials/twitter.vue'
import LinkedIn from '@/assets/socials/linkedIn.vue'
import Youtube from '@/assets/socials/youtube.vue'
import Pinterest from '@/assets/socials/pinterest.vue'

</script>

<template>
    <div class="wrapper">
        <h2>Bhromaon</h2>
        <h4>Safe Travel Anywhere</h4>
        <div class="socials-container">
            <Facebook/>
            <Twitter/>
            <LinkedIn/>
            <Youtube/>
            <Pinterest/>
        </div>
    </div>
</template>

<style scoped lang="scss">
.wrapper {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    gap: 20px;
    padding: 60px;
    color: white;
    font-family: JosefinSans;
    background-color: black;
}

.socials-container {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    gap: 20px;
    align-items: center;
}

h2 {
    font-size: 24px;
    line-height: 28px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
}

h4 {
    font-weight: 400;
    font-size: 14px;
    line-height: 20px;
    letter-spacing: 0.2em;
}
</style>