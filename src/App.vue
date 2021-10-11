<template>
  <div id="app">
    <HeaderHeroBox />
    <About />
  </div>
</template>

<script>
import HeaderHeroBox from './components/HeaderHeroBox.vue'
import About from './components/About.vue'


export default {
  components: {
    HeaderHeroBox,
    About
    }
}
</script>

<style lang="scss">
@import './assets/style/common.scss';

</style>
