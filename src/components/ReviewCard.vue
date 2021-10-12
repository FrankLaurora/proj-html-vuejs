<template>
    <div>
        <div class="review_card" v-for="(element, index) in reviews" :key="index">
            <div class="text_box">
                <h4>{{element.title}}</h4>
                <p>{{element.content}}</p>
            </div>
            <div class="signature">
                <img :src="require(`../assets/img/${element.logoPath}-xsmall.png`)" :alt="`${element.logoPath} logo`">
                <p><span class="author"><strong>{{element.author}}</strong></span>, {{element.newspaper}}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ReviewCard',

    data() {
        return {
            reviews: [
                {
                    title: 'A True Masterpiece, Bravo!',
                    content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Vero perferendis expedita sapiente, saepe deleniti ad veritatis repellat minus aliquam, blanditiis vel laborum pariatur voluptate accusamus dolorem porro omnis voluptates odit.',
                    logoPath: 'theguardian',
                    author: 'Gerald Hendley',
                    newspaper: 'The Guardian'
                },
                {
                    title: 'A Unique View On The World',
                    content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Vero perferendis expedita sapiente, saepe deleniti ad veritatis repellat minus aliquam, blanditiis vel laborum pariatur voluptate accusamus dolorem porro omnis voluptates odit.',
                    logoPath: 'globe',
                    author: 'Mary Maxey',
                    newspaper: 'The Globe And Mail'
                }
            ]
        }
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
                font-size: 1.5rem;
                margin-bottom: 1rem;
            }

            p {
                color: $gray-text;
            }
        }

        .signature {
            display: flex;
            align-items: center;
            margin-top: 1rem;

            img {
                margin-right: 30px;
            }

            .author {
                color: $gray-text;
            }
        }
    }

</style>