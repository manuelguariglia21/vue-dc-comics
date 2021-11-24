<template>
  <header>
    <div class="container">
      <div>
        <img src="../assets/img/dc-logo.png" alt="">
      </div>
      <nav>
        <ul>
          <li v-for="(link, index) in links" :key="index" ><a href="#" ><span :class="{'active': link.current === true}">{{link.text}}</span></a></li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data(){
    return{
      links:[
        {
          url:'/characters',
          text: 'CHARACTERS',
          current: false
        },
        {
          url:'/comics',
          text: 'COMICS',
          current: true
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
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

@import '../assets/style/mixins.scss';
header{
  height: 90px;
  width: 100vw;
  background-color: white;
  color: black;
  font-size: 12px;
  font-weight: bolder;
}

  
.container img{
  width: 70px;
}

ul{
  @include list();

  li{
    a{  
      text-decoration: none;
      margin: 15px;
      &:hover,
      &:active{
        color: #0C7CEC;
      }
      span{
        padding-bottom: 29px;
      }
    }
  }
  
}

span.active{
  color: #0C7CEC;
  border-bottom: 5px solid #0C7CEC;
}
  
</style>
