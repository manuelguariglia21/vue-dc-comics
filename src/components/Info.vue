<template>
  <section>
    <div class="info">
      <ul>
        <li v-for="(image, index) in images " :key="index">
          <a href="#">
            <img :src="image.image" alt="">
            <span>{{image.text}}</span>
          </a>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Info',
  data(){
    return{
      images:[
        {
          image: require('../assets/img/buy-comics-digital-comics.png'),
          text: 'digital comics'
        },
        {
          image: require('../assets/img/buy-comics-merchandise.png'),
          text: 'dc merchandise'
        },
        {
          image: require('../assets/img/buy-comics-subscriptions.png'),
          text: 'subscription'
        },
        {
          image: require('../assets/img/buy-comics-shop-locator.png'),
          text: 'comic shop locator'
        },
        {
          image: require('../assets/img/buy-dc-power-visa.svg'),
          text: 'dc power visa'
        },
       ]
    }
  }
}      
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/style/mixins.scss';
  section{
    height: 150px;
    width: 100%;
    background-color: #0086FF;
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 15px 0;
    .info{
      width: 65%;
      margin: 0 auto;
      ul{
      @include list();
      li{
        a{
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;
        text-transform: uppercase;
        color: white;
        text-decoration: none;
        img{
          height: 50px;
          padding-right: 5px;
        }
        span{
          font-size: 12px;
        }
      }
      }
      
      }
    }

    
  }
  
</style>