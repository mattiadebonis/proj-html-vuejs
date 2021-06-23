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
                        <p>{{item.rating}}</p>
                        <p>{{item.intro}}</p>
                        <a :href="item.link">Read the article</a>
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
            margin: 0 15px 15px 0;
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
            } 
        }
        
        .container-review-full{
            width: calc(100% - 15px);
            background-color: black;
            display: block;
            .text-container{
                width: 50%;
            }
            .img-container{
                width:50%;
                
            }
        }       
        .container-review-half{
            width: calc(50% - 15px);

            flex: wrap;
            display: inline-block;
            .img-container{
                width:100%;
            }
        }
    }
.clearfix::after {
  content: "";
  clear: both;
  display: table;
}
    

</style>