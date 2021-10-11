<template>
    <div class="hero md_lg_container">
        <div class="infobox">
            <h2>Demon Vaughn</h2>
            <h3>Best-selling author and the most influential public intellectual in the western world right now.</h3>
            <p><em>- The New York Times </em></p>
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

    .infobox {
        width: 50%;
        padding-block: 40px;

        h2 {
            color: $highlighted-text;
            font-size: 3.75rem;
            font-family: 'Caveat', cursive;
        }
        
        h3 {
            color: $light-text;
            font-size: 2.25rem;
            line-height: 5rem;
        }

        p {
            font-family: 'Roboto', sans-serif;
            color: #a3a39a;
            margin-bottom: 2rem;
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