<template>
    <section id="menu" class="flex">
        
            <div 
                v-for="(menu,indexMenu) in item"
                :key="indexMenu"
                :class="isMain(menu.title)"
                class="menu-container"
            >
                
                <h2>{{menu.title}}</h2>
                <ul>
                    <li
                        v-for="(dish,indexDish) in menu.dishes"
                        :key="indexDish"
                    >
                        <div class="name-price-row">
                            <a href="#">{{dish.name}}</a><h4></h4>
                            <span>${{dish.price}}</span>
                        </div>
                        <p class="dish-description">{{dish.description}}</p>
                    </li>
                </ul>
            </div>
        
        

    </section>
</template>

<script>
    export default {
        name: 'Menu',
        props:{
            item: Array
        },
        methods:{
            isMain : function(title){
                if (title.includes("Main")){
                    return "main-menu";
                }else{
                    return "normal-menu";
                }
            }
        }
    }
</script>

<style lang="scss">
    #menu{
        position: relative;
        width: 90%;
        margin: 60px auto;
        .menu-container{
            display: inline-block;
            margin: 20px 0;
            padding: 50px;
            
            width:calc(100%/3);
            h2{
                margin-bottom: 60px;
            }
            ul{
                li{
                    list-style: none;
                    margin-bottom:25px;
                    .name-price-row{
                        h4{
                            margin-bottom:10px;
                        }
                        display:flex;
                        justify-content: space-between;
                    }
                    .dish-description{
                        font-size: 14px;
                    }
                }
            }
        }
        .main-menu{
            position: static;
            background-color:black;
            color:white;
            margin-top: -30px;
            height: 100%;
            background-image: linear-gradient(to bottom, black, rgba(0,0,0,0.2)), url("../assets/images/misc22x.jpg");
            background-size: cover;       
            background-repeat: no-repeat;
        }
        
        .normal-menu{
            background-color:lightgray;
            color:black;
        }
    }
    

</style>