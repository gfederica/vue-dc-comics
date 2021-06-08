<template>

<div class="jumbotron">
    <div class="container">
        <h1>Content goes here</h1>
    </div>
</div>

<section class="comics">
    <div class="container">
        <ComicsList v-for="(comic, index) in comics" :key="index" :thumb="comic.thumb" :series="comic.series" :type="comic.type"/>
    </div>
</section>

</template>
<script>
import ComicsList from './components/ComicsList.vue'

export default {
    name: 'Jumbotron',
    components: {
        ComicsList
    }
}
</script>
<style scoped lang="scss">

@import "../style/general.scss";

.jumbotron {
    padding: 40px 0;
    background-color: black;
}

.comics {
    background-color: $greyColorProductsBg;
}

</style>
