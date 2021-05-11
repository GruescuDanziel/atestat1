<template>
  <div id="app">
    <homePage />
    <aplicatii />
    <etape />
    <timpii />
    <geneza />
    <diferenta />
    <substratul />
    <imaginii />
    <selectiva />
    <magnet />
    <investigare />
  </div>
</template>

<script>

//Pages
import homePage from './components/homePage.vue'
import aplicatii from './components/aplicatii.vue'
import etape from './components/etapele.vue' 
import geneza from './components/geneza.vue'
import Timpii from './components/timpii.vue'
import Diferenta from './components/diferenta.vue'
import Substratul from './components/substratul.vue'
import Imaginii from './components/imaginii.vue'
import Selectiva from './components/selectiva.vue'
import Magnet from './components/magnet.vue'
import Investigare from './components/investigare.vue'

export default {
  name: 'App',
  components: {
    homePage,
    aplicatii,
    etape,
    geneza,
    Timpii,
    Diferenta,
    Substratul,
    Imaginii,
    Selectiva,
    Magnet,
    Investigare

  },
  methods:{
    changePage : function(nextPage){
      this.currentPage = nextPage;
    }
  },
  data(){
    return{
      currentPage: 'homePage'
    }
  }
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Share:wght@400;700&display=swap');

  ::-webkit-scrollbar {
    width:10px;
  }
  ::-webkit-scrollbar-track {
    background: #AEA388;
  }
  ::-webkit-scrollbar-thumb {
    background:#282F37;
    width:9px;
    border-radius:10px;
  }
  body, html{
  height:100%;
  width:100%;
  background:black;
  }
  #app{

    top:0;
    left:0;
    height:100%;
    width:auto;
  }
  *{
    font-family:cursive;
    margin:0;
  }

</style>
