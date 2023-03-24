<script>
    export default{
    name: 'AppHeader',
    data(){
        return {
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
        <div><img src="public/img/dc-logo.png" alt="logo"></div>
        <div>
            <ul class="navBox">
                <li v-for="menu in menu"><a href="#" :target="menu.target">{{ menu.name }}</a></li>
            </ul>
        </div>
    </header>
</template>
<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
    header{
        height: 7.375rem;
        background-color: $head-bg-color;
        display: flex;
        justify-content: space-around;
        align-items: center;
        text-transform: uppercase;
        .navBox{
            display: flex;
            list-style: none;
            padding: 50px;
            
            a{
                padding: 45px .625rem;
                color: #6f4646;
                font-weight: 800;
                &:hover{
                    color: $main-bottom-color;
                    border-bottom: 4px solid $main-bottom-color;
                }
                
            }
        }
    }
    
</style>