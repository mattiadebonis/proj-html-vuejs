<template>
    <section id="blog" class="wdt-100 ">

        <p>Lastest news e promotions</p>
        <hr>
        <ul class="flex">
            <li 
                v-for="(item,index) in publishedPost"
                :key="index"
            >
                <img :src="componeUrlImg(item.img)" alt="">
                <h4 class="title-post">{{item.title}}</h4>
                <p>By {{item.user}} | {{item.date}} | Categories {{item.category}}</p>    
            </li>
        </ul>

    </section>
</template>

<script>
    export default {
        name: 'Post',
        props: {
            publishedPost: Array
        },
        methods: {
            componeUrlImg : function (nameFile){
                return require("../assets/images/"+ nameFile);

            }
        } 
        
    }
</script>

<style lang="scss">
  @import "../assets/styles/general.scss";

    #blog{
        width:100%;
        text-align: center;
        padding: 60px;
        p{
            font-size: 24px;
        }
        hr{
            width: 70px;
            margin: 30px auto;
            border-color: lightgray;
        }
        ul{
            list-style: none;
            li{
                color: black;
                margin: 0 20px;
                .title-post{
                    margin: 22px 0 8px;
                }
                img{
                    width: 240px;
                    height:350px;
                    object-fit: cover;
                }
                p{
                    font-size: 12px;
                    color: gray;
                }
            }
        }
    }
  
    
</style>
