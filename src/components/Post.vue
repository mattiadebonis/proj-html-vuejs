<template>
    <section id="blog" class="wdt-100 margin-page">

        <p>Lastest news e promotions</p>
        <hr>
        <ul class="flex">
            <li 
                v-for="(item,index) in publishedPost"
                :key="index"
            >
                <img :src="componeUrlImg(item.img)" alt="">
                <h4>{{item.title}}</h4>
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
                const folder = "../assets/images/"
                var url = folder + nameFile;
                return url;
            }
        } 
        
    }
</script>

<style lang="scss">
  @import "../assets/styles/general.scss";

    #blog{
        text-align: center;
        p{
            font-size: 24px;
        }
        hr{
            width: 100px;
            margin: 30px auto;
        }
        ul{
            list-style: none;
            li{
                margin: 0 20px;
                img{
                    height: 400px;
                }
                p{
                    font-size: 12px;
                    color: gray;
                }
            }
        }
    }
  
    
</style>
