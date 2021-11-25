<template>
  <section>
    <div>
      <ul>
        <li v-for="image in images " :key="image">
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
    height: 90px;
    width: 100vw;
    background-color: #0086FF;
    color: white;

    div{
      width: 60%;
      margin: 0 auto;
      line-height: 90px;
      ul{
      @include list();
      a{
        display: flex;
        justify-content: space-between;
        align-items: center;
        text-transform: uppercase;
        color: white;
        text-decoration: none;
        padding-right: 1rem;
        img{
          height: 35px;
          padding-right: 15px;
        }
        span{
          font-size: 10px;
        }
      }
      }
    }

    
  }
  
</style>