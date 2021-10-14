<template>
    <footer>
        <img :src="require('../assets/img/author-logo-round-small.png')" alt="Logo">
        <div class="md_container">
            <div class="col about">
                <h5 class="light">{{footerAbout.title}}</h5>
                <p class="light_gray">{{footerAbout.content}}</p>
            </div>
            <div class="col">
                <h5 class="light">{{footerLinks.title}}</h5>
                <ul class="fa-ul links">
                    <li class="light" v-for="(element, index) in footerLinks.content" :key="index">
                        <span class="fa-li"><i class="fas fa-angle-right"></i></span>
                        <a href="#">{{element}}</a>
                    </li>
                </ul>
            </div>
            <div class="col contacts">
                <h5 class="light">{{footerContacts.title}}</h5>
                <p class="light_gray">{{footerContacts.address}}</p>
                <p class="light_gray">Phone: {{footerContacts.phone}}</p>
                <p class="light_gray">Mobile: {{footerContacts.mobile}}</p>
                <p class="light_gray">Email: <span class="email light">{{footerContacts.email}}</span></p>
                <ul class="social">
                    <li class="light_gray" v-for="(element, index) in footerContacts.social" :key="index">
                        <a href="#"><i :class="`fab fa-${element}`"></i></a>
                    </li>
                </ul>
            </div>
        </div>
        <p class=" light_gray credits">&copy; Copyright 2012 - 2020 | Avada Theme by <a class="light" href="#">ThemeFusion</a> | All Rights Reserved | Powered by <a class="light" href="#">WordPress</a></p>        
    </footer>
</template>

<script>
export default {
    name: 'Footer',

    props: {
        footerAbout: Object,
        footerLinks: Object,
        footerContacts: Object
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/variables.scss';

    footer {
        position: relative;
        background-image: url('../assets/img/footer-3.jpg');
        background-size: cover;
        background-position: top;
        padding: 120px 0 50px;

        img {
            position: absolute;
            top: 130px;
            left: 120px;
            width: 110px;
        }

        .credits {
            text-align: center;
            margin-top: 5rem;
        }

        .md_container {
            display: flex;
            justify-content: flex-end;
        }
        
        .col {
            width: 445px;
            
            h5 {
                margin-bottom: 2rem;
            }

            .links {
                li {
                    padding: 0.5rem;
                }
            }

        }

        .about {
            p{
                padding: 0.5rem 7.5rem 0 0;
            }
        }

        .contacts {

            p {
                margin-bottom: 1rem;
            }

            .social {
                display: flex;

                li {
                    margin-right: 1rem;
                }
            }
        }
    }
</style>