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
    padding: 10px;
    & img {
        width: 150px;
        height: 150px;
        object-fit: cover;
        object-position: top;
    }

    & h3 {
        text-transform: uppercase;
        font-size: 12px;
        padding-bottom: 10px;
    }
}
</style>