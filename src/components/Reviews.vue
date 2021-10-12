<template>
    <div class="reviews md_container">
        <div class="top_bar">
            <div class="title_box">
                <h3>What The Critics Say</h3>
                <h4 class="green_text">Testimonials from around the world</h4>
            </div>
            <button class="btn btn_yellow">Read All Testimonials</button>
        </div>
        <div class="col_left">
            <div class="text_box">
                <h3>Best Author Of His Generation</h3>
                <hr>
                <p class="big_text">This Book will change your perspective on life</p>
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Modi ab soluta id reprehenderit magnam itaque excepturi vel, recusandae porro iusto consequuntur ipsum alias minima blanditiis ullam pariatur. Ipsa, minus obcaecati.</p>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quos optio illo ipsa, quidem deserunt at cumque itaque voluptatum quia recusandae dolores ipsam, necessitatibus cupiditate, fuga molestias hic. Necessitatibus, esse voluptatum.</p>
                <div class="signature"><img :src="require('../assets/img/nytimes-logo-white-xsmall.png')" alt="New York Times logo"><strong>Justine Kilpatrick, <span class="green_text">The New York Times</span></strong></div>
            </div>
        </div>
        <div class="col_right">
            <ReviewCard />
        </div>
    </div>
</template>

<script>
import ReviewCard from './ReviewCard.vue';

export default {
    name: 'Reviews',

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

        .green_text {
            color: $dark-green;
        }

        .signature {
            display: flex;
            align-items: center;
            font-family: 'Roboto', sans-serif;
            padding-top: 1rem;
            
            img{
                margin-right: 1rem;
            }
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
            position: relative;
            width: calc(60% - 40px);
            background-image: url('../assets/img/testimonial2-2x.jpg');
            background-size: cover;
            background-position: center;
            border-bottom-right-radius: 90px;
            padding: 110px 80px;
            overflow: hidden;
            color: #fff;
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
                    border: 1px solid #575a58;
                }

                .big_text {
                    font-size: 1.2rem;
                }

                p {
                    margin-block: 2rem;
                }
            }
        }

        .col_right {
            width: calc(40% - 40px);
        }
    }

</style>