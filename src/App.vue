<template>
  <div id="app">
    <HeaderHeroBox />
    <About />
    <Audiobook />
  </div>
</template>

<script>
import HeaderHeroBox from './components/HeaderHeroBox.vue'
import About from './components/About.vue';
import Audiobook from './components/Audiobook.vue'


export default {
  components: {
    HeaderHeroBox,
    About,
    Audiobook
    }
}
</script>

<style lang="scss">
@import './assets/style/common.scss';

</style>
