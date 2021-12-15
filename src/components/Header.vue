<template>
    <header>

        <div class="topHeaderMenu">
            <div class="obliqueSquare" v-for="(item, index) in dataHeaderTop" :key="index">
                <a :href="item.link"><img :src="item.img"  :alt="index"></a>
            </div>
        </div>

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

            dataHeaderTop:[
                {
                    link:"https://www.dcuniverseinfinite.com",
                    img: "https://upload.wikimedia.org/wikipedia/commons/3/3d/DC_Comics_logo.svg",
                },
                {
                    link: "https://www.dcuniverseinfinite.com/?_ga=2.78271380.1495375928.1639472812-5255609.1639472812",
                    img: "https://www.dccomics.com/sites/all/themes/dc_comics_bp/images/DCUI_desktop.svg",
                },
                {
                    link: "https://shop.dccomics.com",
                    img: "https://www.dccomics.com/sites/all/themes/dc_comics_bp/images/DC_SHOP_desktop.svg",
                },
                {
                    link:"https://community.dcuniverseinfinite.com",
                    img:"https://www.dccomics.com/sites/all/themes/dc_comics_bp/images/DC_community.svg",
                },
                {
                    link:"https://www.hbomax.com/hub/dc?utm_source=dccomics&utm_medium=nav&utm_campaign=dcglobalnav",
                    img:"https://www.dccomics.com/sites/all/themes/dc_comics_bp/images/DC_on_HBOMAX_desktop.svg",
                },
            ],

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

        // *** START SECTION TOP HEADER *** 
        .topHeaderMenu{
            background-color: $blueDC;
            display: flex;
            justify-content: flex-end;
            align-items: center;

            .obliqueSquare:first-child{
                background-color: white;
            }
            
            .obliqueSquare{
                display: flex;
                align-items: center;
                justify-content: center;
                height: 40px;
                width: 180px;
                transform: skewX(-15deg);
                
                &:hover:not(:first-child){
                    background-color: #3797F6;
                }

                img{
                    transform: skewX(15deg);
                    height: 25px;
                    object-fit: cover;
                }
            }

            .obliqueSquare:not(:last-child){
                border-right: 1px solid #3797F6;
            }
        }
        // *** STOP SECTION TOP HEADER *** 

        .container{
            height: 115px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }


        nav{
            height: 100%;

            ul {
                height: 100%;

                li{
                    display: inline-block;
                    height: 100%;
                    line-height: 115px;


                    &:hover {
                    border-bottom: solid 5px $blueDC;  
                    transition: transform 300ms ;

                    &:hover a{
                        color: $blueDC;
                    }
                }
                    
                    a {
                        color: black;
                        font-weight: bold;
                        margin: 0 20px;
                    }
                }
            }
        }

    }
</style>