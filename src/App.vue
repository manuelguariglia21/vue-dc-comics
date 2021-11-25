<template>
  <div id="app">
    <Header />
    <Main />
    <Info />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Info from './components/Info.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Info,
    Footer
  }
}
</script>

<style lang="scss">
  
@import "./assets/style/vars.scss";
@import "./assets/style/generals.scss";
@import "./assets/style/utilities.scss";
  
</style>
