<template>
  <header>
    <div class="container">
      <div class="header-left">
        <img src="../assets/img/dc-logo.png" alt="">
      </div>
      <div class="header-right">
        <ul>
          <li v-for="(link,index) in links" :key="index"><a href="" :class="{active: link.active}">{{link.text}}</a></li>
        </ul>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data: function () {
    return {
      links: [
        {
          text: "characters",
          active: false
        },
        {
          text: "comics",
          active: true
        },
        {
          text: "movies",
          active: false
        },
        {
          text: "tv",
          active: false
        },
        {
          text: "games",
          active: false
        },
        {
          text: "collectibles",
          active: false
        },
        {
          text: "videos",
          active: false
        },
        {
          text: "fans",
          active: false
        },
        {
          text: "news",
          active: false
        },
        {
          text: "shop",
          active: false
        },
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

@import "../style/general.scss";
@import "../style/mixins.scss";


.container {
  @include flex;
  height: 10vh;
  

  .header-left {
    margin-left: 0;
    @include flex;
    width: 60%;
    
    img {
      margin-left: 0;
      width: 54px;
    }
  }


 ul {
   display: flex;

   
   li {
     padding: 0 14px;
   }

   a {
     text-transform: uppercase;
     font-size: 12px;
     color: $darkGreyText;
     font-weight: bold;

     & .active {
       color: $blueColor;
     }
     
   }
 }

}

</style>
