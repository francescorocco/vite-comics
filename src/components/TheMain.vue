<script>
export default {
  name: "TheMain",
}
</script>

<template>
    <main>
        <div class="container">
            contenuto da inserire
        </div>
    </main>
</template>

<style scoped lang="scss">
@use "../style/partials/mixins";
    .container{
        @include mixins.container
    }

    main{
        background-color: black;
        height: 300px;
    }
</style>