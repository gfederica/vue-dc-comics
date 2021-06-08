<template>

<footer>
    <div class="navigate">
        <div class="container">
            <div class="navigate-list">
                <div v-for="(link, index) in links" :key="index">
                    <h2>{{link.title}}</h2>
                    <ul >
                        <li v-for="subtitle in link.subtitle" :key="subtitle"><a href="">{{subtitle}}</a></li>
                    </ul>                
                </div>
            </div>
        </div>
    </div>
    <div class="sign-up-bar">
        <div class="container">
            <div class="button">
                <h2>Sign up now!</h2>
            </div>
            <div class="follow">
                <h2>Follow us</h2>
                <ul>
                    <li v-for="(footerLink, index) in footerLinks" :key="index"><a href=""><img :src="footerLink.img" alt=""></a></li>
                </ul>
            </div>
        </div>
    </div>
</footer>


</template>
<script>


export default {
    name: 'Footer',
    data: function () {
    return {
      links: [
        {
          title: "dc comics",
          subtitle: ["Characters", "Comics","Movies", "TV", "Games", "Videos", "News"]
        },
        {
          title: "shop",
          subtitle: ["Shop DC", "Shop DC Collectibles"]
        },
        {
          title: "dc",
          subtitle: ["Terms of Use", "Privacy Policy (New)", "Ad Choices", "Advertising","Jobs", "Subscriptions", "Talent Workshops", "CPSC Certificates", "Ratings", "Shop Help", "Contact Us"]
        },
        {
          title: "sites",
          subtitle: ["DC", "MAD Magazine", "DC Kids", "DC Universe","DC Power Visa"]
        }
      ],
      footerLinks: [
          {
              name: "facebook",
              img: require("../assets/img/footer-facebook.png")
          },
          {
              name: "twitter",
              img: require("../assets/img/footer-twitter.png")
          },
          {
              name: "youtube",
              img: require("../assets/img/footer-youtube.png")
          },
          {
              name: "pinterest",
              img: require("../assets/img/footer-pinterest.png")
          },
          {
              name: "periscope",
              img: require("../assets/img/footer-periscope.png")
          }
      ]
    }
  }
}
</script>
<style scoped lang="scss">

@import "../style/general.scss";
@import "../style/mixins.scss";


a {
    color: $greyText;
}

.navigate {
    background-image: url($footerBackground);
    background-repeat: no-repeat;
    background-size: cover;
    // position: relative;
    // z-index: -2;
    .navigate-list {
        @include flex-column-wrap;
        align-content: flex-start;
        justify-content: flex-start;
        padding-top: 20px;
        height: 300px;

        h2 {
            margin-bottom: 4px;
        }

        & div {
            margin: 0;
            padding-right: 20px;

            & ul {
                margin-bottom: 14px;

                & li {
                    padding: 2px 0;
                    font-size: 12px;
                }
            }
        }

    
    }

}

.sign-up-bar {
    height: 10vh;
    background-color: $greyColorFooterBg;

    .button {
        @include button;
        margin-left: 0;
    }

    .follow {
        margin-right: 0;
    }

    & > .container {
        @include flex;
        height: 100%;

        & .follow,
        & ul {
            @include flex;
            padding: 0 20px;

            & h2 {
                color: $blueColor;
                font-size: 18px;
            }

            & li {
                padding: 0 6px;

                & img {
                    width: 30px;
                }
            }
        }


    }
}

</style>
