<script>
    export default{
        name: 'Main top'
    }
</script>
    <!-- JUMBOTRON -->
<template>
    <div class="top_main"></div>
</template>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
    .top_main{
        height: 25.25rem;
        display: flex;
        align-items: center;
        color: $head-bg-color;
        background-image: url("public/img/jumbotron.jpg");
        h1{
            margin-left: 15.625rem;
        }
    }
</style>