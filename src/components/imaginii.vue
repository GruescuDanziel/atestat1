<template>
  <div id="imaginiiContainer" class='hide'>

    <div id="etapa1" class="dataContainer">
      <div class='textData'> 
        <h3>Imaginea RMN rezultă prin alăturarea unui număr variabil de pixeli, a căror valoare este determinată de amplitudinea fiecăruia din semnalele cu originea într-o unitate de volum.</h3>
        <h3>Aceste volume elementare se găsesc dispuse într-un plan de secțiune prin corpul uman, astfel încât, ca și în cazul CT, imaginea RMN este de fapt o imagine tomografică realizată în planul respectiv</h3>
      </div>
    </div>

    <div id="etapa2" class="dataContainer">
      <div class='textData'>
        <h3>Pentru ca ea să capete semnificația dorită, nu este suficient ca semnalele RMN provenite din fiecare volum elementar examinat să fie recepționate ; aceste semnale trebuie să cuprindă și informații cu privire la poziția exactă în spațiu a volumelor respective</h3>
      </div>
    </div>
     <div id="etapa3" class="dataContainer">
      <div class='textData'>
        <h3>Poziția pixelilor în matrice trebuie să realizeze în ansamblu o veritabilă hartă a secțiunii anatomice.Acest deziderat creează în cazul IRM probleme tehnice complexe</h3>
      </div>
    </div>
  </div>
</template>

<style scoped>

#etapa3 img, #etapa1 img{
    max-width: 50%;
    margin-left:10%;
  }

  #etapa4{
    padding-bottom:10%;
  }

  #etapa3{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }

  .show{
    opacity:1;
  }

  .dataContainer{
    height:auto;
    display:flex;
    width:80%;
    align-items:center;
  }


  #imaginiiContainer{

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    margin-bottom:10%;

  }
  .dataContainer h3{
    font-size: 2vw;
    color:#D9CFBF;
  }

  .hide{
    opacity:0;
    transition: 1s;
  }

  .show{
    opacity: 1;
    text-align:left;
  }


</style>



<script>


  export default{

    name:"etapele",

    mounted(){
      
      const scene1 = this.$scrollmagic.scene({
        triggerElement: '#imaginiiContainer'
      }).setClassToggle('#imaginiiContainer', 'show');

      this.$scrollmagic.addScene(scene1);

    }

  }

</script>

