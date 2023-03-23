<script>
    export default{
        name: 'AppMain',
        data(){
            return{
                items:[
                    {
                        image: "public/buy-comics-digital-comics.png",
                        text: "Digital Comics"
                    },
                    {
                        image: "public/buy-comics-merchandise.png",
                        text: 'DC Merchandise'
                    },
                    {
                        image: "public/buy-comics-subscriptions.png",
                        text: 'Subscription'
                    }
                    ,
                    {
                        image: "public/buy-comics-shop-locator.png",
                        text: "Comic Shop Locator"
                    },
                    {
                        image: "public/buy-dc-power-visa.svg",
                        text: "DC Power Visa"
                    }
                ]
            }
        }
    }
</script>

<template>
    <div class="top_main">
        <h1> Content goes here </h1>
    </div>
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
    .top_main{
        display: flex;
        align-items: center;
        height: 134px;
        background-color: #1c1c1c;
        color: #ffffff;
        h1{
            margin-left: 15.625rem;
        }
    }
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