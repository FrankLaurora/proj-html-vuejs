<template>
    <section class="events">
        <h3>Upcoming Events</h3>
        <h4>Meet the author in person</h4>
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
            font-size: 2.2rem;
            margin-bottom: 1rem;
        }
        h4 {
            text-transform: uppercase;
            font-family: 'Roboto', sans-serif;
            font-weight: 500;
            text-align: center;
            margin-bottom: 60px;
            word-spacing: 0.5rem;
            color: $highlighted-text;
        }

        .md_container {
        display: flex;
        justify-content: space-between;
        }
    }
</style>