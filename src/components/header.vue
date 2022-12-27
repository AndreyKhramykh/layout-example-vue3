<script setup>
import SearchIcon from '@/assets/icons/search.vue'
import ChevronIcon from '@/assets/icons/chevron.vue'
</script>

<template>
    <div class="header__container">
        <div class="header__block">
            <h1>Bhromaon</h1>
            <h3>Save Travel Anywhere</h3>
            <div class="header__input-container">
                <input class="header__input" placeholder="Search Your Travel Destination" type="text">
                <div class="header__search-button button-hovered">
                    <SearchIcon/>
                    <p>Search</p>
                </div>
            </div>
        </div>
        <a href="#BHROMAON" class="header__block header__block_lower text-hovered">
            <div class="header__scroll-txt">Scroll Down</div>
            <ChevronIcon/>
        </a>

    </div>
</template>

<style scoped lang="scss">

@import '@/assets/styles/global.scss';

.header {
    &__container {
    font-family: JosefinSans;
    background-image: url(@/assets/backgrounds/header-bg.png);
    background-size: cover;
    background-repeat: no-repeat;
    min-height: 100vh;
    color: white;
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: 1fr;
    align-items: center;
    justify-items: center;
    }

    &__block {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-between;
        width: 100%;

        h1 {
            font-weight: 700;
            font-size: 48px;
            line-height: 52px;
            text-transform: uppercase;
        }

        h3 {
            font-weight: 400;
            font-size: 22px;
            line-height: 28px;
            letter-spacing: 0.31em;
        }

        &_lower {
            width: fit-content;
            cursor: pointer;
            margin-bottom: 40px;
        }
    }

    &__input-container {
        width: 40%;
        margin-top: 40px;
        background-color: white;
        position: relative;

    }

    &__input {
        font-family: JosefinSans;
        font-weight: 400;
        font-size: 14px;
        line-height: 20px;
        letter-spacing: 0.2em;
        color: #999999;
        padding: 20px;
        width: 70%;
        border: none;

        &:focus {
                outline: none;
        }
    }
    &__search-button {
        position: absolute;
        right: 6px;
        top: 50%;
        transform: translateY(-50%);
        background: #5373FD;
        display: flex;
        flex-direction: row;
        align-items: center;
        padding: 16px 24px;
        gap: 10px;
        cursor: pointer;
           

        p {
            font-family: Aleo;
            font-weight: 400;
            font-size: 14px;
            line-height: 20px;
            letter-spacing: 0.1em;
            text-transform: uppercase;
        }
    }
    &__scroll-txt {
        font-weight: 400;
        font-size: 14px;
        line-height: 20px;
        letter-spacing: 0.2em;
        margin-bottom: 10px;
    }

}

@media screen and (max-width: 1360px) {
    .header__input-container {
        width: 50%;
    }
}
@media screen and (max-width: 1024px) {
    .header__input-container {
        width: 60%;
    }
}
@media screen and (max-width: 768px) {
    .header__input-container {
        width: 80%;
    }
}
@media screen and (max-width: 425px) {
    .header__input-container {
        font-size: 10px;
    }

    .header__input {
        font-size: 8px;
    }
    p {
        display: none;
    }
}
@media screen and (max-width: 375px) {
    h3 {
        text-align: center;
    }
}

</style>