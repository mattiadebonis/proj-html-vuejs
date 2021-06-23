<template>
  <div id="app">
    <!-- send menu to header -->
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
      //site menu
      menu : [
        {
          title:"Home",
          link: "#"
        },
        {
          title:"Culinary history",
          link: "#"
        },
        {
          title:"Our team",
          link: "#"
        },
        {
          title:"Our menu",
          link: "#"
        },
        {
          title:"Take out",
          link: "#"
        },
        {
          title:"Reservation",
          link: "#"
        },
        {
          title:"Carrello",
          link: "#"
        }
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
