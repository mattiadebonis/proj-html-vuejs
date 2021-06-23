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
                    <p>{{item.author}}</p>
                    <h4>{{item.newspaper}}</h4>
                    <p>{{item.rating}}</p>
                    <p>{{item.intro}}</p>
                    <a :href="item.link">Read the article</a>
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
    
    ul{
        list-style: none;      
        display: flex;
        width: 100%;
        justify-content: center;
        li{

            color:white;
            display: inline;
            position: relative;

            .img-container{
                width: 100%;
                img{
                    width: 100%;
                }    
            }
            .text-container{
                display:inline;
                position:absolute;
                top: 0;
                right: 10px;
                padding: 50px;
            }
            
            .container-review-full{
                width:100%;
                background-color: black;

            }       
            .container-review-half{
                width:50%;
                
            }       
        }
    }
.clearfix::after {
  content: "";
  clear: both;
  display: table;
}
    

</style>