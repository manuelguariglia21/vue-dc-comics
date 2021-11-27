<template>
  <header>
    <div class="container flex-box">
      <div>
        <img src="../assets/img/dc-logo.png" alt="">
      </div>
      <nav>
        <ul>
          <li @click="handleClick(menu, index)" v-for="(link, index) in menu" :key="index" ><a href="#" ><span :class="{'active': link.current === true}">{{link.text}}</span></a></li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  methods: {
    handleClick: function(linkedList, index) {
      for(let i = 0; i < linkedList.length; i++){
        linkedList[i].current = false;
      }
      if(linkedList[index].current === false){
        linkedList[index].current = true;
      }
      else if(linkedList[index].current === true){
        linkedList[index].current = false;
      }
    }
  },
  name: 'Header',
  props:{
    menu: Array
  },
  data(){
    return{
      isActive: true,
    }
  }

}
  
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

@import '../assets/style/mixins.scss';
header{
  height: 90px;
  width: 100%;
  background-color: white;
  color: black;
  font-size: 12px;
  font-weight: bolder;
}

  
.container{
  img{
  width: 70px;
  }
}

ul{
  @include list();

  li{
    a{  
      text-decoration: none;
      margin: 15px;
      color: black;
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
