<template>
    <footer>
        <div class="top-footer">
            <div>
                <img src="../assets/images/logo-restaurant-2x.png" alt="logo-footer">
                <p>Quam eu proin sit massa condimentum. Volupat non pulvinar aliquet nunc. Quam eu proin sit massa condimentum.</p>
                <ul>
                    <li><a href="#" class="social-button">F</a></li>
                    <li><a href="#" class="social-button">T</a></li>
                    <li><a href="#" class="social-button">Y</a></li>
                    <li><a href="#" class="social-button">I</a></li>
                    <li><a href="#" class="social-button">L</a></li>
                </ul>

            </div>
            

        </div>
        <div class="bottom-footer">
            <p>Copyright 2012 - 2019 avada | All Rights Reserved | Powered by <strong>Wordpress | ThemeFusion</strong></p>
        </div>
        
  
    </footer>
</template>

<script>
    export default {
        name: 'Footer',
    }

</script>

<style lang="scss">
  @import "../assets/styles/general.scss";
    footer{
        width: 100%;
        height: 600px;
        .top-footer{
            position: relative;
            width: 100%;
            height: 500px;
            background-image: linear-gradient(to bottom, black, rgba(0,0,0,0.5)), url("../assets/images/slider52x.jpg");
            background-size: contain;
            div{
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
                text-align: center;
                color: lightgray;
                line-height:30px;
                padding: 40px;

                img{
                    height: 60px;
                    margin-bottom: 30px;
                }
                ul{
                    list-style: none;
                    margin: 30px;
                    li{
                        display: inline;
                        .social-button{
                            background-color: white;
                            height: 15px;
                            width: 15px;
                            margin: 20px;
                            padding: 15px;
                            border-radius: 100px;
                            
                        }
                    }
                    
                }
                
            }
        }
        .bottom-footer{
            width: 100%;
            height: 100px;
            background-color: black;
            position: relative;
            text-align:center;
            p{
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
                color:lightgray;
                font-size: 14px;
            }

        }
        

      
        
    }


</style>
