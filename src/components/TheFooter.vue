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
        <ul class="links-wrapper">
            <li v-for="(element, index) in foorterLiks">
                {{element.name}}
                <ul>
                    <li v-for="link in foorterLiks.links">{{ link }}</li>
                </ul>
            </div>
        </div>
    </footer>
</template>



<style scoped lang="scss">
@use "../style/partials/variables" as *;
@use "../style/partials/mixins";

    footer{
        background-image: url(../assets/footer-bg.jpg);
        height: 370px;
        padding: 20px 50px;
    }

    .links-wrapper{
        @include mixins.d-flex;
        flex-direction: column;
        list-style: none;
        flex-wrap: wrap;
        height: 400px;
        

        li{
            color: white;
            padding: 0 55px 35px 0;
            font-weight: bolder;
            font-size: 25px;
        }
    }

</style>