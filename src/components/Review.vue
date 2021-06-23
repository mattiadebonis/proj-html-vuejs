<template>
    <section class="margin-page">
        
        <ul>
            <!-- review -->
            <li 
                v-for="(item, index) in publishedReviews" 
                :key="index"
                :class="isFull(item.fullWidth)"
            >
                <!-- img container -->
                <div class="img-container">
                    <img :src="componeUrlImg(item.img)" alt="">
                </div>
                <!-- /img container -->

                <!-- text container -->
                <div class="text-container">
                    <div class="container-call">
                        <p class="subtitle-call">{{item.author}}</p>
                        <h3>{{item.newspaper}}</h3>
                        <i
                            v-for= "(n,index) in 5"
                            :key= "index" 
                            class="fas fa-star"
                            :class="getRating(item.rating,index)"
                        ></i>
                        <hr>

                        <p class="description-call description-review">{{item.intro}}</p>
                        
                        <a :href="item.link" class="button-call button-review">Read the article</a>
                    </div>
                </div>
                <!-- /text container -->       
            </li>
            <!-- review -->
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
                return require("../assets/images/"+ nameFile);
            },
            isFull : function(full){
                if(full==true){
                    return "container-review-full"
                }else{
                    return "container-review-half"
                }
            },
            getRating : function(ratingTen, index){
                //get five star rating
                var ratingFive = (ratingTen/2).toFixed(0);
                if (index <= ratingFive){
                    return "star_yellow"
                }else{
                    return "star_none";
                }
            }
        } 
    }
  
</script>

<style lang="scss">
    @import "../assets/styles/variable.scss";
    @import "../assets/styles/callToAction.scss";

    
    ul{
        list-style: none;      
        width: 100%;
        justify-content: center;
        color:white;

        li{
            margin: 0 20px 20px 0;
            position: relative;
            .img-container{
                img{
                    width: 100%;
                }
            }
            .text-container{
                display:inline;
                position:absolute;
                top: 0;
                right: 10px; 
                padding: 40px 25px; 
                
                i{
                    font-size: 10px;
                    margin: 20px 3px 0 0;
                }

                hr{
                    left: 0;
                    width: 60px;
                    border: 0;
                    margin-left: 45px;
                    background-color:lightgray;
                    height: 1px; 
                }

                .description-review,
                .button-review{
                    //bugfix
                    margin-left: 0px;
                    font-size: 11px;
                }    
                
            } 
        }
        
        .container-review-full{
            width: calc(100% - 20px);
            background-color: black;
            display: block;
            .text-container{
                width: 50%;
            }
            .img-container{
                width:50%;
                height: 100%;
                
            }
        }       
        .container-review-half{
            width: calc(50% - 20px);

            flex: wrap;
            display: inline-block;
            .img-container{
                width:100%;
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
            
        }
    }
</style>