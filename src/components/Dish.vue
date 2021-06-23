<template>
    <section id="dish">
        <img src="../assets/images/hero42x.jpg" alt="">
        <div class="dish-container">
            <div class="name-price">
                <h3 class="title-call">Braised Abalone</h3>
                <span>$52</span>
                <hr>
                <p class="description-call">Pretium accumsan porttitor viverra leo gravida mollis imperdiet. Fringilla nibh pharetra sociis leo amet.</p>
                <a class="button-call" href="#">View in the menu</a>
            </div>
            
            <span></span>
        </div>
    </section>
</template>

<script>
export default {
    name: "Dish"
}
</script>

<style lang="scss">
    @import "../assets/styles/general.scss";
    #dish{
        width:100%;
        position: relative;
        .dish-container{
            position: absolute;
            top: 100px;
            left: 200px;
            background-color: black;
            color: white;
            .name-price{
                display:flex;
                justify-content: space-between;
            }
        }
        img{
            width:100%;
            object-fit: cover;
            height: 600px;
        }
    }

</style>

