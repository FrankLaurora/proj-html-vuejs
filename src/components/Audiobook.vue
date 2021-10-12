<template>
    <div class="audiobook">
        <div class="top">
            <div class="sm_container">
                <img v-for="(element, index) in formats" :key="index" :src="require(`../assets/img/${element}-logotan-2x-200x66.png`)" :alt="element">
            </div>
        </div>
        <div class="bottom">
            <div class="sm_container">
                <img class="col_6" :src="require('../assets/img/audible-app-2x-600x628.png')" alt="audiobook presetation">
                <div class="text_box col_6">
                    <h3>New Audiobook</h3>
                    <h4>No time to read? No problem. Listen to it</h4>
                    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Tempore saepe officia aliquid, sapiente debitis dicta enim voluptas deleniti delectus.</p>
                    <div class="logos">
                        <img :src="require('../assets/img/audible-logo.png')" alt="audible logo">
                        <img :src="require('../assets/img/bn-logo-tall.png')" alt="bn logo">
                        <img :src="require('../assets/img/kindle-logo-tall.png')" alt="kindle logo">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Audiobook',

    data() {
        return {
            formats: [
                'ebay',
                'audible',
                'bb',
                'kindlefire'
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/variables.scss';

    .audiobook {
        .sm_container {
            display: flex;
            align-items: center;
            height: 100%;
            justify-content: space-between;
        }

        .top {
            background-color: $main-bg;
            height: 200px;

            img {
                width: 20%;
            }
        }

        .bottom {
            background-image: url('../assets/img/banner.jpg');
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;  
            
            .sm_container {
                padding-top: 85px;
                .col_6 {
                    width: calc(50% - 2rem);
                }

                .text_box {
                    text-align: center;

                    h3 {
                        color: $light-text;
                    }

                    h4 {
                        color: $highlighted-text;
                        text-transform: uppercase;
                    }

                    p {
                        color: $gray-text;
                    }
                    
                    .logos {
                        display: flex;
                        justify-content: space-between;
                        
                        img {
                            width: 30%;
                        }
                    }
                }
            }
        }
        
    }

</style>