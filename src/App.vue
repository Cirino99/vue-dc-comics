<template>
  <div id="app">
    <Header/>
    <Content/>
    <ContentShop/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import Content from './components/Content.vue'
import ContentShop from './components/ContentShop.vue'

export default {
  name: 'App',
  components: {
    Header,
    Footer,
    Content,
    ContentShop
}
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
