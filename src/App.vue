<template>
  <div id="app">
    <Header
      :menuHeader = "menu"
    />
    <Main />
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  data: function(){
    return{
      menu : [
        "Home",
        "Culinary history",
        "Our team",
        "Our menu",
        "Take out", 
        "Bulletin",
        "Reservation",
        "Carrello"
      ]
    }
  },
  components: {
    Header,
    Main,
    Footer
    
  }
}
</script>

<style lang="scss">
  @import "./assets/styles/general.scss";
  @import "~@fortawesome/fontawesome-free/css/all.min.css"; 

  
  #app{
    margin: 0 auto;

  }

</style>
