<script>
export default {
  name: "TheFooter",
  data() {
    return {
        foorterLiks:[
            {
                name: "DC COMICS",
                links:[
                    "Characters",
                    "Comics",
                    "Movies",
                    "TV",
                    "Games",
                    "Videos",
                    "News"
                ]
            },
            {
                name: "SHOP",
                links: [
                    "Shop DC",
                    "Shop DC Collectibles"
                ]
            },
            {
                name: "DC",
                links: [
                    "Terms Of Use",
                    "Privacy policy(New)",
                    "Ad Choices",
                    "Advertising",
                    "Jobs",
                    "Subscriptions",
                    "Talent Workshops",
                    "CPSC Certificates",
                    "Ratings",
                    "Shop Help",
                    "Contact Us"
                ]
            },
            {
                name: "SITES",
                links: [
                    "DC",
                    "MAD Magazine",
                    "DC Kids",
                    "DC Universe",
                    "DC Power Vista"
                ]
            }
        ],
        followUsLinks: [
            "footer-facebook.png",
            "footer-periscope.png",
            "footer-pinterest.png",
            "footer-twitter.png",
            "footer-youtube.png"
        ]
    }
},
methods: {
    getImagePath: function(image){
        return new URL(`../assets/${image}`, import.meta.url).href;
    }
}
}    

</script>


<template>
    <footer>
        <div class="container">
            <ul class="links-wrapper">
                <li class="list-name" v-for="element in foorterLiks">
                    {{element.name}}
                    <ul>
                        <li v-for="link in element.links">
                            <a class="links" href="#">{{ link }}</a>
                        </li>
                    </ul>
                </li>
            </ul>
            <div class="img-wrapper">
                <img class="blu-img" src="../assets/dc-logo-bg.png" alt="">
            </div>
        </div>
        <div class="bottom-footer">
            <div class="container">
                <button class="sign-up">SIGN-UP NOW</button>
                <ul>
                    <li class="follow-text">FOOLOW US</li>
                    <li v-for="element in followUsLinks"><img :src="getImagePath(element)" alt=""></li>
                </ul>
            </div>
        </div>
    </footer>
</template>



<style scoped lang="scss">
@use "../style/partials/variables" as *;
@use "../style/partials/mixins";


    .container{
        @include mixins.d-flex;
        @include mixins.container;
        justify-content: space-between;
        height: 400px;
        overflow-y: hidden;
    }
    footer{
        background-image: url(../assets/footer-bg.jpg);
        height: 400px;
        background-size: cover;
    }

    .links-wrapper{
        @include mixins.d-flex;
        flex-direction: column;
        list-style: none;
        flex-wrap: wrap;
        height: 400px;
        
        .list-name{
            color: white;
            padding: 0 55px 35px 0;
            font-weight: bolder;
            font-size: 25px;
        }
        ul{
            list-style: none;
            .links{
                text-decoration: none;
                color:gray;
                font-size: 14px;
            }
        }
    }

    .img-wrapper{
        overflow-y: hidden;
        
        img{
            transform: translateY(-15%);
        }
    }

    .bottom-footer{
        height: 100px;
        width: 100%;
        background-color: $bottom-footer-color;
        
        .container{
            align-items: center;
            height: 100%;
        }

        .sign-up{
            background-color: transparent;
            padding: 12px 18px;
            border: 3px solid $primary-color;
            color: white;
            font-size: 18px;
        }

        ul{
                display: flex;
                list-style: none;
                align-items: center;
                li{
                    padding:10px;
                }
            }
        .follow-text{
            color: $primary-color;
            font-size: 20px;
            font-weight: 600;
        }
    }
</style>