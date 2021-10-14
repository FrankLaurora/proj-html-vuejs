<template>
    <section class="reviews" id="articles">
        <div class="md_container">
            <div class="top_bar">
                <div class="title_box">
                    <h3 class="dark">Recent Articles</h3>
                    <p class="subtitle green bold_text">Read the last entries</p>
                </div>
                <button class="btn btn_yellow">All Articles</button>
            </div>
            <div class="col_left">
                <div class="article_highlight">
                    <img :src="mainArticle.img" :alt="mainArticle.title">
                    <div class="text_box">
                        <h4 class="slim">{{mainArticle.title}}</h4>
                        <div class="small_text gray">By <span class="dark">{{mainArticle.author}}</span> | {{mainArticle.date}} | Categories: <span class="dark">{{mainArticle.categories}}</span></div>
                        <p class="gray">{{mainArticle.content}}</p>
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

        .top_bar {
            width: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;

            .subtitle {
                margin-block: 1.875rem;
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

            .small_text {
                margin: 1rem 0 1.5rem;
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