<template>
    <section id="blog" class="wdt-100 ">

        <p>Lastest news & promotions</p>
        <hr>
        <ul class="flex">
            <li 
                v-for="(item,index) in publishedPost"
                :key="index"
            >
                <img :src="componeUrlImg(item.img)" alt="">
                <h4 class="title-post">{{item.title}}</h4>
                <p class="info-post">By {{item.user}} | {{item.date}} | Categories {{item.category}}</p>    
                <p class="info-post-hover">{{item.category}}</p>    
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
            color:gray;
            font-family: 'Lora', serif;
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
                .info-post-hover{
                    display: none;
                }
                &:hover{
                    position:relative;
                    img{
                        width:100%;
                        height:100%;
                        &:after{
                            content: '';
                            position: absolute;
                            top: 0;
                            left: 0;
                            right: 0;
                            bottom: 0;
                            background: linear-gradient(to top, transparent 0%, black 100%);
                        }
                    }
                    .title-post,
                    .info-post-hover{
                        position:absolute;
                        top: 50%;
                        left:50%;
                        transform: translate(-50%, -50%);
                        color: white;
                    }
                    .title-post{
                        font-size: 24px;
                    }
                    .info-post-hover{
                        display: inline;
                    }
                    .info-post{
                        display: none;
                        
                    }
                }
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
