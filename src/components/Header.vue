<template>
    <header>

        <div class="container">
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="">
            </div>

            <nav>
                <ul>
                    <li v-for="(link, index) in links" :key="index">
                        <a :href="link.url">{{link.text.toUpperCase()}}</a>
                    </li>
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

        .container{
            height: 90px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        img{
            width: 60px;
        }

        ul {
            display: flex;

            li{
                list-style: none;
                border: 1px solid red;
                a {
                    text-decoration: none;
                    color: black;
                    font-weight: bold;
                    margin: 0 20px;
                    border: 1px solid black;
                }
            }
        }

        border: 1px solid $blueDC;
    }
</style>