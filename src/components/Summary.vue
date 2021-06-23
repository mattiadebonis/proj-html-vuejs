<template>
    <section class="margin-page">
        <div class="wdt-100 flex">
            <!-- left summary -->
            <div class="left-summary">
                <p>HAC TELLUS, FELIS RISUS AT mattis mattis. Eget eusimod semper egwt tortor,donec amet, blandit. Trisique facilisi faucibus elementum feugiat in nam in feugiat. Ipsum odio etiam duis dacilisis amet vulaputate</p>
                <h2>Food is our common ground, a universal experience.</h2>
                <p>Tristique tempus condimentum diam donec. Condimentum ullamcorper sit elementum hendrerit mi nulla in consequat, ut. Metus, nullam scelerisque netus viverra dui.</p>
                <img class="signature" src="../assets/images/signature.jpg" alt="signature">
            </div>
            <!-- /left summary -->

            <div class="right-summary">a</div>

        </div>
        
        <div class="bottom-summary flex">
            <div>
                <img src="../assets/images/sushi-1.png" alt="sushi-1">
                <h4>The best table in town</h4>
                <hr>
                <p>Sed aenean egestas ut aliquam turpis mauris, molestie. Vitae tellus tempor sem id tempus neque, tellus turpis turpis. Morbi otrtor id gravida aliquet.</p>
                <span>Explore the menu</span>
            </div>
            <div>
                <img src="../assets/images/sushi-1.png" alt="sushi-1">
                <h4>The best table in town</h4>
                <hr>
                <p>Sed aenean egestas ut aliquam turpis mauris, molestie. Vitae tellus tempor sem id tempus neque, tellus turpis turpis. Morbi otrtor id gravida aliquet.</p>
                <span>Explore the menu</span>
            </div>
            <div>
                <img src="../assets/images/sushi-1.png" alt="sushi-1">
                <h4>The best table in town</h4>
                <hr>
                <p>Sed aenean egestas ut aliquam turpis mauris, molestie. Vitae tellus tempor sem id tempus neque, tellus turpis turpis. Morbi otrtor id gravida aliquet.</p>
                <span>Explore the menu</span>
            </div>
        </div>
    </section>
</template>

<script>

    export default {
        name: 'Summary',
        
    }
</script>

<style  lang="scss">
    @import "../assets/styles/general.scss";
    
    .left-summary,
    .right-summary{
        width: 45%;
        margin: 0 auto;
    }
    .right-summary{
        background-size: cover;
        background-image: url("../assets/images/info22x.jpg")
    }
    .bottom-summary{
        width: 100%;
        margin: 100px 0;
        div{
            width:(100% /3);
            padding: 10px;
            text-align: center;
            img{
                width: 80px;
            }
        }
    }
    .signature{
        width: 100px;
    }
    

</style>