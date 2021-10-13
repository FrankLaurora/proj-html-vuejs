<template>
    <div class="card_container">
        <div class="article_card" v-for="(element, index) in articleCards" :key="index">
            <img :src="element.img" :alt="element.title">
            <h3>{{element.title}}</h3>
            <div class="small_text">{{element.date}} <span class="black_text">| {{element.comments}} comments</span></div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ArticleCard',

    data() {
        return {
            articleCards: [
                {
                    title: 'What\'s On Your Booklist?',
                    date: 'October 24th, 2019',
                    comments: 0,
                    img: require('../assets/img/thumb-13-2x-320x202.jpg')
                },
                 {
                    title: 'Istanbul Travel Guide',
                    date: 'October 24th, 2019',
                    comments: 0,
                    img: require('../assets/img/thumb-08-2x-320x202.jpg')
                }
            ]
        }
    }

}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/variables.scss';

    .card_container {

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
    }

</style>