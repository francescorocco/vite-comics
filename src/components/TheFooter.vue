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
            "fa-brands fa-facebook-f",
            "fa-brands fa-twitter",
            "fa-brands fa-youtube",
            "fa-brands fa-pinterest-p",
            "fa-solid fa-location-dot"
        ]
    }
}}
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
        </div>
        <div class="bottom-footer">
            <div class="container">
                <button class="sign-up">SIGN-UP NOW</button>
                <ul>
                    <li>FOOLOW US</li>
                    <li v-for="element in followUsLinks" :key="element"><i :class="element"></i></li>
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
    }
    footer{
        background-image: url(../assets/footer-bg.jpg);
        height: 500px;
        background-size: cover;
        position: relative
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

                li{
                    padding: 10px;
                    background-color: white;
                    border-radius: 50%;
                    color :red;
                }
            }        
    }
</style>