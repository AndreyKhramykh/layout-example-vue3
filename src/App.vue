<script setup>
import { ref } from "vue";
import Header from "@/components/header.vue"
import Navigation from '@/components/navigation.vue'
import Block__whyChooseUs from '@/components/block-whyChooseUs.vue'
import Block__steps from '@/components/block-steps.vue'
import Block__example1 from '@/components/block-example1.vue'
import Block__example2 from '@/components/block-example2.vue'
import Block__example3 from '@/components/block-example3.vue'
import Footer from '@/components/footer.vue'

</script>

<template>
  <div class="app">
  <Header/>
  <Navigation/>
  <Block__whyChooseUs/>
  <Block__steps/>
  <Block__example1/>
  <Block__example2/>
  <Block__example3/>
  <Footer/>


  </div>
</template>

<style lang="scss">
@import '@/assets/styles/global.scss';
.app {
  overflow-x: hidden;
}
</style>
