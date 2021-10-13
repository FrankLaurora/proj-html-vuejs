<template>
    <section class="reviews">
        <div class="md_container">
            <div class="top_bar">
                <div class="title_box">
                    <h3>Recent Articles</h3>
                    <h4 class="green_text">Testimonials from around the world</h4>
                </div>
                <button class="btn btn_yellow">All Articles</button>
            </div>
            <div class="col_left">
                <div class="article_highlight">
                    <img :src="mainArticle.img" :alt="mainArticle.title">
                    <div class="text_box">
                        <h3>{{mainArticle.title}}</h3>
                        <div class="small_text">By <span class="black_text">{{mainArticle.author}}</span> | {{mainArticle.date}} | Categories: <span class="black_text">{{mainArticle.categories}}</span></div>
                        <p>{{mainArticle.content}}</p>
                    </div>
                </div>
            </div>
            <div class="col_right">
                <ArticleCard v-for="(element, index) in articleCards" :key="index" :articleCard="element" />
            </div>
        </div>
    </section>
</template>

<script>
import ArticleCard from './ArticleCard.vue'

export default {
    name: 'RecentArticles',

    components: {
        ArticleCard
    },

    props: {
        mainArticle: Object,
        articleCards: Array
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/variables.scss';

    .reviews {
        background-color: $main-bg;
    }

    .md_container {
        display: flex;
        flex-wrap: wrap;
        padding: 80px 60px;
        justify-content: space-between;

        .green_text {
            color: $dark-green;
        }
        
        h3 {
            font-size: 2.2rem;
        }

        .top_bar {
            width: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;

            h4 {
                text-transform: uppercase;
                font-family: 'Roboto', sans-serif;
                font-weight: 500;
                text-align: center;
                margin-block: 2rem;
                word-spacing: 0.5rem;
            }
        }

        .col_left {
            width: calc(((100% / 3) * 2) - 55px);
            padding: 50px;
            background-color: #fff;

            img {
                width: 100%;
                display: block;
            }

            .text_box {
                padding: 40px 20px 0;
            }

            h3 {
                font-size: 1.5rem;
                font-weight: 400;
                font-family: 'Roboto', sans-serif;
            }

            p {
                color: $gray-text
            }

            .small_text {
                color: $gray-text;
                font-family: 'Roboto', sans-serif;
                margin: 1rem 0 1.5rem;
            }

            .black_text {
                color: #000;
            }
        }

        .col_right {
            display: flex;
            flex-direction: column;
            width: calc(100% / 3);
            padding: 35px;
            background-color: #fff;
        }
    }

</style>