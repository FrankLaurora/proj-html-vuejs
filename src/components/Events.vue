<template>
    <section class="events">
        <h3 class="dark">Upcoming Events</h3>
        <p class="subtitle highlighted bold_text">Meet the author in person</p>
        <div class="md_container">
            <EventCard v-for="(element, index) in events" :key="index" :event="element"/>
        </div>
    </section>
</template>

<script>
import EventCard from './EventCard.vue'

export default {
    name: 'Events',

    props: {
        events: Array
    },

    components: {
        EventCard
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/variables.scss';

    .events {
        background-color: $main-bg;
        text-align: center;
        padding-block: 80px;

        h3 {
            margin-bottom: 1rem;
        }
        p {
            margin-bottom: 60px;
        }

        .md_container {
        display: flex;
        justify-content: space-between;
        }
    }
</style>