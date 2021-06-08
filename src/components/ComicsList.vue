<template>
        <div class="product">
          <img :src="thumb" :alt="type">
          <h3>{{series}}</h3>
        </div>
</template>


<script>

export default {
    name: 'ComicsList',
    props: ["thumb", "series", "type"]
}
</script>

<style scoped lang="scss">
@import "../style/general.scss";
@import "../style/mixins.scss";

.product {
    width: calc(100% / 6);
    padding: 20px;
    & img {
        width: 100px;
    }
    & h3 {
        text-transform: uppercase;
        font-size: 12px;
    }
}
</style>