<template>
    <section>
        <div class="sm_container">
            <h3 class="light">Subscribe To My Newsletter</h3>
            <p class="subtitle highlighted bold_text">Be notified about book signing tour dates</p>
            <form>
                <input type="email" placeholder="Insert your email ...*">
                <button class="btn btn_green" type="button">Subscribe</button>
            </form>
            <p class="gray">Quibusdam suscipit odit est accusantium officiis? Quo praesentium, earum impedit modi nulla quaerat.</p>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Subscription'
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/variables.scss';

    section {
        background-image: url('../assets/img/banner-2.jpg');
        background-size: cover;
        background-position: top;

        .sm_container {
            text-align: center;
            padding: 120px 80px;

            h3 {
                margin-bottom: 1rem;
            }

            form {
                display: flex;
                justify-content: space-around;
                padding-block: 40px;
            }

            input {
                border: none;
                border-radius: 5px;
                padding-block: 1rem;
                padding-inline: 1.5rem;
                width: 60%;
                outline: none;
            }
        }
    }
</style>