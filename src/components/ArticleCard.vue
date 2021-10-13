<template>
    <div class="article_card">
        <img :src="articleCard.img" :alt="articleCard.title">
        <h3>{{articleCard.title}}</h3>
        <div class="small_text">{{articleCard.date}} <span class="black_text">| {{articleCard.comments}} comments</span></div>
    </div>
</template>

<script>
export default {
    name: 'ArticleCard',

    props: {
        articleCard: Object
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/variables.scss';

    .article_card {
        margin-bottom: 3rem;
    }

    img {
        width: 100%;
        display: block;
    }

    h3 {
        font-size: 1.5rem;
        font-weight: 400;
        font-family: 'Roboto', sans-serif;
        margin-block: 1rem;
    }

    .small_text {
        color: $gray-text;
        font-family: 'Roboto', sans-serif;
    }

    .black_text {
        color: #000;
    }
</style>