<script>
export default {
  name: "TheHeader",
  data() {
    return {
        navbarLinks:[
            "CHARACTERS",
            "COMICS",
            "MOVIES",
            "TV",
            "GAMES",
            "CELECTIBLES",
            "VIDEOS",
            "FANS",
            "NEWS",
            "SHOP"

        ]
    }
}}
</script>

<template>

<header>
    <div>
        <img src="../assets/dc-logo.png" alt=" ">
    </div>
    <nav>
        <ul>
            <li v-for="element in navbarLinks">
                <a class="nav-links" href="#">{{element}}</a>
            </li>
        </ul>
    </nav>
</header>

</template>


<style scoped lang="scss">
@use "../style/partials/mixins";

header{
    @include mixins.container;
    @include mixins.d-flex-a-center;
    justify-content: space-between;
    height: 170px;
}

ul{
    @include mixins.d-flex;
    list-style: none;
    padding: 10px 20px;

    .nav-links{
        color: black;
        text-decoration: none;
        padding: 10px 20px;
        font-weight: 600;
    }
}
</style>