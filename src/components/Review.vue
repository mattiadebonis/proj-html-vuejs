<template>
    <section class="margin-page">
        <ul class="reviews">
            <li v-for="(item, index) in publishedReviews" 
            :key="index">
                <img :src="componeUrlImg(item.img)" alt="">
                <p>{{item.author}}</p>
                <h4>{{item.newspaper}}</h4>
                <p>{{item.rating}}</p>
                <p>{{item.intro}}</p>
                <a :href="item.link">Read the article</a>
            </li>
        </ul>
    </section>
</template>

<script>
    
    export default {
        name: 'Review',
        props: {
            publishedReviews: Array
        },
        methods: {
            componeUrlImg : function (nameFile){
                const folder = "../assets/images/"
                var url = folder + nameFile;
                return url;
            }
        } 
    }
  
</script>

<style lang="scss">
    @import "../assets/styles/variable.scss";
    
    .reviews{
        list-style: none;            
        li{
            background-color: black;
            color:white;
            padding: 50px;
            margin:5px;
            
            img{
                width: 100px;
            }    
        }
    }
    
    

</style>