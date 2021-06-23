<template>
    <section id="menu">
        <!-- send menus to Menu component -->
        <Menu  :item="menus"/>
    </section>
</template>

<script>
    import Menu from "./Menu.vue";
    export default {
        
        name: 'Menus',
        components:{
            Menu
        },
        data : function (){
            return{
                //menus
                menus: [
                    {
                        title: "Hors d'oeuvres",
                        dishes:[
                            {
                                name: "Ahi salmon nigiri",
                                description: "Eget vulputate vitae quis rutrum blandit sed. Quam nulla soit lacinia",
                                price: 48,
                                link:"#"
                            },
                            {
                                name: "Umi masu salad",
                                description: "Mollis omare sit sapien, sodales. Cursus duis proin semper quisque.",
                                price: 21,
                                link:"#"
                            },
                            {
                                name: "Temaki uiz creb",
                                description: "Ae vel risus omare seneetus placerat duis amet disctumst tellus. ",
                                price: 32,
                                link:"#"
                            },
                            {
                                name: "California rolls",
                                description: "Ae vel risus omare seneetus placerat duis amet disctumst tellus. ",
                                price: 22,
                                link:"#"
                            },

                        ]
                    },
                    {
                        title: "Main course",
                        dishes:[
                            {
                                name: "Braised abalone",
                                description: "Mollis omare sit sapien, sodales. Cursus duis proin semper quisque.",
                                price: 52,
                                link:"#"
                            },
                            {
                                name: "Twiced cooked pork",
                                description: "Ae vel risus omare seneetus placerat duis amet disctumst tellus. ",
                                price: 21,
                                link:"#"
                            },
                            {
                                name: "Kung pao chicken",
                                description: "Quis duis sit dictum aliquam a velit enim. Tellus in sit augue aliquam",
                                price: 32,
                                link:"#"
                            },
                            {
                                name: "Char siu e sushis ",
                                description: "Feugiat rhoncus ipsum tristique prurs diam, et dolor molestie.  ",
                                price: 48,
                                link:"#"
                            },

                        ]
                    },
                    {
                        title: "Dessert",
                        dishes:[
                            {
                                name: "Chocolate ball cake",
                                description: "In pellentesque in felis massa vehicula. In sed euismod ut",
                                price: 13
                            },
                            {
                                name: "Lime pie with crust",
                                description: "Mollis ornare sit sapien,sodales. Cursus dui proin semper quisque.",
                                price: 14
                            },
                            {
                                name: "Raspeberry pear cake",
                                description: "Eget vulputate vitae quis rutrum blandit sed. Quam nulla sit.",
                                price: 18
                            },
                            {
                                name: "Cafè au lait",
                                description: "Eget vulputate vitae quis rutrum blandit sed. Quam nulla sit.",
                                price: 6
                            },

                        ]
                    }
                ]
            }
            
            
        }
    }
</script>

<style lang="scss">
    #menu{
        margin-top:120px;
    }
</style>