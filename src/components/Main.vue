<template>
  <main>
    <div class="container">
      <div class="content">
        <div>Content goes here</div>   
      </div>
    </div>

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
      </div>

  </main>
</template>

<script>
import digitalComics from "../assets/img/buy-comics-digital-comics.png";
import dcmerchandise from "../assets/img/buy-comics-merchandise.png";
import subscription from "../assets/img/buy-comics-subscriptions.png";
import comicshoplocator from "../assets/img/buy-comics-shop-locator.png";
import dcpowervisa from "../assets/img/buy-dc-power-visa.svg";



export default {
    name: 'Main',
    data(){
      return{
        links:[
          {
            text: "digital comics",
            image: digitalComics,
            url: "#",
          },
          {
            text: "dc merchandise",
            image: dcmerchandise,
            url: "#",
          },
          {
            text: "subscription",
            image: subscription,
            url: "#",
          },
          {
            text: "comic shop locator",
            image:comicshoplocator,
            url: "#",
          },
          {
            text: "dc power visa",
            image: dcpowervisa,
            url: "#",
          },    
        ],
      }
    }

}
</script>

<style lang="scss" scoped>
  @import '../assets/style/colorPalette.scss';

  main{
    background-color: $grayBackground;

    .content{
      color: white;
      height: 100px;
      font-size: 30px;
      font-weight: bolder;
      display: flex;
      align-items: center;
    }
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
  }

</style>