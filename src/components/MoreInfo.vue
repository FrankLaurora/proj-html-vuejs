<template>
    <section class="more_info">
        <h3 class="dark">Dig A Little Deeper Into Damon Vaughn</h3>
        <p class="subtitle green bold_text">Find out more about the author himsel</p>
        <div class="md_container">
            <InfoCard v-for="(element, index) in cardInfo" :key="index" :info="element"/>
        </div>
    </section>
</template>

<script>
import InfoCard from './InfoCard.vue'

export default {
    name: 'MoreInfo',

    props: {
        cardInfo: Array
    },

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
            margin-bottom: 1rem;
        }
        p {
            margin-bottom: 60px;
        }

        .md_container {
        display: flex;
        padding-inline: 60px;
        justify-content: space-between;
        }
    }
</style>