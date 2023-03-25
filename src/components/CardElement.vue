<script>
    export default{
        name: 'card',
        props: {
            img: String,
            title: String
        }
    }
</script>

<template>
    <div class="cards">
        <div><img :src="img"></div>
        <h5>{{ title }}</h5>
    </div>
</template>