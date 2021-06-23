<template>
    <section class="wdt-100 flex">

        <!-- left menu -->
        <div class="left-menu">
            <img :src="componeUrlImg(item.img)" alt="">

        </div>
        <!-- /left menu -->

        <!-- right menu -->
        <div class="right-menu">
            <div class="container-call">
                    <hr class="up-divider-call">
                    <p class="subtitle-call">{{item.subtitle}}</p>
                    <h1 class="title-call">{{item.title}}</h1>
                    <p class="description-call">{{item.description}}</p>
                    <a href="#" class="button-call">{{item.button}}</a>
                </div>
        </div>
        <!-- right menu -->
    </section>
</template>

<script>

    export default {
        name: 'CallToAction',
        props: {
            item : Object
        },
        methods: {
            componeUrlImg : function (nameFile){
                const folder = "./assets/images/"
                var url = folder + nameFile;
                return url;
            }
        } 
    }
</script>

<style lang="scss">
    @import "../assets/styles/variable.scss";
    .left-menu,
    .right-menu{
        height: 560px;
    }

    .left-menu{
        width: $wdt-60;
        background-size:cover;
    }

    .right-menu{
        width: $wdt-40;
        background-color:black;
        color: white;
        padding: 100px;
    }

</style>