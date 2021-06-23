<template>
    <main class="wdt-100">
        <Summary />
        <!-- send data to first call to action -->
        <CallToAction :item ="callMenu" />
        <Reviews />
        <Gallery />
        <Blog />
        <!-- send data to the second call to action -->
        <CallToAction :item="callDelivery" />
        <Menus />
        <Dish />
    </main>
</template>

<script>
import Summary from"./Summary.vue";
import CallToAction from "./CallToAction.vue";
import Reviews from "./Reviews.vue";
import Gallery from "./Gallery.vue";
import Blog from "./Blog.vue";
import Menus from "./Menus.vue";
import Dish from "./Dish.vue";


    export default {
        name: 'Main',
        components:{
            Summary,
            CallToAction,
            Reviews,
            Gallery,
            Blog,
            Menus,
            Dish
        },
        data: function(){
            return{
                //data first call to action
                callMenu: {
                    img:"slider32x.jpg",
                    title: "The best table in town",
                    subtitle: "Fine dining experience",
                    description: "Pellentesque vitae viverra risus, sagittis. Venenatis ridiculus scelerisque nisi in urna nulla. Sit tempora a et nils, ac felis.",
                    button: "explore the menu"
                },
                //data first second to action
                callDelivery: {
                    img:"slider72x-scaled.jpg",
                    title: "Enjoy your meal at home",
                    subtitle: "Takeout now available",
                    description: "Pellentesque vitae viverra risus, sagittis. Venenatis ridiculus scelerisque nisi in urna nulla non arcu noris tortor.",
                    button: "View Takeout menu"
                }
            }
        }

    }
</script>

<style lang="scss">
  @import "../assets/styles/general.scss";
  
</style>
