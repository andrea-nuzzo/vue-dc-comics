<template>
  <header>
      <div class="container">
        <div class="logo">
            <img src="../assets/img/dc-logo.png" alt="">
        </div>

        <nav>
            <ul>
                <li v-for="(link, index) in links" :key="index"><a :href="links.url">{{link.text}}</a></li>

            </ul>
        </nav>
      </div>
  </header>
</template>

<script>
export default {
    name: 'Header',
    data() {
        return{

            links: [ 
                {
                text: "characters",
                url: "#",
                current: false,
                },

                {
                text: "comics",
                url: "#",
                current: true,
                },

                {
                text: "movies",
                url: "#",
                current: false,
                },

                {
                text: "tv",
                url: "#",
                current: false,
                },

                {
                text: "games",
                url: "#",
                current: false,
                },

                {
                text: "collectibles",
                url: "#",
                current: false,
                },

                {
                text: "Characters",
                url: "#",
                current: false,
                },

                {
                text: "videos",
                url: "#",
                current: false,
                },

                {
                text: "fans",
                url: "#",
                current: false,
                },

                {
                text: "news",
                url: "#",
                current: false,
                },

                {
                text: "shop",
                url: "#",
                current: false,
                },
            ]
        }
    }

}
</script>

<style lang="scss" scope>
    @import '../assets/style/colorPalette.scss';
    header{
        height: 90px;

        .container {
            display: flex;
        }
        img{
            width: 60px;
        };

        border: 1px solid $blueDC;
    }
</style>