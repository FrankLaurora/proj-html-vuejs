<template>
    <section class="reviews md_container" id="testimonials">
        <div class="top_bar">
            <div class="title_box">
                <h3 class="dark">What The Critics Say</h3>
                <p class="subtitle green bold_text">Testimonials from around the world</p>
            </div>
            <button class="btn btn_yellow">Read All Testimonials</button>
        </div>
        <div class="col_left" :style="{backgroundImage: 'url(' + mainReview.img + ')'}">
            <div class="text_box">
                <h3 class="light">{{mainReview.title}}</h3>
                <hr>
                <p class="med_text light">{{mainReview.subtitle}}</p>
                <p class="light" v-for="(element, index) in mainReview.paragraphs" :key="index">{{element}}</p>
                <div class="signature">
                    <img :src="mainReview.logoPath" :alt="mainReview.newspaper">
                    <p class="light bold_text">{{mainReview.author}}, <span class="green">{{mainReview.newspaper}}</span></p>
                </div>
            </div>
        </div>
        <div class="col_right">
            <ReviewCard v-for="(element, index) in reviews" :key="index" :review="element"/>
        </div>
    </section>
</template>

<script>
import ReviewCard from './ReviewCard.vue';

export default {
    name: 'Reviews',

    props: {
        mainReview: Object,
        reviews: Array
    },

    components: {
        ReviewCard
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/variables.scss';

    .md_container {
        display: flex;
        flex-wrap: wrap;
        padding: 80px 60px;
        justify-content: space-between;

        .signature {
            display: flex;
            align-items: center;
            padding-top: 1rem;
            
            img{
                margin-right: 1rem;
            }
        }
        
        .top_bar {
            width: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 45px;

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
            position: relative;
            width: calc(60% - 40px);
            background-size: cover;
            background-position: center;
            border-bottom-right-radius: 90px;
            padding: 110px 80px;
            overflow: hidden;
            align-self: flex-start;

            &::before {
                position: absolute;
                top: 0;
                left: 0;
                bottom: 0;
                right: 0;
                content: '';
                background: linear-gradient(0deg, rgba(0,0,0,0.6) 0%, rgba(0,0,0, 0.2) 100%);
            }

            .text_box {
                position: relative;
                z-index: 1;

                hr {
                    margin-top: 2.5rem;
                }

                p {
                    margin-block: 1.5rem;
                }
            }
        }

        .col_right {
            width: calc(40% - 40px);
        }
    }

</style>