<script>
export default {
  name: "MyInformationBar",
  data() {
    return {
        informationList:[
            {
                name: "DIGITAL COMICS",
                image: "src/assets/buy-comics-digital-comics.png"
            },
            {
                name: "DC MERCHANDISE",
                image: "src/assets/buy-comics-merchandise.png"
            },
            {
                name: "SUBSCRIPTION",
                image: "src/assets/buy-comics-subscriptions.png"
            },
            {
                name: "COMIC SHOP LOCATOR",
                image: "src/assets/buy-comics-shop-locator.png"
            },
            {
                name: "DC POWER VISA",
                image: "src/assets/buy-dc-power-visa.svg"
            }
        ]
    }
}
}
</script>

<template>
    <div class="wrapper">
        <div class="container">
            <ul>
                <li v-for="(element, index) in informationList" :key="index">
                    <div class="elements-wrapper">
                        <div class="image-wrapper">
                            <img :src="element.image" alt="">
                        </div>
                        <div class="text-information">{{ element.name }}</div>
                    </div>
                </li>
            </ul>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/mixins";
@use "../style/partials/variables" as *;

    .container{
    @include mixins.container;

    }
    .wrapper{
        background-color: $primary-color;
        padding: 60px 0;
    }
    ul{
        display: flex;
        list-style: none;
        justify-content: space-between;
        
        .elements-wrapper{
            display: flex;
            align-items: center;
        
            .image-wrapper{
                height: 50px;

                img{
                    object-fit: contain;
                    height: 100% ;
                }
            }
        }
        & li:last-child .elements-wrapper img{
            height: 40px;
        }

        .text-information{
            color: white;
            padding-left: 15px;
        }
    }
</style>