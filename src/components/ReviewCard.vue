<template>
    <div class="review_card">
        <div class="text_box">
            <h4 class="dark">{{review.title}}</h4>
            <p class="gray">{{review.content}}</p>
        </div>
        <div class="signature">
            <img :src="require(`../assets/img/${review.logoPath}-xsmall.png`)" :alt="`${review.logoPath} logo`">
            <p><span class="gray"><strong>{{review.author}}</strong></span>, {{review.newspaper}}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ReviewCard',

    props: {
        review: Object
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/variables.scss';

    .review_card {
        width: 100%;
        margin-bottom: 45px;

        .text_box {
            position: relative;
            background-color: $main-bg;
            text-align: center;
            padding: 40px 50px;

            &::after {
                position: absolute;
                bottom: -13px;
                left: 36px;
                content: "\f0d7";
                font-family: "Font Awesome 6 Free";
                font-weight: 900;
                font-size: 1.5rem;
                color: $main-bg;
            }

            h4 {
                margin-bottom: 1rem;
            }
        }

        .signature {
            display: flex;
            align-items: center;
            margin-top: 1rem;

            img {
                margin-right: 30px;
            }
        }
    }

</style>