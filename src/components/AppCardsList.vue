<script>
import CardElement from './CardElement.vue';
    export default{
        name: 'Cards list',
        components: {
                    CardElement
                },
        data(){
            return {
                
                products: [
                    {
                        src: "https://fastly.picsum.photos/id/406/200/200.jpg?hmac=RkvoDL29GdYFLEDajHXtCCieqAjWVp9vl__A-D6bddw",
                        price: "$19.99",
                        series: "Action Comics",
                        type: "comic book"
                    },
                    {
                        src: "https://fastly.picsum.photos/id/638/200/200.jpg?hmac=64UpQ4ouFUNEG9cnXLQ9GxchDShg-mL1rdCrZGfc94U",
                        price: "$3.99",
                        series: "American Vampire 1976",
                        type: "comic book"
                    },
                    {
                        src: "https://fastly.picsum.photos/id/478/200/200.jpg?hmac=YfKBYcZHT991lmrKfB0pYNaztmUvQecXbVrc5V4mj8E",
                        price: "$16.99",
                        series: "Aquaman",
                        type: "graphic novel"
                    },
                    {
                        src: "https://fastly.picsum.photos/id/612/200/200.jpg?hmac=HbIkwJ0QBqhSlGTi3bnF4JFTp9BntF-teQZUQhpqWyM",
                        price: "$2.99",
                        series: "Batgirl",
                        type: "comic book"
                    },
                    {
                        src: "https://fastly.picsum.photos/id/54/200/200.jpg?hmac=-2_HX5umbAEVPP9CokmPW3Kc8V9iDplneKlS73LWdQQ",
                        price: "$3.99",
                        series: "Batman",
                        type: "comic book"
                    },
                    {
                        src: "https://fastly.picsum.photos/id/910/200/200.jpg?hmac=5y7FBcwrEQLaT1hO3VufjbQNxx_eg-znDlA1JclTpDQ",
                        price: "$2.99",
                        series: "Batman Beyond",
                        type: "comic book"
                    },
                    {
                        src: "https://fastly.picsum.photos/id/596/200/200.jpg?hmac=TiMsstBNF6YKq9Gn7QGsihITEUcv_O8QuTXEVR3T6GA",
                        price: "$3.99",
                        series: "Batman/Superman",
                        type: "comic book"
                    },
                    {
                        src: "https://fastly.picsum.photos/id/24/200/200.jpg?hmac=Tw5b43UPAehS5e4JyB0qMQysvfLBmu_GZ_iafWou3m8",
                        price: "$4.99",
                        series: "Batman/Superman Annual",
                        type: "comic book"
                    },
                    {
                        src: "https://fastly.picsum.photos/id/399/200/200.jpg?hmac=LCWCFY16G50iBPpqU6-FCw79ovEqvznYsxoQNCIldV8",
                        price: "$5.99",
                        series: "Batman: The Joker War Zone",
                        type: "comic book"
                    },
                    {
                        src: "https://fastly.picsum.photos/id/137/200/200.jpg?hmac=qhNK8PzcRQJaCJlGEj1q5ceRIkKkfPmVuOwE5ZInXA8",
                        price: "$6.99",
                        series: "Batman: Three Jokers",
                        type: "comic book"
                    },
                    {
                        src: "https://fastly.picsum.photos/id/257/200/200.jpg?hmac=k0qf_n518If39xOB7qmdqgZZNQ38WdbfQXdF30TSPCw",
                        price: "$4.99",
                        series: "Batman: White Knight Presents: Harley Quinn",
                        type: "comic book"
                    },
                    {
                        src: "https://fastly.picsum.photos/id/113/200/200.jpg?hmac=lMncqLZmsXtr3D92sy1GU_2v-kwHOS-UW2iS5p98WMU",
                        price: "$16.99",
                        series: "Catwoman",
                        type: "graphic novel"
                    }
                ]
            }
        }
    }
</script>

<template>
    <section>
        <div class="current">
            <span>Current Series</span>
        </div>
        <div>
            <div class="card_container">
                <CardElement class="cards" v-for="item in products" 
                :img="item.src" 
                :title="item.series"/>
            </div>
            
        </div>
        <button class="btn">Load More</button>
    </section>
</template>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
    section{
        position: relative;
        background-color: $main-top-color;
        padding: 3.125rem 0 1.875rem 0;
        text-align: center;
        .card_container{
            width: 70%;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: center;
            margin: 0 auto;
            gap: 3.125rem 0;
            .cards{
                flex-basis: calc(100% / 6);
                color: $head-bg-color;
                text-transform: uppercase;
                text-align: start;
                :deep(img){
                    margin-bottom: .625rem;
                }
            }
        }
        button, .current{
            width: 11.5625rem;
            padding: .625rem 0;
            font-weight: 600;
            text-transform: uppercase;
            color: $head-bg-color;
            background-color: $main-bottom-color;
            border: none;
            
        }
        .btn{
            margin-top: 4.375rem;
            cursor: pointer;
        }
        .current{
            position: absolute;
            top: -1.25rem;
            left: 15.625rem;
        }
    }

    
</style>
