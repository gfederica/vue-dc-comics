<template>

<footer>
    <div class="pre-footer"></div>
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
        <div class="button">
            <h2>Sign up now!</h2>
        </div>
        <div class="follow">
            <h2>Follow us</h2>
            <ul>
                <li v-for="(link, index) in footerLink" :key="index"><a href=""><img src="" alt=""></a></li>
            </ul>
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
      footerLink: [
          {
              name: "facebook",
              img: "../assets/img/footer-facebook.png"
          },
          {
              name: "twitter",
              img: "../assets/img/footer-twitter.png"
          },
          {
              name: "youtube",
              img: "../assets/img/footer-youtube.png"
          },
          {
              name: "pinterest",
              img: "../assets/img/footer-pinterest.png"
          },
          {
              name: "periscope",
              img: "../assets/img/footer-periscope.png"
          }
      ]
    }
  }
}
</script>
<style scoped lang="scss">

@import "../style/general.scss";

.pre-footer {
    height: 150px;
    background-color: $blueColor;
}

h2 {
    text-transform: uppercase;
}

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
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;
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
}

</style>
