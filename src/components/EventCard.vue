<template>
    <div class="md_container">
        <div class="card" v-for="(element, index) in events" :key="index">
            <img :src="require(`../assets/img/event-${element.img}-400x240.jpg`)" :alt="element.title">
            <div class="text_box">
                <h4>{{element.title}}</h4>
                <hr>
                <p>{{element.content}}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'EventCard',

    data() {
        return {
            events: [
                {
                    title: 'Chicago Book Signing',
                    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam, aspernatur suscipit dicta velit quae eius fuga dignissimos.',
                    img: '05'
                },
                {
                    title: 'Meet & Greet With Amanda',
                    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam, aspernatur suscipit dicta velit quae eius fuga dignissimos.',
                    img: '04'
                },
                {
                    title: 'Open Book: Dialogues',
                    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam, aspernatur suscipit dicta velit quae eius fuga dignissimos.',
                    img: '07'
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
        justify-content: space-between;

        .card {
            width: calc((100% - 100px) / 3);

            img {
                position: relative;
                display: block;
                width: 100%;
            }

            &:hover img {
                filter: opacity(70%);
            }

            .text_box {
                background-color: #fff;
                padding: 36px;

                hr {
                    margin-block: 1rem;
                    border: 0.5px solid #e8e8e8;
                }

                p {
                    color: $gray-text
                }
            }
        }
    }

</style>