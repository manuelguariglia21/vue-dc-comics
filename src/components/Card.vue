<template>
    <section>
      <div class="card">
        <img :src="cardImage" alt="">
      </div>
      <div class="desc">
        {{cardName}}
      </div>
      
    </section>
</template>

<script>
export default {
  name: 'Card',
  props:{
    cardName: String,
    cardImage: String,
  }
  
}      
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/style/mixins.scss';
@import '../assets/style/vars.scss';
.card{
  width: calc(100vw / 6);
  height: calc(100vw / 6);
  margin: 5px;
  background-color: red;
  overflow: hidden;
  img{
    width: 100%;
  }
}
.desc{
  width: calc(100vw / 6);
  font-weight: bolder;
  text-transform: uppercase;
  margin-left: 5px;

}
</style>