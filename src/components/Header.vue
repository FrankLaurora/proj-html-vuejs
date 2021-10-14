<template>
    <div class="lg_container">
        <img :src="require('../assets/img/author-logo-round-200x205.png')" alt="Logo">
        <ul class="bold_text">
            <li class="small_text" :class="element.active == true ? 'active' : ''" v-for="(element, index) in menu" :key="index"><a :href="`#${element.href}`">{{element.link}}</a></li>
            <li class="small_text"><a href="#"><i class="fas fa-shopping-cart"></i></a></li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'Header',

    props: {
        menu: Array
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/variables.scss';

    .lg_container {
        position: relative;
        z-index: 1;
        height: 185px;
        font-family: 'Roboto', sans-serif;

        ul{
            display: flex;

            li {
                padding-top: 45px;
                margin-left: 45px;
                border-top: 6px solid transparent;
                color: $light-text;

                &.active {
                    color: $highlighted-text;
                    border-top: 6px solid $highlighted-text;
                }
            }
        }
    }
</style>