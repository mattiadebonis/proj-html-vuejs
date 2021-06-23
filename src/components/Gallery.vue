<template>
    <section class="wdt-100 gallery-container">
        <img src="../assets/images/page52x.jpg" alt="">
        <p>Kung pad chicken - $32</p>
    </section>
</template>

<script>
    export default {
        name: 'Gallery'
    }
</script>

<style lang="scss">
  @import "../assets/styles/general.scss";
  
    .gallery-container{
        position: relative;
        img{
            height: 325px;
        }
        p{
            position: absolute;
            bottom:5px;
            right: 50%;
            transform: translate(50%, -0%);
            color:white;
            text-transform: uppercase;
            font-size: 12px;
        }
    }
</style>
