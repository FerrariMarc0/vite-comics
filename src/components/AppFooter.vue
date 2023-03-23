<script>
    export default{
        name: 'AppFooter',
        data(){
            return{
                title: ['Dc comics', 'Shop', 'DC', 'Sites'],
                comics:['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News'],
                shop: ['Shop DC', 'Shop DC Collectibles'],
                dc: ['Terms Of Use', 'Privacy policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshops', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us'],
                sites: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa'],
                icons:['public/fb.png', 'public/twitter.png', 'public/utube.png', 'public/pinterest.png', 'public/periscope.png']
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
        <div class="logo">
            <img src="" alt="">
        </div>
    </div>
    <div class="bottom_footer">
        <div>
            <div>
                <h2 class="sign">Sign-up now!</h2>
            </div>
        </div>
        <div class="social">
            <h2 class="follow">Follow Us</h2>
            <ul>
                <li v-for="icon in icons"><img :src="icon" alt=""></li>
            </ul>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    .top_footer{
        height: 28.125rem;
        display: flex;
        justify-content: space-around;
        align-items: center;
        background-image: url(footer-bg.jpg);
        
    }
    .bottom_footer{
        background-color: #303030;
        display: flex;
        justify-content: space-around;
        align-items: center;
        height: 5.5rem;
        text-transform: uppercase;
    }
    .footer_list{
        display: flex;
        color: #ffffff;
        gap: 2.5rem;
        li{
            list-style: none;
            margin-bottom: .625rem;
            color: #95957c;
        }
        h1{
            margin-bottom: 1.25rem;
            text-transform: uppercase;
        }
    }
    .logo{
        height: 28.125rem;
        width: 34.375rem;
        background-image: url(dc-logo-bg.png);
        background-size: 34.375rem ;
        background-repeat: no-repeat;
        overflow: hidden;
    }
    .sign{
        border: 1px solid #0282f9;
        padding: 10px;
        color: #ffffff;
    }
    .follow{
        color: #0282f9;
        line-height: 2.5rem;
    }
    .social{
        display: flex;
        ul{
            display: flex;
            list-style: none;
            li{
                margin-left: 20px;
            }
        }
    }
</style>