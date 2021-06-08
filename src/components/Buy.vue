<template>
  <div class="buy">
      <div class="container">
          <div v-for="(feature, index) in features" :key="index">
              <img :src="feature.image" alt="">
              <h2>{{feature.text}}</h2>
          </div>
      </div>
  </div>
</template>

<script>
export default {
    name: 'Buy',
    data: function() {
        return {
            features: [
                {
                    image: require("../assets/img/buy-comics-digital-comics.png"),
                    text: "digital comics"
                },
                {
                    image: require("../assets/img/buy-comics-merchandise.png"),
                    text: "dc merchandise"
                },
                {
                    image: require("../assets/img/buy-comics-subscriptions.png"),
                    text: "subscription"
                },
                {
                    image: require("../assets/img/buy-comics-shop-locator.png"),
                    text: "comic shop locator"
                },
                {
                    image: require("../assets/img/buy-dc-power-visa.svg"),
                    text: "dc power visa"
                }
            ]
        }
    }
    }
</script>

<style scoped lang="scss">
@import "../style/general.scss";
@import "../style/mixins.scss";

.buy {
    background-color: $blueColor;
    height: 150px;

    & .container {
        @include flex;
        height: 100%;

        & > div {
            @include flex;
            width: 20%;

            & h2 {
                margin-left: 0;
                font-size: 14px;
            }
            
            & img {
                max-width: 50px;
                max-height: 50px;
                margin-right: 6px;
            }
        }

    }

}

</style>