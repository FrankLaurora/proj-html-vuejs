<template>
    <section class="more_info">
        <h3>Dig A Little Deeper Into Damon Vaughn</h3>
        <h4>Find out more about the author himsel</h4>
        <div>
            <InfoCard />
        </div>
    </section>
</template>

<script>
import InfoCard from './InfoCard.vue'

export default {
    name: 'MoreInfo',

    components: {
        InfoCard
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/variables.scss';

    .more_info {
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
            color: $dark-green;
        }

        .md_container {
            display: flex;
        }
    }
</style>