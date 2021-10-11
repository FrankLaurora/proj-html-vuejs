<template>
    <div class="lg_container">
        <img :src="require('../assets/img/author-logo-round-small.png')" alt="Logo">
        <ul>
            <li class="small_text" :class="element.active == true ? 'active' : ''" v-for="(element, index) in menu" :key="index">{{element.link}}</li>
            <li class="small_text"><i class="fas fa-shopping-cart"></i></li>
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