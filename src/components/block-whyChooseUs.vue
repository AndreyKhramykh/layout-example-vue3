<template>
    <div class="block-one__container">
        <div class="block-one__moduleOne">
            <div class="block-one__h2">Why Choose Us</div>
            <div class="block-one__p">Tion and dislike men who are so beguiled and demoralized by desire by the charms of pleasure of the moment, so blinded by desire, that they cannot foresee.</div>
            <div class="block-one__p">Dislike men who are so beguiled and demoralized by the charms of pleasure of the moment, so blinded by desire, that.</div>
            <div class="button button-hovered">Explore Places </div>
        </div>
        <div class="block-one__moduleTwo">
            <img class="block-one__img align-self" src="@/assets/backgrounds/image1.png" alt="">
            <img class="block-one__img ml10percent" src="@/assets/backgrounds/image3.png" alt="">
        </div>
    </div>
</template>

<style lang="scss">
@import '@/assets/styles/blueButton.scss';


.block-one {
    &__container {
        background-image: url(@/assets/backgrounds/image2.png);
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;
        padding: 10%;
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        gap: 10%;
        color: white;
        min-height: calc(100vh - 88px);
    }

    &__moduleOne {
        display: flex;
        flex-direction: column;
        justify-content: center;
        width: 40%;
    }

    &__moduleTwo {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 20px;
        width: 40%;

        
    }

    &__h2 {
        font-family: Aleo;
        font-weight: 400;
        font-size: 36px;
        line-height: 40px;
        text-transform: capitalize;
    }
    &__p {
        font-family: JosefinSans;
        font-weight: 300;
        font-size: 16px;
        line-height: 28px;
        letter-spacing: 0.1em;
        margin: 20px 0px;
    }
    
    &__img {
        width: 350px;
        height: 220px;
    }
}

.ml10percent {
    margin-left: 10%;
}
.align-self {
    align-self: flex-start;
}

@media screen and (max-width: 1024px) {
    .block-one__container {
        padding: 5%;
        flex-direction: column-reverse;
        gap: 40px;
    }
    .block-one__moduleOne{
        align-items: center;
        width: 100%;
        text-align: center;
    }
    .block-one__moduleTwo {
        flex-direction: row;
        width: auto;
    }
    .ml10percent {
        margin-left: 0;
    }
    .align-self {
        align-self: auto;
    }
}

@media screen and (max-width: 768px) {
    .block-one__img {
        width: 200px;
        height: 120px;
    }
}
@media screen and (max-width: 576px) {
    .block-one__img {
        width: 160px;
        height: 90px;
    }
}
@media screen and (max-width: 375px) {
    .block-one__img {
        width: 100px;
        height: 60px;
    }
}


</style>