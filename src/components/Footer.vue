<template>
    <footer>
        <img :src="require('../assets/img/author-logo-round-small.png')" alt="Logo">
        <div class="md_container">
            <div class="col about">
                <h4>{{about.title}}</h4>
                <p>{{about.content}}</p>
            </div>
            <div class="col">
                <h4>{{links.title}}</h4>
                <ul class="fa-ul links">
                    <li v-for="(element, index) in links.content" :key="index">
                        <span class="fa-li"><i class="fas fa-angle-right"></i></span>
                        <a href="#">{{element}}</a>
                    </li>
                </ul>
            </div>
            <div class="col contacts">
                <h4>{{contacts.title}}</h4>
                <p>{{contacts.address}}</p>
                <p>Phone: {{contacts.phone}}</p>
                <p>Mobile: {{contacts.mobile}}</p>
                <p>Email: <span class="email">{{contacts.email}}</span></p>
                <ul class="social">
                    <li v-for="(element, index) in contacts.social" :key="index">
                        <a href="#"><i :class="`fab fa-${element}`"></i></a>
                    </li>
                </ul>
            </div>
        </div>
        <p class="credits">&copy; Copyright 2012 - 2020 | Avada Theme by <a href="#">ThemeFusion</a> | All Rights Reserved | Powered by <a href="#">WordPress</a></p>        
    </footer>
</template>

<script>
export default {
    name: 'Footer',

    data() {
        return {
            about: {
                title: 'about me',
                content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate perspiciatis id, aut sit dolorem animi est inventore! Repellat eius ducimus quam ipsam culpa! Facere ducimus laborum nesciunt ipsam autem quos.'
            },

            links: {
                title: 'useful links',
                content: [
                    'Latest Books',
                    'Upcoming Events',
                    'Recent Articles',
                    'Business Enquiries',
                    'Visit My Foundation'
                ]
            },

            contacts: {
                title: 'contact info',
                address: '63 E. Studebaker Street Bolingbrook, IL 60440',
                phone: '(800) 000-0000',
                mobile: '(800) 000-0000',
                email: 'info@your-company.com',
                social: [
                    'facebook-f',
                    'twitter',
                    'instagram',
                    'linkedin-in',
                    'youtube'
                ]
            }
        }
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
            color: $gray-text;
            margin-top: 5rem;
            
            a {
                color: $light-text;
            }
        }

        .md_container {
            display: flex;
            justify-content: flex-end;
        }
        
        .col {
            width: 445px;
            
            h4 {
                text-transform: uppercase;
                font-size: 1rem;
                color: $light-text;
                margin-bottom: 2rem;
            }

            .links {
                color: $light-text;
                padding-left: 1.5rem;
                font-family: 'Roboto', sans-serif;
                li {
                    padding: 0.5rem;
                }
            }

        }

        .about {
            p{
                color: $gray-text;
                padding: 0.5rem 7.5rem 0 0;
            }
        }

        .contacts {
            color: $gray-text;

            p {
                margin-bottom: 1rem;
            }

            .email {
                color: $light-text;
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