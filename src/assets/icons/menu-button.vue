<script setup>
import {ref} from 'vue';

let isActive = ref(false);

let toggleButtonClass = () => {
    isActive.value = !isActive.value;
}
</script>

<template>
    <div @click="toggleButtonClass" :class="['menu-button', {active: isActive}]">
        <span></span>
        <span></span>
        <span></span>
    </div>
</template>

<style scoped lang="scss">
.menu-button {
  cursor: pointer;
  width: fit-content;

}

.menu-button > span {
  display: block;
  width: 28px;
  height: 2px;
  background-color: white;
  border-radius: 9999px;
}

.menu-button > span:not(:last-child) {
  margin-bottom: 7px;
}

.menu-button, .menu-button > span {
  transition: all 0.4s ease-in-out;
}

.menu-button.active {
  transition-delay: 0.8s;
  transform: rotate(45deg);
}

.menu-button.active > span:nth-child(2) {
  width: 0;
}
.menu-button.active > span:nth-child(1),
.menu-button.active > span:nth-child(3) {
  transition-delay: 0.4s;
}

.menu-button.active > span:nth-child(1) {
  transform: translateY(9px);
}
.menu-button.active > span:nth-child(3) {
  transform: translateY(-9px) rotate(90deg);
}

</style>