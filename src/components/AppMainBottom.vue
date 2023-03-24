<script>
    export default{
        name: 'AppMainBottom',
        data(){
            return{
                items:[
                    {
                        image: "public/img/buy-comics-digital-comics.png",
                        text: "Digital Comics"
                    },
                    {
                        image: "public/img/buy-comics-merchandise.png",
                        text: 'DC Merchandise'
                    },
                    {
                        image: "public/img/buy-comics-subscriptions.png",
                        text: 'Subscription'
                    }
                    ,
                    {
                        image: "public/img/buy-comics-shop-locator.png",
                        text: "Comic Shop Locator"
                    },
                    {
                        image: "public/img/buy-dc-power-visa.svg",
                        text: "DC Power Visa"
                    }
                ]
            }
        }
    }
</script>

<template>
    <div class="bottom_main">
        <ul>
            <li v-for="item in items">
                <img :src="item.image" alt="image">
                <span>{{item.text}}</span>
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
    .bottom_main{
        background-color: #0282f9;
        display: flex;
        justify-content: center;
        padding: 50px;
        text-transform: uppercase;
        ul{
            display: flex;
            li{
                list-style: none;
                display: flex;
                align-items: center;
                padding: 0 40px;
                img{
                    height: 57px;
                }
                span{
                    padding-left: 10px;
                    color: #ffffff;
                }
            }
        }
    }
</style>