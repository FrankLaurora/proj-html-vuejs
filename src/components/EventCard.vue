<template>
    <div class="card">
        <img :src="require(`../assets/img/event-${event.img}-400x240.jpg`)" :alt="event.title">
        <div class="text_box">
            <h4 class="slim">{{event.title}}</h4>
            <hr>
            <p class="gray">{{event.content}}</p>
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
            transition: 0.1s;
        }

        .text_box {
            background-color: #fff;
            padding: 36px;

            hr {
                margin-block: 1rem;
                border-top: 2px solid #e8e8e8;
            }
        }
    }

</style>