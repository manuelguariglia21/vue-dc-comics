<template>
  <section class="jumbotron">
  </section>
</template>

<script>
export default {
  name: 'Jumbotron',
  data(){
    return{
    } 
  }
}      
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/style/mixins.scss';
  .jumbotron{
    background-image: url('../assets/img/jumbotron.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    width: 100vw;
    height: 300px;
  }
  
</style>