<template>
    <section id="menu" class="flex">
        <div 
            v-for="(menu,indexMenu) in item"
            :key="indexMenu"
            class="menu-container"
            :class="isMain(menu.title)"
        >
        <h2>{{menu.title}}</h2>
        <ul>
            <li
                v-for="(dish,indexDish) in menu.dishes"
                :key="indexDish"
            >
                <div class="name-price-row">
                    <h4>{{dish.name}}</h4>
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
                    return "main-container";
                }
            }
        }
    }
</script>

<style lang="scss">
    #menu{
        width: 90%;
        margin: 60px auto;
        position: relative;
        .menu-container{
            display: inline-block;
            margin: 20px 0;
            padding: 50px;
            background-color:lightgray;
            width:calc(100%/3);
            h2{
                margin-bottom: 30px;
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
        .main-container{
            background-color:black;
            color:white;
            margin-bottom: 20px;
                        
        }
    }
    

</style>