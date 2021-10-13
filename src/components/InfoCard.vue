<template>
    <div class="info_card md_container">
        <div class="col_third" v-for="(element, index) in cardInfo" :key="index" :style="{backgroundImage: 'url(' + element.img + ')'}">
            <div class="text_box">
                <h3>{{element.title}}</h3>
                <hr>
                <p>{{element.content}}</p>
                
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'InfoCard',

    data() {
        return {
            cardInfo: [
                {
                    title: 'About Me',
                    content: 'Vestibulum ante ipsum primis',
                    img: require('../assets/img/box-1.jpg')
                },
                {
                    title: 'My Latest Book',
                    content: 'Vestibulum ante ipsum primis',
                    img: require('../assets/img/box-4.jpg')
                },
                {
                    title: 'Book',
                    content: 'Vestibulum ante ipsum primis',
                    img: require('../assets/img/box-3.jpg')
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/variables.scss';

    .md_container {
        display: flex;
        padding: 80px 60px;
        justify-content: space-between;
    }

    .col_third {
        position: relative;
        width: calc((100% - 110px) / 3);
        background-size: cover;
        background-position: left;
        border-bottom-right-radius: 90px;
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

            h3 {
                font-family: 'Roboto', sans-serif;
                font-size: 1.5rem;
                margin-block: 20px;
                font-weight: 400;
            }

            hr {
                border: 1px solid #575a58;
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