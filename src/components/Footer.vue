<template>
  <footer>
    <!-- Menu buyer con immagini  -->
    <div class="menuBuyBar">
      <div class="container">
        <ul>
          <li v-for="(item, index) in buyBar" :key="index">
            <a :href="item.url">
              <img :src="item.image" :alt="item.text" />
              {{ item.text.toUpperCase() }}
            </a>
          </li>
        </ul>
      </div>
    </div>

    <div class="backgroundImage">
      <div class="container">
        <!-- Menu footer con link  -->
        <div class="menuFooter">
          <div
            :class="`box${index + 1}`"
            v-for="(item, index) in linksMenuFooter"
            :key="index"
          >
            <div class="title">{{ item.title.toUpperCase() }}</div>
            <ul>
              <li v-for="(element, index) in item.link" :key="index">
                <a href="#">{{ element }}</a>
              </li>
            </ul>
          </div>
        </div>

        <!-- sezione log -->
        <div class="logoBig">
          <img src="../assets/img/dc-logo-bg.png" alt="" />
        </div>
      </div>
    </div>

    <div class="social">
      <div class="container">
        <div class="btn">SIGN-UP NOW!</div>

        <div class="socialMEdia">
          <div>FOLLOW US</div>
          <img v-for="(element, index) in socialMedia" :key="index" :src="element.img" :alt="element.name">
        </div>
      </div>
    </div>

  </footer>
</template>

<script>
export default {
  name: "Footer",

  data() {
    return {
      buyBar: [
        {
          text: "digital comics",
          image: require("../assets/img/buy-comics-digital-comics.png"),
          url: "#",
        },
        {
          text: "dc merchandise",
          image: require("../assets/img/buy-comics-merchandise.png"),
          url: "#",
        },
        {
          text: "subscription",
          image: require("../assets/img/buy-comics-subscriptions.png"),
          url: "#",
        },
        {
          text: "comic shop locator",
          image: require("../assets/img/buy-comics-shop-locator.png"),
          url: "#",
        },
        {
          text: "dc power visa",
          image: require("../assets/img/buy-dc-power-visa.svg"),
          url: "#",
        },
      ],

      linksMenuFooter: [
        {
          title: "dc comics",
          link: [
            "Characters",
            "Comics",
            "Movies",
            "TV",
            "Games",
            "Video",
            "News",
          ],
        },
        {
          title: "dc",
          link: [
            "Terms of Use",
            "Privacy Policy (New)",
            "Ad Choices",
            "Advertising",
            "Jobs",
            "Subscriptions",
            "Talent Workshops",
            "CPSC Certificates",
            "Ratings",
            "Shoip Help",
            "Contact Us",
          ],
        },
        {
          title: "sites",
          link: [
            "DC",
            "MAD Magazine",
            "DC Kids",
            "DC Universe",
            "DC Power Visa",
          ],
        },
        {
          title: "shop",
          link: ["Shop DC", "Shop DC Collectibles"],
        },
      ],

      socialMedia:[
        {
          name:'facebook',
          img:require("../assets/img/footer-facebook.png"),
        },
        {
          name:'twitter',
          img:require("../assets/img/footer-twitter.png"),
        },
        {
          name:'youtube',
          img:require("../assets/img/footer-youtube.png"),
        },
        {
          name:'pinterest',
          img:require("../assets/img/footer-pinterest.png"),
        },
        {
          name:'periscope',
          img:require("../assets/img/footer-periscope.png"),
        },
        
      ]
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/style/colorPalette.scss";
footer {
  height: 100px;

  .menuBuyBar {
    background-color: $blueDC;
    z-index: 2;

    ul {
      display: flex;
      justify-content: center;
      align-items: center;

      li {
        list-style: none;

        a {
          height:  55px;

          img {
            height: 100%;
            margin-right: 20px;
          }


          display: flex;
          align-items: center;
          text-decoration: none;
          color: white;
          margin: 30px 30px;
        }
      }
    }
  }

  .backgroundImage {
    background-image: url("../assets/img/footer-bg.jpg");
    background-size: cover;
    background-position: center;
    position: relative;
    z-index: -1;

    .container {
      display: flex;
      justify-content: space-between;
    }
    // MENU FOOTER CON LINK
    .menuFooter {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
      padding: 40px;
    }
    .box1,
    .box2,
    .box3,
    .box4 {
      
      .title{
        color: white;
        font-size: 20px;
        font-weight: bold;
      }

      ul{
        & > *{
          list-style: none;
          a{
            text-decoration: none;
            color: #959595;

            &:hover{
              color: $blueDC;
            }
          }
        }
      }
      
    }

    .box1 {
      grid-row: 1/1;
    }
    .box4 {
      grid-row: 2/2;
    }
    .box2,
    .box3 {
      grid-row: 1/3;
    }


    .logoBig img {
      z-index: 0;
      position: absolute;
      right: 300px;
      bottom: -40px;
      width: 450px;
    }
  }

  .social {
    background-color: $grayBackground;
    z-index: 2;

    .container {
      display: flex;
      justify-content: space-between;
      align-items: center;

      .btn {
        border: 2px solid $blueDC;
        color: white;
        font-size: 20px;
        font-weight: bold;
        padding: 10px;
        cursor: pointer;
      }

      .socialMEdia {
        display: flex;
        align-items: center;
        margin: 30px 0;

        div {
          font-size: 20px;
          font-weight: bold;
          color: $blueDC;
        }

        img {
          margin: 0 10px;
        }
      }
    }
  }
}
</style>