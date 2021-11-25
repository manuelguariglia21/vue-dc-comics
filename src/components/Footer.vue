<template>
  <footer>
    <div class="f-top">
      <div class="container">
        <div class="side-l">
          <div class="f-menu">
            <ul>
              <li v-for="(link, index) in menus.links" :key="index" ><a href="#" ><span :class="{'active': link.current === true}">{{link.text}}</span></a></li>
            </ul>
          </div>
          <div class="f-menu">
            <ul>
              <li v-for="(link, index) in menus.links" :key="index" ><a href="#" ><span :class="{'active': link.current === true}">{{link.text}}</span></a></li>
            </ul>
          </div>
          <div class="f-menu">
            <ul>
              <li v-for="(link, index) in menus.links" :key="index" ><a href="#" ><span :class="{'active': link.current === true}">{{link.text}}</span></a></li>
            </ul>
          </div>
        </div>
        <div class="side-r">
          <img src="../assets/img/dc-logo-bg.png" alt="">
        </div>
      </div>
    </div>
    <div class="f-bottom">
      <div class="container">
        <div class="fb-left">
          <div class="btn"><a href="#">Sign-Up Now!</a></div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  data(){
    return{
      menus: {
        links:[
          {
            url:'/dc comics',
            text: 'Dc Comics',
            current: false
          },
          {
            url:'/characters',
            text: 'Characters',
            current: false
          },
          {
            url:'/comics',
            text: 'Comics',
            current: true
          },
          {
            url:'/movies',
            text: 'Movies',
            current: false
          },
          {
            url:'/tv',
            text: 'TV',
            current: false
          },
          {
            url:'/games',
            text: 'Games',
            current: false
          },
          {
            url:'/videos',
            text: 'Videos',
            current: false
          },
          {
            url:'/news',
            text: 'News',
            current: false
          },
        ]
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/style/mixins.scss';
  footer{

    .f-top{
      height: 300px;
      width: 100vw;
      background-image: url(../assets/img/footer-bg.jpg);
      background-size: cover;
      color: white;
      display: flex;
      justify-content: space-between;
      overflow: hidden;
      
      .f-menu{
        display: inline-block;
        margin-right: 35px;
        ul{
        list-style: none;
        color: white;
        font-size: 12px;
        li{
          &:first-of-type{
            font-size: 16px;
            font-weight: bolder;
            text-transform: uppercase;
          }
          a{
            text-decoration: none;
            color: white;
            span{
              &:hover,
              &:active{
              color: white;
              } 
            }
          }
          
        }
      }
      }
    }

    .f-bottom{
      height: 90px;
      width: 100vw;
      background-color: #303030;
      color: white;
      display: flex;
      justify-content: space-between;
      align-items: center;
      .fb-left{
        .btn a{
          @include btn();
        }
      }
    }
    
    
  }
  
</style>