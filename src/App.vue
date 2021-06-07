<template>
  <div id="app">
    <Header/>
    <main>
      <Jumbotron/>
    </main>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Jumbotron from './components/Jumbotron.vue'

export default {
  name: 'App',
  components: {
    Header,
    Jumbotron
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
