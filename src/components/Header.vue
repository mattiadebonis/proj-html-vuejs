<template>
    <header>
        <div class="header-left">


        </div>
        <div class="header-right"></div>
            
        <!-- navbar -->
        <nav>
            <!-- logo -->
            <img src="../assets/images/logo-restaurant-2x.png" alt="logo">
            <!-- logo -->

            <!-- menu -->
            <ul>
                <li 
                    v-for="(item, index) in menuHeader" 
                    :key="index">{{item}}</li>

            </ul>

            <!-- /menu -->

        </nav>
        <!-- /navbar -->

        <!-- jumbotron -->
        <div class="jumbotron">
        

        </div>
        <!-- /jumbotron -->
    </header>
</template>

<script>

    export default {
        name: 'Header',
        props: {
            "menuHeader" : Array
        }
    }
</script>

<style lang="scss">
  @import "../assets/styles/general.scss";
    header{
        height: 500px;
        

        .header-right,
        .header-left{
            display: inline-block;
            width:50%;
            height: 100%;
        }
        .header-left{
            background-color: black;
        }
        .header-right{
            background-image: url("../assets/images/slider52x.jpg");
            background-size: cover;
            background-position: fixed;
            background-repeat: no-repeat;
        }
        
        nav{
            position: absolute;
            top: 0;
            display: flex;
            justify-content: space-between;
            img{
                height: 50px;
            }
            ul{
                li{
                    display: inline-block;
                    margin: 10px;
                    list-style: none;
                }
            }
        }
    }
    .flex{
        display: flex;
    }

</style>
