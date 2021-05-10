<template>

  <div id="slectiveContainer" class='hide'>
    <div id="dataContainer">
      <h3>Corpul uman este plasat în câmpul magnetic exterior foarte puternic.</h3>
      <h3>Pentru obținerea excitației selective se aplică în aceeași direcție spațială un câmp-gradient mult mai slab, care variază de-a lungul pacientului, astfel încât este mai redus la extremitatea lui superioară și mai intens la cea inferioară. Rezultă un câmp magnetic total, care crește și el în același sens.</h3>
      <h3>Tehnica excitației selective este aplicată pentru a alege planul ce va fi reprezentat în imagine. Poate fi aleasă o secțiune tomografică sagitală, utilizând un gradient dispus transversal, sau una frontală, cu un gradient orientat antero-posterior.</h3>
    </div>
  </div>
</template>

<style scoped>

  #slectiveContainer{
    width:100%;
    height:100%;
    display: flex;
    flex-direction: column;
    align-items:center;

  }

  #dataContainer{
    width:80%;
    display:flex;
    flex-direction: column;
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


</style>

<script>

export default{
    mounted(){
      const scene1 = this.$scrollmagic.scene({
        triggerElement: '#slectiveContainer'
      }).setClassToggle('#slectiveContainer', 'show');

      this.$scrollmagic.addScene(scene1);


    }
}


</script>
