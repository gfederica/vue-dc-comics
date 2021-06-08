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

    & img {
        width: 100px;
    }
}
</style>