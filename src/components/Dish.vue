<template>
    <section id="dish">
        <img src="../assets/images/hero42x.jpg" alt="">
        <div class="container-call dish-container">
            <div class="name-price">
                <h2 class="title-call">Braised Abalone</h2>
                <span>$52</span>
            </div>
            <hr>
            <p class="description-call">Pretium accumsan porttitor viverra leo gravida mollis imperdiet. Fringilla nibh pharetra sociis leo amet.</p>
            <a class="button-call" href="#">View in the menu</a>
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
        height: 630px;

        position: relative;
        
        .dish-container{
            width: 350px;
            padding: 50px;
            position: absolute;
            top: 100px;
            left: 10%;
            background-color: black;
            color: white;
            .name-price{
                display:flex;
                justify-content: space-between;
                align-items: flex-start;
                span{
                    margin: 20px 0;
                }
            }
            h2,
            span,
            p,
            a,
            hr{
                margin-left: 20px;
            }
            hr{
                width:50px;
            }
            

        }
        img{
            width:100%;
            height: 100%;
            object-fit: cover;
        }
    }

</style>

