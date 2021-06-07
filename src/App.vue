<template>
  <div id="app">
    <Header/>
    <main>
      <Jumbotron/>
    </main>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Jumbotron from './components/Jumbotron.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Jumbotron,
    Footer
  }
}
</script>

<style lang="scss">
* {
  box-sizing: border-box;
  margin: 0 auto;
  padding: 0;
}
</style>
