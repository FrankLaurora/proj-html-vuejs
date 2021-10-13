<template>
    <div class="headerHeroBox">
        <div>
            <Header :menu="menu" />
            <Hero />
            <ShopBox />
        </div>
    </div>
</template>

<script>
import Header from './Header.vue';
import Hero from './Hero.vue';
import ShopBox from './ShopBox.vue';


export default {
    name: 'HeaderHeroBox',

    components: {
        Header,
        Hero,
        ShopBox
    },

    props: {
        menu: Array
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';

    .headerHeroBox{
        position: relative;
        background-image: url('../assets/img/hero-07-2x.jpg');
        background-position: center;
        background-size: cover;
        background-repeat: no-repeat;
        height: 800px;

        &::before {
            position: absolute;
            top: 0;
            left: 0;
            bottom: 0;
            right: 0;
            content: '';
            background: linear-gradient(0deg, rgba(0,0,0,0.6) 0%, rgba(0,0,0, 0.2) 100%);
        }
    }

</style>