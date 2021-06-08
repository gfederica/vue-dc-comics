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
import dcComics from './data/dcComics'


export default {
  name: 'App',
  components: {
    Header,
    Jumbotron,
    ComicsList,
    Footer
  },
    data: function() {
        return {
            comics: dcComics
        }
    }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=PT+Sans:wght@400;700&display=swap');
$titleFont: 'PT Sans';

body {
    font-family: $titleFont, sans-serif;
}


* {
  box-sizing: border-box;
  margin: 0 auto;
  padding: 0;
}
</style>
