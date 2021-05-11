<template>

  <div id="mainContainer">

    <img src="../assets/main.png">
    <h1> IMAGISTICA PRIN REZONANȚĂ MAGNETICĂ NUCLEARĂ </h1>


  </div>

</template>



<style scoped>

  img{
    position:absolute;
    max-width:100%;
  }

  h1{
  
    z-index:100;
    
  }

  #mainContainer{
    height:100%;
    width:100%;
    background-size:stretch;

    display:flex;
    justify-content:center;
    align-items:center;
    font-size:150%;
    text-align:center;
    color:white;
  }

  @media only screen and (max-width:414px){ 
      
    h1{
        
      font-size: 100%;

    }
   img{
    position:absolute;
    max-width:100%;
  }

     
    

     }

</style>


<script>


</script>
