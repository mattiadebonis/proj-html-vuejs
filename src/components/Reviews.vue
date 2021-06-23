<template>
    <section id="review" class="margin-page">
        <p class="title-review">What critics are saying about us</p>
        <hr>
        <!-- send reviwes to Review component-->
        <Review :publishedReviews="reviews"/>
    </section>
</template>

<script>
    import Review from "./Review"
    export default {
        name: 'App',
        data: function(){
            return{
                //reviews
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
    #review{
        .title-review{
            text-align: center;
            font-family: 'Lora', serif;
            font-size: 24px;
            color: gray;
            margin-bottom:30px;
        }
        hr{
            display: inline;
            position:absolute;
            right: 50%;
            transform:translate(50%,0);
            width: 60px;
            border: 0 ;
            background-color:lightgray;
            height: 1px;
                        
        }
    }
</style>