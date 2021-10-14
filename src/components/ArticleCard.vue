<template>
    <div class="article_card">
        <img :src="articleCard.img" :alt="articleCard.title">
        <h4 class="slim med_text">{{articleCard.title}}</h4>
        <div class="gray small_text">{{articleCard.date}} <span class="dark">| {{articleCard.comments}} comments</span></div>
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

    h4 {
        margin-block: 1rem;
    }
</style>