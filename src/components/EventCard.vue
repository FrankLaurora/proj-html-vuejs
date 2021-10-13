<template>
    <div class="card">
        <img :src="require(`../assets/img/event-${event.img}-400x240.jpg`)" :alt="event.title">
        <div class="text_box">
            <h4>{{event.title}}</h4>
            <hr>
            <p>{{event.content}}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'EventCard',

    props: {
        event: Object
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/variables.scss';
    

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

            h4 {
                font-size: 1.5rem;
                font-weight: 400;
                font-family: 'Roboto', sans-serif;
            }

            hr {
                margin-block: 1rem;
                border: 0.5px solid #e8e8e8;
            }

            p {
                color: $gray-text
            }
        }
    }

</style>