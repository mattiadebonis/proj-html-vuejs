<template>
    <footer>
        <!-- top footer -->
        <div class="top-footer">
            <div>
                <img src="../assets/images/logo-restaurant-2x.png" alt="logo-footer">
                <p>Quam eu proin sit massa condimentum. Volupat non pulvinar aliquet nunc. Quam eu proin sit massa condimentum.</p>

                <!--social buttons -->
                <ul>
                    <li><a href="#" class="social-button">
                        <i class="fab fa-facebook-f"></i></a></li>
                    <li><a href="#" class="social-button"><i class="fab fa-twitter"></i></a></li>
                    <li><a href="#" class="social-button"><i class="fab fa-youtube"></i></a></li>
                    <li><a href="#" class="social-button"><i class="fab fa-instagram"></i></a></li>
                    <li><a href="#" class="social-button"><i class="fab fa-linkedin-in"></i></a></li>
                </ul>
                <!--/social buttons -->
            </div>
        </div>
        <!-- /top footer -->

        <!-- bottom footer -->
        <div class="bottom-footer">
            <p>Copyright 2012 - 2019 avada | All Rights Reserved | Powered by <strong>Wordpress | ThemeFusion</strong></p>
        </div>
        <!-- /bottom footer -->
        
  
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
                            color: black;
                            background-color: white;
                            font-size: 12px;
                            height: 20px;
                            width: 20px;
                            padding: 15px;
                            border-radius: 50px;
                            &:hover{
                                background-color: gray;
                                transition: background-color 0.2s ease;

                            }
                            
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
