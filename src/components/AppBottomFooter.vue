<script>
    export default{
        name: 'AppBottomFooter',
        data(){
            return{
                icons:['public/img/fb.png', 'public/img/twitter.png', 'public/img/utube.png', 'public/img/pinterest.png', 'public/img/periscope.png']
            }
        }
    }
</script>
<template>
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
    .bottom_footer{
        background-color: #303030;
        display: flex;
        justify-content: space-around;
        align-items: center;
        height: 5.5rem;
        text-transform: uppercase;
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