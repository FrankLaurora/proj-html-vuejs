<template>
  <div id="app">
    <HeaderHeroBox />
    <About />
    <Audiobook />
    <Reviews />
    <Events />
    <Subscription />
    <MoreInfo />
    <RecentArticles />
  </div>
</template>

<script>
import HeaderHeroBox from './components/HeaderHeroBox.vue'
import About from './components/About.vue';
import Audiobook from './components/Audiobook.vue';
import Reviews from './components/Reviews.vue';
import Events from './components/Events.vue';
import Subscription from './components/Subscription.vue'
import MoreInfo from './components/MoreInfo.vue';
import RecentArticles from './components/RecentArticles.vue'

export default {
  components: {
    HeaderHeroBox,
    About,
    Audiobook,
    Reviews,
    Events,
    Subscription,
    MoreInfo,
    RecentArticles
    }
}
</script>

<style lang="scss">
@import './assets/style/common.scss';

</style>
