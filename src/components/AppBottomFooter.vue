<script>
    export default{
        name: 'Bottom footer',
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
                <li v-for="icon in icons"><img :src="icon" alt="icon"></li>
            </ul>
        </div>
    </div>
</template>
<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
    .bottom_footer{
        background-color: $footer-color;
        display: flex;
        justify-content: space-around;
        align-items: center;
        height: 5.5rem;
        text-transform: uppercase;
    }
    .sign{
        border: .0625rem solid $main-bottom-color;
        padding: .625rem;
        color: $head-bg-color;
    }
    .follow{
        color: $main-bottom-color;
        line-height: 2.5rem;
    }
    .social{
        display: flex;
        ul{
            display: flex;
            list-style: none;
            li{
                margin-left: 1.25rem;
            }
        }
    }
</style>