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
              <img v-bin:src="link.image" :alt="link.text">
              <a :href="link.url">
                {{link.text.toUpperCase()}}
              </a>
            </li>
          </ul>
        </div>
      </div>

  </main>
</template>

<script>
export default {
    name: 'Main',
    data(){
      return{
        links:[
          {
            text: "digital comics",
            image: "../assets/img/buy-comics-digital-comics.png",
            url: "#",
          },
          {
            text: "dc merchandise",
            image:"../assets/img/buy-comics-merchandise.png",
            url: "#",
          },
          {
            text: "subscription",
            image:"../assets/img/buy-comics-subscriptions.png",
            url: "#",
          },
          {
            text: "comic shop locator",
            image:"../assets/img/buy-comics-shop-locator.png",
            url: "#",
          },
          {
            text: "dc power visa",
            image:"../assets/img/buy-dc-power-visa.svg",
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
    }
  }

</style>