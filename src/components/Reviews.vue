<template>
    <section class="margin-page">
        <Review :publishedReviews="reviews"/>
    </section>
</template>

<script>
    import Review from "./Review"
    export default {
        name: 'App',
        data: function(){
            return{
            reviews : [
                {
                    author:"Meggy Stewart",
                    newspaper: "New York Times",
                    rating:5,
                    intro: "Non arcu mauris tortor ultrices mollis tellus eusmod fermentum. Habitant amet tincidunt id sapien accumsan sed at. Mmalesuada ullamcorper amet.Pretium pretium dignissim nisi.",
                    img:"blog72x.jpg",
                    link:"#",
                    fullWidth: true
                },
                {
                    author:"Mary Maxey",
                    newspaper: "The Guardian",
                    rating:5,
                    intro: "Non arcu mauris tortor ultrices mollis tellus eusmod fermentum. Habitant amet tincidunt id sapien accumsan sed.",
                    img:"info52x.jpg",
                    link:"#",
                    fullWidth: false

                },
                {
                    author:"Patrick Monroe",
                    newspaper: "Globe and mail",
                    rating:5,
                    intro: "Vivamus magna justo, lacinia eget consectetur sed, convallis at tellus . Nulla porttitor accusan tincidunt.",
                    img:"info12x.jpg",
                    link:"#",
                    fullWidth: false

                },
            ]
            }
        },
        components: {
            Review
        }
}
</script>

<style lang="scss">
    @import "../assets/styles/variable.scss";
    

</style>