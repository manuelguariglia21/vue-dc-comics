<template>
  <header>
    <div class="container">
      <div>
        <img src="../assets/img/dc-logo.png" alt="">
      </div>
      <nav>
        <ul>
          <li><a href="#"><span>Home</span></a></li>
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
          current: true
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
          current: true
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
  header{
    height: 90px;
    width: 100vw;
    background-color: white;
  }

  
  .container img{
    width: 70px;
  }
  
</style>
