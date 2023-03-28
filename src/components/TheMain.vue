<script>
import PersonalCard from './PersonalCard.vue'

export default {
  name: "TheMain",
  components: {
    PersonalCard
  },
    data() {
      return {
        seriesList:[
            {
                "thumb": "https://static.dc.com/2023-03/LEGIONOB_Cv1_00111_DIGITAL.jpg?w=640",
                "price": "$19.99",
                "series": "Action Comics",
                "type": "comic book"
            },
            {
                "thumb": "https://static.dc.com/2023-03/BA_Cv9_00911_DIGITAL.jpg?w=640",
                "price": "$3.99",
                "series": "American Vampire 1976",
                "type": "comic book"
            },
            {
                "thumb": "https://static.dc.com/2023-03/ST_GH_Cv3_00311_DIGITAL.jpg?w=640",
                "price": "$16.99",
                "series": "Aquaman",
                "type": "graphic novel"
            },
            {
                "thumb": "https://static.dc.com/2023-03/MS30A_Cv1_00111_DIGITAL.jpg?w=640",
                "price": "$2.99",
                "series": "Batgirl",
                "type": "comic book"
            },
            {
                "thumb": "https://static.dc.com/2023-03/MS30A_Cv1_00111_DIGITAL.jpg?w=640", 
                "price": "$3.99",
                "series": "Batman",
                "type": "comic book"
            },
            {
                "thumb": "https://static.dc.com/2023-03/BMSMWF_Cv13_01311_DIGITAL.jpg?w=640",
                "price": "$2.99",
                "series": "Batman Beyond",
                "type": "comic book"
            },
            {
                "thumb": "https://static.dc.com/2023-03/NTW_Cv102_10211_DIGITAL-1.jpg?w=640",
                "price": "$3.99",
                "series": "Batman/Superman",
                "type": "comic book"
            },
            {
                "thumb": "https://static.dc.com/2023-03/FLS_Cv795_79511_DIGITAL.jpg?w=640",
                "price": "$4.99",
                "series": "Batman/Superman Annual",
                "type": "comic book"
            },
            {
                "thumb": "https://static.dc.com/2023-03/DCConnect_35-CVR.jpg?w=640",
                "price": "$5.99",
                "series": "Batman: The Joker War Zone",
                "type": "comic book"
            },
            {
                "thumb": "https://static.dc.com/2023-03/ROBIN_v3%20%28Cover%29.jpg?w=640",
                "price": "$6.99",
                "series": "Batman: Three Jokers",
                "type": "comic book"
            },
            {
                "thumb": "https://static.dc.com/2023-03/LP-ROTG_Cv1_00111_DIGITAL.jpg?w=640",
                "price": "$4.99",
                "series": "Batman: White Knight Presents: Harley Quinn",
                "type": "comic book"
            },
            {
                "thumb": "https://static.dc.com/2023-03/SM_LOST_Cv1_00111_DIGITAL.jpg?w=640",
                "price": "$16.99",
                "series": "Catwoman",
                "type": "graphic novel"
            }
        ]
      }
    }
}
</script>

<template>
    <main>
        <div class="container">
            <button class="btn-current-series">Current Series</button>
            <div v-for="(element, index) in seriesList" class="card-wrapper" :key="index">
                <PersonalCard :image="element.thumb" :name="element.series"/>
            </div>
        </div>
        
        <button class="btn-leade-more">Lead More</button>

    </main>
</template>

<style scoped lang="scss">
@use "../style/partials/mixins";
@use "../style/partials/variables" as *;

    .container{
        @include mixins.container;
        position: relative;
        
    }

    main{
        background-color: black;
        text-align: center;
    }

    .container{
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        padding: 50px 0 150px 0;

        .card-wrapper{
            width: calc(100% / 6 - 5px);
            margin: 30px 0;
        }
    }
    button {
    background-color: $primary-color;
    border: none;
    padding: 10px 39px;
    font-size: 18px;
    color: white;
    margin-bottom: 30px;
    }

    .btn-current-series{
    position: absolute;
    left: -1%;
    top: -4%;
    font-size: 30px;
    font-weight: 800;
}
</style>