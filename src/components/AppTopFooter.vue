<script>
    export default{
        name: 'Top footer',
        data(){
            return{
                title: ['Dc comics', 'Shop', 'DC', 'Sites'],
                comics:['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News'],
                shop: ['Shop DC', 'Shop DC Collectibles'],
                dc: ['Terms Of Use', 'Privacy policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshops', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us'],
                sites: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa']
            }
        }
    }
</script>
<template>
    <div class="top_footer">
        <div class="footer_list">
            <div>
                <div>
                    <h1>{{ title[0] }}</h1>
                    <ul>
                        <li v-for="link in comics">{{ link }}</li>
                    </ul>
                </div>
                <div>
                    <h1>{{ title[1] }}</h1>
                    <ul>
                        <li v-for="link in shop">{{ link }}</li>
                    </ul>
                </div>
            </div>
            <div>
                <h1>{{ title[2] }}</h1>
                <ul>
                    <li v-for="link in dc">{{ link }}</li>
                </ul> 
            </div>
            <div>
                <h1>{{ title[3] }}</h1>
                <ul>
                    <li v-for="link in sites">{{ link }}</li>
                </ul>
            </div>
        </div>
        <div class="logo"></div>
    </div>
</template>
<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;
    .top_footer{
        height: 28.125rem;
        display: flex;
        justify-content: space-around;
        align-items: center;
        background-image: url(img/footer-bg.jpg);
        
    }
    
    .footer_list{
        display: flex;
        color: $head-bg-color;
        gap: 2.5rem;
        li{
            list-style: none;
            margin-bottom: .625rem;
            color: $footer-font-color;
        }
        h1{
            margin-bottom: 1.25rem;
            text-transform: uppercase;
        }
    }
    .logo{
        height: 28.125rem;
        width: 34.375rem;
        @include bgImage('img/dc-logo-bg.png')
    }
</style>