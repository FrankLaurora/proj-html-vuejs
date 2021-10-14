<template>
    <div class="col_third" :style="{backgroundImage: 'url(' + info.img + ')'}">
        <div class="text_box">
            <h4 class="slim big_text">{{info.title}}</h4>
            <hr>
            <p>{{info.content}}</p>     
        </div>
    </div>
</template>

<script>
export default {
    name: 'InfoCard',

    props: {
        info: Object
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/variables.scss';

    .col_third {
        position: relative;
        width: calc((100% - 110px) / 3);
        background-size: cover;
        background-position: left;
        border-bottom-right-radius: 45px;
        padding: 380px 80px 45px;
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

        &:hover {
            transform: scale(1.03);
            box-shadow: 0 5px 10px #000;
            transition: 0.1s;
        }

        .text_box {
            position: relative;
            text-align: center;
            z-index: 1;

            h4 {
                margin-block: 20px;
            }

            hr {
                width: 50px;
                margin: auto;
            }

            p {
                margin-top: 20px;
                color: $highlighted-text;
            }
        }
    }
</style>