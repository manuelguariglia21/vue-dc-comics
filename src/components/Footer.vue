<template>
  <footer>
    <div class="f-top">
      <div class="container flex-box">
        <div class="side-l">
          <div class="f-menu" v-for="(menu, index) in fmenu" :key="index">
            <ul>
              <li v-for="(menu, indice) in fmenu[index]" :key="indice"><a href="#"><span>{{menu}}</span></a></li>
            </ul>
          </div>
        </div>
        <div class="side-r">
          <img src="../assets/img/dc-logo-bg.png" alt="">
        </div>
      </div>
    </div>
    <div class="f-bottom">
      <div class="container flex-box">
        <div class="fb-left">
          <div class="btn"><a href="#">Sign-Up Now!</a></div>
        </div>
        <div class="fb-right">
          <span>Follow us</span>
          <img src="../assets/img/footer-facebook.png" alt="">
          <img src="../assets/img/footer-twitter.png" alt="">
          <img src="../assets/img/footer-youtube.png" alt="">
          <img src="../assets/img/footer-pinterest.png" alt="">
          <img src="../assets/img/footer-periscope.png" alt="">
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  props:{
    fmenu: Array
  },
  data(){
    return{
      
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
      width: 100%;
      background-image: url(../assets/img/footer-bg.jpg);
      background-size: cover;
      color: white;
      display: flex;
      justify-content: space-between;
      overflow: hidden;
      
      .f-menu{
        display: inline-block;
        margin-right: 2vw;
        ul{
        list-style: none;
        color: white;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        li{
          font-size: .8vw;
          &:first-of-type{
            font-size: 1.2vw;
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
      width: 100%;
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
      .fb-right{
        display: flex;
        justify-content: space-between;
        align-items: center;
        span{
          text-transform: uppercase;
          color: #0086FF;
          font-weight: bolder;
        }
        span, img{
          padding-right: 1vw;
        }
        img:last-of-type{
          padding-right: 0;
        }
      }
    }
    
    
  }
  
</style>