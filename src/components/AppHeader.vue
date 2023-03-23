<script>
    export default{
        name: 'AppHeader',
        data(){
            return {
                image: "public/dc-logo.png",
                menu: [
                    {
                        name: 'Characters',
                        target: '_blank'
                    },
                    {
                        name: 'Comics',
                        target: '_blank'
                    },
                    {
                        name: 'Movies',
                        target: '_blank'
                    },
                    {
                        name: 'Tv',
                        target: '_blank'
                    },
                    {
                        name: 'Games',
                        target: '_blank'
                    },
                    {
                        name: 'Collectibles',
                        target: '_blank'
                    },
                    {
                        name: 'Videos',
                        target: '_blank'
                    },
                    {
                        name: 'Fans',
                        target: '_blank'
                    },
                    {
                        name: 'News',
                        target: '_blank'
                    },
                    {
                        name: 'Shop',
                        target: '_blank'
                    }
                ]
            }
        }
    }
</script>

<template>
    <header>
        <div><img :src="image" alt="logo"></div>
        <div>
            <ul class="navBox">
                <li v-for="menu in menu"><a href="#" :target="menu.target">{{ menu.name }}</a></li>
            </ul>
        </div>
    </header>
</template>

<style lang="scss" scoped>
    
    *{
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    header{
        background-color: $head-bg-color;
        display: flex;
        justify-content: space-around;
        .navBox{
            display: flex;
            list-style: none;
            padding: 50px;
            
            a{
                text-decoration: none;
                padding: 0 .625rem;

            }
        }
    }
</style>