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
                        img:"blog92x.jpg",
                        title:"The best coffee in town",
                        user: "admin", 
                        date: "2020-07-01",
                        category: "News"
                    },
                    {
                        img:"blog72x.jpg",
                        title:"Discover our new menu",
                        user: "admin", 
                        date: "2020-07-01",
                        category: "News"
                    },
                    {
                        img:"blog82x.jpg",
                        title:"We now accept square",
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
