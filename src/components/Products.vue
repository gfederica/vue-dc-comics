<template>
<div class="products">
    <div class="container">
        <ComicsList v-for="(comic, index) in comics" :key="index" :thumb="comic.thumb" :series="comic.series" :type="comic.type"/>
    </div>
</div>
</template>

<script>
import ComicsList from '../components/ComicsList.vue'
import dcComics from '../data/dcComics'

export default {
    name: 'Products',
    components: {
        ComicsList
    },
    data: function() {
        return {
            comics: dcComics
        }
    }
}


</script>

<style scoped lang="scss">
    @import "../style/general.scss";
    @import "../style/mixins.scss";

    .products {
        background-color: $greyColorProductsBg;

        .container {
            @include flex;
            flex-wrap: wrap;
            align-items: normal;
        }
    }
</style>