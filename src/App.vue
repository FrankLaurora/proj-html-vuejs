<template>
  <div id="app">
    <HeaderHeroBox :menu="menu" />
    <About :about="about" />
    <Audiobook />
    <Reviews :reviews="reviews" :mainReview="highlightedReview"/>
    <Events :events="events"/>
    <Subscription />
    <MoreInfo :cardInfo="cardInfo"/>
    <RecentArticles :mainArticle="article_highlight" :articleCards="articleCards"/>
    <Footer :footerAbout="footerAbout" :footerLinks="footerLinks" :footerContacts="footerContacts"/>
    <ToTopButton />
  </div>
</template>

<script>
import HeaderHeroBox from './components/HeaderHeroBox.vue'
import About from './components/About.vue';
import Audiobook from './components/Audiobook.vue';
import Reviews from './components/Reviews.vue';
import Events from './components/Events.vue';
import Subscription from './components/Subscription.vue'
import MoreInfo from './components/MoreInfo.vue';
import RecentArticles from './components/RecentArticles.vue';
import Footer from './components/Footer.vue';
import ToTopButton from './components/ToTopButton.vue'

export default {
  components: {
    HeaderHeroBox,
    About,
    Audiobook,
    Reviews,
    Events,
    Subscription,
    MoreInfo,
    RecentArticles,
    Footer,
    ToTopButton
  },

  data() {
      return {
        // header navbar data
        menu: [
          {
            link: 'Home',
            active: true,
            href: 'home'
          },          
          {
            link: 'About Me',
            active: false,
            href: 'about'
          },
          {
            link: 'Testimonials',
            active: false,
            href: 'testimonials'
          },
          {
            link: 'My Blog',
            active: false,
            href: 'my_blog'
          },
          {
            link: 'Meetups',
            active: false,
            href: 'meetups'
          },
          {
            link: 'Shop',
            active: false,
            href: 'shop'
          },
          {
            link: 'Contact Me',
            active: false,
            href: 'contacts'
          }
        ],
        // about seciton data
        about: {
          title: 'More About Damon Vaughn',
          content: 'Damon Vaughn is a professor of psychology at the University of Toronto, a clinical psychologist and the author of the multi-million copy bestseller "The story of my life."'
        },
        //reviews highlighted data
        highlightedReview: {
          img: require('./assets/img/testimonial2-2x.jpg'),
          title: 'Best Author Of His Generation',
          subtitle: 'This Book will change your perspective on life',
          paragraphs: {
            first: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Modi ab soluta id reprehenderit magnam itaque excepturi vel, recusandae porro iusto consequuntur ipsum alias minima blanditiis ullam pariatur. Ipsa, minus obcaecati.',
            second: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Modi ab soluta id reprehenderit magnam itaque excepturi vel, recusandae porro iusto consequuntur ipsum alias minima blanditiis ullam pariatur. Ipsa, minus obcaecati.'
          },
          author: 'Justine Kilpatrick',
          newspaper: 'The New York Times',
          logoPath: require('./assets/img/nytimes-logo-white-xsmall.png')
        },
        //review cards data
        reviews: [
          {
            title: 'A True Masterpiece, Bravo!',
            content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Vero perferendis expedita sapiente, saepe deleniti ad veritatis repellat minus aliquam, blanditiis vel laborum pariatur voluptate accusamus dolorem porro omnis voluptates odit.',
            logoPath: 'theguardian',
            author: 'Gerald Hendley',
            newspaper: 'The Guardian'
          },
          {
            title: 'A Unique View On The World',
            content: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Vero perferendis expedita sapiente, saepe deleniti ad veritatis repellat minus aliquam, blanditiis vel laborum pariatur voluptate accusamus dolorem porro omnis voluptates odit.',
            logoPath: 'globe',
            author: 'Mary Maxey',
            newspaper: 'The Globe And Mail'
          }
        ],
        //events cards data
        events: [
          {
            title: 'Chicago Book Signing',
            content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam, aspernatur suscipit dicta velit quae eius fuga dignissimos.',
            img: '05'
          },
          {
            title: 'Meet & Greet With Amanda',
            content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam, aspernatur suscipit dicta velit quae eius fuga dignissimos.',
            img: '04'
          },
          {
            title: 'Open Book: Dialogues',
            content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam, aspernatur suscipit dicta velit quae eius fuga dignissimos.',
            img: '07'
          }
        ],
        //info cards data
        cardInfo: [
          {
            title: 'About Me',
            content: 'Vestibulum ante ipsum primis',
            img: require('./assets/img/box-1.jpg')
          },
          {
            title: 'My Latest Book',
            content: 'Vestibulum ante ipsum primis',
            img: require('./assets/img/box-4.jpg')
          },
          {
            title: 'Book',
            content: 'Vestibulum ante ipsum primis',
            img: require('./assets/img/box-3.jpg')
          }
        ],
        //articles highlighted data
        article_highlight: {
          title: '20 Creativity Tips',
          author: 'admin',
          date: 'October 24th, 2019',
          categories: 'Event, Tips & Tricks',
          content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe sint provident voluptate enim dolor eos minus excepturi reiciendis, illo molestiae, reprehenderit numquam iste dolores voluptatibus dolorem eum, consectetur quas repellat!',
          img: require('./assets/img/20-Tips-800x471.jpg')
        },
        //article cards data
        articleCards: [
          {
            title: 'What\'s On Your Booklist?',
            date: 'October 24th, 2019',
            comments: 0,
            img: require('./assets/img/thumb-13-2x-320x202.jpg')
          },
          {
            title: 'Istanbul Travel Guide',
            date: 'October 24th, 2019',
            comments: 0,
            img: require('./assets/img/thumb-08-2x-320x202.jpg')
          }
        ],
        //footer about section
        footerAbout: {
          title: 'about me',
          content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptate perspiciatis id, aut sit dolorem animi est inventore! Repellat eius ducimus quam ipsam culpa! Facere ducimus laborum nesciunt ipsam autem quos.'
        },
        //footer links list
        footerLinks: {
          title: 'useful links',
          content: [
            {
              link: 'Latest Books',
              href: 'home'
            },
            {
              link: 'Upcoming Events',
              href: 'meetups'
            },
            {
              link: 'Recent Articles',
              href: 'articles'
            },
            {            
              link: 'Business Enquiries',
              href: 'my_blog'
            },
            {            
              link: 'Visit My Foundation',
              href: 'contacts'
            }
          ]
        },
        //footer contacts section
        footerContacts: {
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

<style lang="scss">
@import './assets/style/common.scss';

</style>