<script setup>
import Quotes from '@/assets/icons/quotes.vue'
</script>

<template>
    <div class="wrapper">
        <h1>
            What Our  Tourists Say
        </h1>
        <div class="content">
            <div class="content__txt">
                <h2>
                    Sam Sumon
                </h2>
                <div class="txt-wrapper">
                    <div class="quotes"><Quotes/></div>
                    <p>
                        But I must explain to you how all this mistaken idea of account to denouncinpleasure and praising pain  But I must explain to you how all this mistaken idea of account to nai denouncing pleasure and praising pain was account  born and I account will give you a complete account of the system was account  born and I account will give you a nai the complete account of the system.
                    </p>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
.wrapper {
    background-image: url(@/assets/backgrounds/image4.png);
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    color: white;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    gap: 20px;
    padding: 4% 16%;
}

h1 {
    font-family: 'Aleo';
    font-weight: 400;
    font-size: 36px;
    line-height: 40px;
    text-transform: capitalize;
}

h2 {
    font-weight: 400;
    font-size: 20px;
    line-height: 28px;
    text-transform: uppercase;
}

p {
    text-indent: 30px;
    font-weight: 300;
    font-size: 16px;
    line-height: 28px;
    letter-spacing: 0.1em;
}

.content {
    display: flex;
    flex-direction: row;
    font-family: JosefinSans;

    &__txt {
        display: flex;
        flex-direction: column;
        justify-content: center;
        gap: 20px;
        background-image: url(@/assets/img/img1.png);
        background-position: left;
        background-size: 30% 100%;
        background-repeat: no-repeat;
        background-color: #333333;
        padding: 30px 30px 30px calc(30% + 30px);
        height: 100%;
    }
}

.txt-wrapper {
    position: relative;
}

.quotes {
    position: absolute;
}

img {
    width: 440px;
    height: 100%;
}

@media screen and (max-width: 1360px) {
    .wrapper {
        padding: 8% 10%;
    }
}
@media screen and (max-width: 768px) {
    .content__txt {
        background-position: top;
        background-size: 100% 50%;
        padding: calc(50% + 10px) 20px 20px 20px;
    }
}
@media screen and (max-width: 676px) {
    .content__txt {
        padding: calc(60% + 10px) 20px 20px 20px;
    }
}
@media screen and (max-width: 576px) {
    .content__txt {
        padding: calc(70% + 10px) 20px 20px 20px;
    }
}
</style>