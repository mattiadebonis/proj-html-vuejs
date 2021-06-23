<template>
    <header>
        <div class="header-left"></div>
        <div class="header-right"></div>

        <div class="content-header">
            <!-- navbar -->
            <nav>
                <!-- left nav -->
                <div class="left-nav">
                    <!-- logo -->
                    <img src="../assets/images/logo-restaurant-2x.png" alt="logo">
                </div>
                <!-- /left nav -->

                <!-- right nav -->
                <div class="right-nav">
                    <!-- menu -->
                    <ul>
                        <li 
                            v-for="(item, index) in menuHeader" 
                            :key="index">{{item}}</li>
                    </ul>
                    <!-- /menu -->
                </div>
                <!-- /right nav -->
            </nav>
            <!-- /navbar -->

            <!-- jumbotron -->
            <div class="jumbotron">
                <div class="container-call">
                    <hr class="up-divider-call">
                    <p class="subtitle-call">The best table in town</p>
                    <h1 class="title-call">Fine dining experience</h1>
                    <p class="description-call">Pellentesque vitae viverra risus, sagittis. Venenatis ridiculus scelerisque nisi in urna nulla. Sit tempora a et nils, ac felis.</p>
                    <a href="#" class="button-call">explore the menu</a>
                </div>
            </div>
            <!-- /jumbotron -->
        </div>
        

        
    </header>
</template>

<script>
    export default {
        name: 'Header',
        props: {
            "menuHeader" : Array
        },
    }
</script>

<style lang="scss">
    @import "../assets/styles/general.scss";
    @import "../assets/styles/variable.scss";

    @import "../assets/styles/callToAction.scss";

    header{
        height: 525px;
        position: relative;
        color:white;

        .header-right,
        .header-left{
            display: inline-block;
            height: 100%;
        }
        .header-left{
            width: $wdt-40;
            background-color: black;
        }
        .header-right{
            width: $wdt-60;
            background-image: url("../assets/images/slider52x.jpg");
            background-size: cover;
            background-position: fixed;
            background-repeat: no-repeat;
        }
             
        .content-header{
            width: 100%;
            position: absolute;
            top: 0;

            nav{
                
                height: 100px;
                display: flex;
                align-items: center;
                
                .left-nav{
                    width: $wdt-40;
                    img{
                        height: 30px;
                        margin-left: 35px;
                    }
                }
                .right-nav{
                    width: $wdt-60;
                    ul{
                        li{
                            font-size: 10px;
                            display: inline-block;
                            margin: 10px;
                            list-style: none;
                        }
                    }
                }   
            }
            .jumbotron{
                width: $wdt-40;
                padding: 20px;
            }
        }
        
    }

</style>
