<template>
    <section>
        <div class="sm_container">
            <h3>Subscribe To My Newsletter</h3>
            <h4>Be notified about book signing tour dates</h4>
            <form>
                <input type="email" placeholder="Insert your email ...*">
                <button class="btn btn_green" type="button">Subscribe</button>
            </form>
            <p>Quibusdam suscipit odit est accusantium officiis? Quo praesentium, earum impedit modi nulla quaerat.</p>
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
                color: $light-text;
                font-size: 2.2rem;
                margin-bottom: 1rem;
            }

            h4 {
                text-transform: uppercase;
                font-family: 'Roboto', sans-serif;
                font-weight: 500;
                text-align: center;
                word-spacing: 0.5rem;
                color: $highlighted-text;
            }

            p {
                color: $gray-text
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

            button {
                width: 30%;
            }
        }
    }
</style>