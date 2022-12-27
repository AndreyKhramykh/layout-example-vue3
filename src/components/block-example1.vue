<template>
    <div class="wrapper">
        <div class="container">
            <div class="content">
                <h3>Spain</h3>
                <h2>Grand Spain Madrid</h2>
                <p>But I must explain to you how all this mistaken idea of account to denouncing pleasure and praising pain was account  born and I account will give you a complete account of the system</p>
                <div class="button button-hovered">Book now</div>
            </div>
        </div>
        <div class="container container_empty"></div>
    </div>
</template>

<style scoped lang="scss">
@import '@/assets/styles/blueButton.scss';

.wrapper {
    background-image: url(@/assets/backgrounds/image1.png);
    background-size: 100% 100%;
    background-repeat: no-repeat;
    background-position: center;
    min-height: 50vh;
    color: white;
    display: flex;
    flex-direction: row;
}

.container {
    position: relative;
    width: 50%;
}
.content {
    position: absolute;
    top: 50%;
    right: 2%;
    left: 2%;
    transform: translateY(-50%);
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    gap: 20px;
    background-color: rgba(35, 35, 35, 0.9);
    padding: 20px 20px;

    h3 {
        font-weight: 300;
        font-size: 20px;
        line-height: 28px;
        letter-spacing: 0.1em;
    }

    h2 {
        font-weight: 400;
        font-size: 20px;
        line-height: 28px;
        text-transform: uppercase;
    }

    p {
        font-weight: 300;
        font-size: 16px;
        line-height: 28px;
        letter-spacing: 0.1em;

    }

}

@media screen and (max-width: 1360px) {
    .content {
        gap: 10px;
    }
    .container {
        padding: 20px;
    }
}
@media screen and (max-width: 1024px) {
    .wrapper {
        display: grid;
        place-items: center;
    }
    .container_empty {
        display: none;
    }
    .container {
        width: 80%;
        position: unset;
    }
    .content {
        position: unset;
        top: none;
        right: none;
        left: none;
        transform: none;
    }
}

</style>