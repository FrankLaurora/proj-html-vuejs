<template>
    <div class="headerHeroBox">
        <div class="overlay">
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

    data() {
        return {
            menu: [
                {
                    link: 'Home',
                    active: true
                },
                
                {
                    link: 'About Me',
                    active: false
                },

                {
                    link: 'Testimonials',
                    active: false
                },

                {
                    link: 'My Blog',
                    active: false
                },

                {
                    link: 'Meetups',
                    active: false
                },

                {
                    link: 'Shop',
                    active: false
                },

                {
                    link: 'Contact Me',
                    active: false
                }
            ]
        }
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

        .overlay {
            position: absolute;
            top: 0;
            left: 0;
            bottom: 0;
            right: 0;
            background: linear-gradient(0deg, rgba(0,0,0,0.6) 0%, rgba(0,0,0, 0.2) 100%);
        }
    }

</style>