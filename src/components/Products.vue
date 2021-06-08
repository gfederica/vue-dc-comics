<template>
<div class="products">
    <div class="button button-top">
            <h2>Current series</h2>
    </div>
    <div class="container">
        <ComicsList v-for="(comic, index) in comics" :key="index" :thumb="comic.thumb" :series="comic.series" :type="comic.type"/>
    </div>
    <div class="button button-bottom">
            <h3>load more </h3>
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

    .button {
        @include button ('full');
        display: inline-block;
        position: absolute;
    }

    .button-top {
        top: -20px;
        left: 200px;
    }
    .button-bottom {
        left: 50%;
        bottom: 10px;
        transform: translate(-50%);
        padding: 6px 40px;
    }

    .products {
        background-color: $greyColorProductsBg;
        position: relative;
        
        & h3 {
            text-transform: uppercase;
        }

        .container {
            @include flex;
            flex-wrap: wrap;
            align-items: normal;
            height: 100%;
           padding-top: 60px;
           padding-bottom: 60px;
        }
    }
</style>