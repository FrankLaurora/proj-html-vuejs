<template>
    <div class="hero md_container">
        <div class="infobox">
            <h2 class="highlighted">Damon Vaughn</h2>
            <h2 class="light">Best-selling author and the most influential public intellectual in the western world right now.</h2>
            <h4 class="slim"><em>- The New York Times </em></h4>
            <div class="page_turner">
                <i class="fas fa-arrow-left btn_left"></i>
                <i class="fas fa-arrow-right btn_right"></i>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Hero'
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/variables.scss';

    .hero {
        position: relative;
        z-index: 1;
    }

    .infobox {
        width: 50%;
        padding-block: 40px;

        h4 {
            color: $gray-text;
            margin-block: 2rem;
        }

        .page_turner {
            i {
                display: inline-block;
                width: 50px;
                height: 50px;
                text-align: center;
                line-height: 50px;
                color: $light-text;
                background-color: rgba(0, 0, 0, 0.5);
            }

            i:first-child {
                margin-right: 1px;
            }

            i:last-child {
                margin-left: 1px;
            }
        }
    }
</style>