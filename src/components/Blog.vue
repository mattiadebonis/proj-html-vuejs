<template>
    <section class="wdt-100">
        <Post :publishedPost="posts" />
    </section>
</template>

<script>
import Post from "./Post.vue"
    export default {
        name: 'Blog',
        components: {
            Post
        },
        data: function(){
            return{
                posts : [
                    {
                        img:"sushi-1.png",
                        title:"The best coffee in town",
                        user: "admin", 
                        date: "2020-07-01",
                        category: "News"
                    },
                    {
                        img:"",
                        title:"The best coffee in town",
                        user: "admin", 
                        date: "2020-07-01",
                        category: "News"
                    },
                    {
                        img:"",
                        title:"The best coffee in town",
                        user: "admin", 
                        date: "2020-07-01",
                        category: "News"
                    }

                ]
            }
        }
    }
</script>

<style lang="scss">
  @import "../assets/styles/general.scss";
  
    
</style>
