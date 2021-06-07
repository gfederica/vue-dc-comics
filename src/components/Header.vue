<template>
  <header>
    <div class="container">
      <div class="header-left">
        <img src="../assets/img/dc-logo.png" alt="">
      </div>
      <div class="header-right">
        <ul>
          <li v-for="(link,index) in links" :key="index"><a href="">{{link.text}}</a></li>
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
          active: false
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

header {
  text-transform: uppercase;
}


.container {
  display: flex;
  height: 10vh;
  

  .header-left {
    margin-left: 0;
    display: flex;
    align-items: center;
    
    img {
      margin-left: 0;
      max-width: 60%;
    }
  }


 ul {
   display: flex;

   
   li {
     padding: 8px;
   }

   a {
     font-size: 14px;
     color: $darkGreyText;
     font-weight: bold;
     
   }
 }

}

</style>
