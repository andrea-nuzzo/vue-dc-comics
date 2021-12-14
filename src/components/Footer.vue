<template>
  <footer>
      <div class="backgroundImage">

         <div class="paneContent">
        <div class="container">
          <ul>
            <li v-for="(link, index) in links" :key="index">
              <a :href="link.url">
                <img :src="link.image" :alt="link.text">
                {{link.text.toUpperCase()}}
              </a>
            </li>
          </ul>
        </div>

        <div class="container">
          <div class="nav">
            <ul class="item1">
              <li class="title">DC COMICS</li>
              <li><a href="">Characters</a></li>
              <li><a href="">Comics</a></li>
              <li><a href="">Movies</a></li>
              <li><a href="">TV</a></li>
              <li><a href="">Games</a></li>
              <li><a href="">Videos</a></li>
              <li><a href="">News</a></li>
            </ul>

            <ul class="item2">
              <li class="title">SHOP</li>
              <li><a href="">Shop DC</a></li>
              <li><a href="">Shop DC Collectibles</a></li>
            </ul>

            <ul class="item3">
              <li class="title">DC</li>
              <li><a href="">Terms of Use</a></li>
              <li><a href="">Privacy Policy (New)</a></li>
              <li><a href="">Ad Choices</a></li>
              <li><a href="">Advertising</a></li>
              <li><a href="">Jobs</a></li>
              <li><a href="">Subscriptions</a></li>
              <li><a href="">Talent Workshops</a></li>
              <li><a href="">CPSC Certificates</a></li>
              <li><a href="">Ratings</a></li>
              <li><a href="">Shoip Help</a></li>
              <li><a href="">Contact Us</a></li>
            </ul>

            <ul class="item4">
              <li class="title">SITES</li>
              <li><a href="">DC</a></li>
              <li><a href="">MAD Magazine</a></li>
              <li><a href="">DC Kids</a></li>
              <li><a href="">DC Universe</a></li>
              <li><a href="">DC Power Visa</a></li>
            </ul>
          </div>
          <div class="logoBig">
            <img src="../assets/img/dc-logo-bg.png" alt="">
          </div>
        </div>
      </div>
    </div>
      <div class="social">
        <div class="container">
          <div class="btn">SIGN-UP NOW!</div>
        

          <div class="socialMEdia">
            <div>FOLLOW US</div>
            <img src="../assets/img/footer-facebook.png" alt="">
            <img src="../assets/img/footer-twitter.png" alt="">
            <img src="../assets/img/footer-youtube.png" alt="">
            <img src="../assets/img/footer-pinterest.png" alt="">
            <img src="../assets/img/footer-periscope.png" alt="">
          </div>
        </div>
      </div>
  </footer>
</template>

<script>

export default {
    name: 'Footer',

    data(){
      return{

        links:[
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
      }
    }

}
</script>

<style lang="scss" scoped>
  @import '../assets/style/colorPalette.scss';
  footer{
    height: 100px;
        .paneContent{
      background-color: $blueDC;

      ul{
        display: flex;
        justify-content: center;
        align-items: center;

          li{
          list-style: none;

            a {
              
                img{
                  width: 50px;
                  margin-right: 20px ;
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
    .backgroundImage{

      background-image: url('../assets/img/footer-bg.jpg');
      background-size: cover;
      background-position: center;

      .container{
        display: flex;
        justify-content: space-between;

      }

      .nav{
       display: grid;
       margin: 20px 0;
       
        

        ul{
          margin: 5px;
        }

        .item1{
          grid-column-start: 1;
        }
        .item2{
           grid-column-start: 1;
           grid-row: 2;
        }
        .item3{
           grid-column-start: 2;

        }
         .item4{
           grid-column-start: 3;
        }

        ul li{
          list-style: none;
        }

        ul .title{
          font-size: 20px;
          color: white;
          font-weight: bold;
        }

        ul li a {
          text-decoration: none;
          color: #959595;
        }
      }

      .logoBig img{
        width: 350px;
      }
    }  
  
    .social{
      background-color: $grayBackground;

      .container{
        display: flex;
        justify-content: space-between;
        align-items: center;

        .btn{
          border: 2px solid $blueDC;
          color: white;
          font-size: 20px;
          font-weight: bold;
          padding: 10px;
          cursor: pointer;
        }

        .socialMEdia{
          display: flex;
          align-items: center;
          margin: 30px 0;

          div{
            font-size: 20px;
            font-weight: bold;
            color: $blueDC;
          }

          img{
            margin: 0 10px;
          }
        }
      }

    }

  }

</style>