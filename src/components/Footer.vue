<template>
  <footer>
    <div class="f-top">
      <div class="container">
        <div class="side-l">
          Left
        </div>
        <div class="side-r">
          <img src="../assets/img/dc-logo-bg.png" alt="">
        </div>
      </div>
    </div>
    <div class="f-bottom">
      <div class="container">
        Ciao
      </div>
    </div>
  </footer>
</template>

<script>

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  footer{
    .f-top{
      height: 300px;
      width: 100vw;
      background-image: url(../assets/img/footer-bg.jpg);
      color: white;
      display: flex;
      justify-content: space-between;
      overflow: hidden;
    }
    .f-bottom{
      height: 90px;
      width: 100vw;
      background-color: #303030;
      color: white;
    }
    
    
  }
  
</style>