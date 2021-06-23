<template>
    <section id="summary" class="margin-page">
        <div class="wdt-100 flex">
            <!-- left summary -->
            <div class="left-summary">
                <p><strong>HAC TELLUS, FELIS RISUS AT</strong> mattis mattis. Eget eusimod semper egwt tortor,donec amet, blandit. Trisique facilisi faucibus elementum feugiat in nam in feugiat. Ipsum odio etiam duis dacilisis amet vulaputate</p>
                <h2>Food is our common ground, a universal experience.</h2>
                <p>Tristique tempus condimentum diam donec. Condimentum ullamcorper sit elementum hendrerit mi nulla in consequat, ut. Metus, nullam scelerisque netus viverra dui.</p>
                <img class="signature" src="../assets/images/signature.jpg" alt="signature">
            </div>
            <!-- /left summary -->

            <div class="right-summary">
                <p class="subtitle-call">california rolls - $22</p>
            </div>

        </div>
        
        <div class="bottom-summary flex">
            <div>
                <img src="../assets/images/sushi-1.png" alt="sushi-1">
                <h4>The best table in town</h4>
                <hr>
                <p>Sed aenean egestas ut aliquam turpis mauris, molestie. Vitae tellus tempor sem id tempus neque, tellus turpis turpis. Morbi otrtor id gravida aliquet.</p>
                <a href="#" class="button-light">Explore the menu</a>
            </div>
            <div>
                <img src="../assets/images/sushi-2.png" alt="sushi-1">
                <h4>The best table in town</h4>
                <hr>
                <p>Sed aenean egestas ut aliquam turpis mauris, molestie. Vitae tellus tempor sem id tempus neque, tellus turpis turpis. Morbi otrtor id gravida aliquet.</p>
                <a href="#" class="button-light">Explore the menu</a>
            </div>
            <div>
                <img src="../assets/images/sushi-3.png" alt="sushi-1">
                <h4>The best table in town</h4>
                <hr>
                <p>Sed aenean egestas ut aliquam turpis mauris, molestie. Vitae tellus tempor sem id tempus neque, tellus turpis turpis. Morbi otrtor id gravida aliquet.</p>
                <a href="#" class="button-light">Explore the menu</a>
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
    @import "../assets/styles/callToAction.scss";
    #summary{
        color: gray;
        .left-summary,
        .right-summary{
            width: 40%;
            margin: 0 auto;
        }
        .left-summary{
            padding-right: 50px;
            p{
                font-size:14px;
                line-height: 22px;
            }   
            h2{
                color: black;
            }
            .signature{
                margin: 25px 0;
                width: 100px;
            }
        } 
        .right-summary{
            position: relative;
            background-size: cover;
            background-image: url("../assets/images/info22x.jpg");
            background-position: center;
            p{
                text-transform: uppercase;
                position:absolute;
                bottom:10px;
                right:50%;
                transform: translate(50%, 0);
                font-size: 10px;
                color: white;

            }
        }
        .bottom-summary{
            width: 100%;
            margin: 100px 0;
            div{
                width:(100% /3);
                padding: 10px;
                text-align: center;
                position: relative;
                img{
                    width: 70px;
                    
                }
                h4{
                    margin: 20px 0;
                    color: black;
                }
                hr{
                    display: inline;
                    position:absolute;
                    right: 50%;
                    transform:translate(50%,0);
                    width: 60px;
                    border: 0 ;
                    background-color:lightgray;
                    height: 1px;
                    
                }
                
                p{
                    margin: 42px 0;
                    font-size:12px;
                    line-height: 22px;
                }
                .button-light{
                    padding: 10px 30px;
                    background-color: none;
                    border: 1px solid lightgray;
                    text-decoration: none;
                    color: gray;
                    text-transform: uppercase;
                    font-size: 12px;
                    &:hover{
                        border-color: black;
                    }
                }
            }
        }
    }
    
    

</style>