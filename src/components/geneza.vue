<template>

  <div id="genezaContainer" class='hide'>
    <div id="dataContainer">
      <h3>Metoda se bazează pe fenomenul fizic al rezonanței magnetice nucleare.
O imagine obținută traduce în semnale optice intensitatea semnalelor de radiofrecvență (RF) ale unor nuclei atomici din structuri anatomice examinate. 
Metoda se bazează pe proprietatea unor nuclei atomici, în special a celor de hidrogen (respectiv protonilor) de a realiza o mișcare de rotație în jurul propriului ax, adică de a avea un moment cinetic propriu, spinul nuclear.
Rotația unei particule încărcate electric, cum este protonul, determină apariția unui câmp magnetic propriu orientat în sens opus câmpului electric.
Aceasta transformă fiecare nucleu într-un dipol magnetic, un magnet microscopic. 
</h3>
    <img src="../assets/proton.svg">
    </div>
  </div>
</template>

<style scoped>

  #dataContainer{
    height:100%;
    display:flex;
    align-items:center;
    padding-left:10%;
    padding-right:10%;
  }

  .hide{
    opacity:0;
    transition:1s;
  }

  .show{
    opacity:1;
  }

  #dataContainer h3{
    font-size: 3.5vh;
    color:#D9CFBF;
  }

  @media only screen and (max-width:414px){ 

      #dataContainer{
        flex-direction: column-reverse;
        border-top: 1px #D9CFBF solid;
      }

      #dataContainer img{
        max-width: 100%;
      }     

     }

</style>

<script>

export default{
    mounted(){
      const scene1 = this.$scrollmagic.scene({
        triggerElement: '#genezaContainer'
      }).setClassToggle('#genezaContainer', 'show');

      this.$scrollmagic.addScene(scene1);


    }
}


</script>
