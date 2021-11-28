<template>
  <div id="app">
    <Header :menu = "linkedList"/>
    <Jumbotron />
    <Main />
    <Info />
    <Footer :fmenu = "footerMenus"/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Jumbotron from './components/Jumbotron.vue'
import Main from './components/Main.vue'
import Info from './components/Info.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Jumbotron,
    Main,
    Info,
    Footer
  },
  data(){
    return{
      linkedList:[
        {
          url:'/characters',
          text: 'CHARACTERS',
          current: false
        },
        {
          url:'/comics',
          text: 'COMICS',
          current: false
        },
        {
          url:'/movies',
          text: 'MOVIES',
          current: false
        },
        {
          url:'/tv',
          text: 'TV',
          current: false
        },
        {
          url:'/games',
          text: 'GAMES',
          current: false
        },
        {
          url:'/collectibles',
          text: 'COLLECTIBLES',
          current: false
        },
        {
          url:'/videos',
          text: 'VIDEOS',
          current: false
        },
        {
          url:'/fans',
          text: 'FANS',
          current: false
        },
        {
          url:'/news',
          text: 'NEWS',
          current: false
        },
        {
          url:'/shop',
          text: 'SHOP',
          current: false
        },
      ],

    footerMenus: [

      ['dc comics', 'characters', 'comics', 'movies', 'TV', 'games', 'videos', 'news'],

      ['dc', 'terms of use', 'privacy policy (New)', 'ad choices', 'advertising', 'jobs', 'subscritions', 'talent workshops', 'CPSC Certificates', 'ratings', 'shop help', 'contact us'],

      ['sites', 'DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa'],

      ['shop', 'shop DC', 'shop DC Collectibles'],

],
    }
  }
}
</script>

<style lang="scss">
  
@import "./assets/style/vars.scss";
@import "./assets/style/generals.scss";
@import "./assets/style/utilities.scss";
  
</style>
