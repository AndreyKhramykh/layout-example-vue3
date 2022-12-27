<script setup>
import SearchIcon from '@/assets/icons/search-icon.vue'
import CheckMark from '@/assets/icons/check-mark-icon.vue'
import LikeIcon from '@/assets/icons/like-icon.vue'
</script>

<template>
    <div class="container">
        <div class="wrapper">
            <div class="component-wrapper el1">
                <div class="icon-wrapper">
                    <SearchIcon/>
                </div>
                <p>Search Places</p>
            </div>
            <div class="component-wrapper el2">
                <div class="icon-wrapper">
                    <CheckMark/>
                </div>
                <p>Select Places</p>
            </div>
            <div class="component-wrapper el3">
                <div class="icon-wrapper">
                    <LikeIcon/>
                </div>
                <p>Book & Enjoy</p>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
.container {
    display: grid;
    place-items: center;
    background-color: #333333;
    color: white;
    font-family: Aleo;
    font-weight: 400;
    font-size: 36px;
    line-height: 40px;
    text-align: center;
    text-transform: capitalize;
    padding: 0% 20% 4% 20%;
}

.wrapper {
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    grid-template-rows: repeat(2, 1fr);
    grid-column-gap: 0px;
    grid-row-gap: 0px;
    width: 100%;
    background-image: url(@/assets/backgrounds/dashed-arch.svg);
    background-repeat: no-repeat;
    background-size: 80%;
    background-position: center;
}

.component-wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    white-space: nowrap;

}

.icon-wrapper {
    display: grid;
    place-items: center;
    width: fit-content;
    height: fit-content;
    border-radius: 50%;
    background-color: #333333;
    padding: 20px;

   
}

.el {
    &1 {
        grid-area: 2 / 1 / 3 / 2;
    }

    &2 {
        grid-area: 2 / 3 / 3 / 4;
    }

    &3 {
        grid-area: 2 / 5 / 3 / 6; 
    }
}

@media screen and (max-width: 1360px) {
    .wrapper {
        background-size: 70%;
    }
    .container {
        font-size: 30px;

    }
    
}
@media screen and (max-width: 1024px) {
    .container {
        font-size: 24px;
    }
    
}
@media screen and (max-width: 768px) {
    .wrapper {
        display: flex;
        flex-direction: column;
        background-image: none;
    }
    .container {
        padding: 10px 0;
    }
    
}
</style>