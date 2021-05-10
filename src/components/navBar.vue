<template>

  <nav id="navBarContainer">
    
    <div id="logoContainer">

      <img @click="changePage('homePage')" src="../assets/logo.svg">

    </div>

    <div id="tagsMenuContainer">
      
      <h1 @click="changePage('aplicatii')"> APLICAȚII </h1>
      <h1 @click="changePage('geneza')"> GENEZA </h1>
      <h1 @click="changePage('etapele')"> ETAPELE </h1>
      <h1 @click="changePage('diferenta')"> DIFERENȚĂ </h1>
      <h1 @click="changePage('timpii')">TIMPII</h1>

    </div>

  </nav>


</template>


<style scoped>

  #navBarContainer{
    position:fixed;
    width:100%;
    z-index:100;
    display:flex;
    flex-direction:row;
    justify-content:space-between;
    align-items:center;
    background:#282F37;
  }

  #tagsMenuContainer{
    display: flex;
    justify-content: space-between;
    width:25%;
    padding:1%;
    color:#D9CFBF;
  }

</style>


<script>

  export default{

    name:"navBar",
    
    methods:{
      
      changePage: function(nextPage){
        this.$emit("changePage", nextPage);
      }
    },

  }


</script>
