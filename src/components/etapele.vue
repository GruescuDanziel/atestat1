<template>
  <div id="etapeleContainer">

    <div id="etapa1" class="dataContainer">
      <div class='textData'> 
        <h3>
          Obținerea imaginii prin aceste fenomen de rezonanță magneticâ cuprinde câteva momente distincte.
          În condiții obișnuite, orientarea micromagneților reprezentați de nucleii atomici din structurile anatomice este întâmplătoare.
          Câmpurile magnetice individuale se neutralizeazâ reciproc, astfel că manifestările lor nu sunt decelabile.
        </h3>
        <h3>Corpul uman este supus unui câmp magnetic exterior foarte puternic, care rămâne constant în timpul investigației și care produce alinierea în aceeași direcție a dipolilor magnetici nucleari.</h3>
      </div>
      <img src="../assets/etapa1.svg">
    </div>

    <div id="etapa2" class="dataContainer">
      <div class='textData'>
        <h3> Aplicarea unui câmp magnetic exterior foarte puternic produce alinierea lor în direcția acestuia </h3>
        <h3> Se aplică apoi o undă de radiofrecvență (RF), ceea ce determină rezonanța nucleilor.  </h3>
      </div>
      <img src="../assets/etapa2.svg">
    </div>
     <div id="etapa3" class="dataContainer">
      <div class='textData'>
        <h3>Un impuls scrut RF determinâ intrare în rezonanță a nucleilor</h3>
        <h3>Unda de RF este apoi suprimată. Nucleii continuă să oscileze, emițând o undă de RF, care poate fi detectată ca semnal rezonant magnetic al nucleilor. </h3>
      </div>
      <img src="../assets/etapa3.svg">
    </div>
     <div id="etapa4" class="dataContainer">
      <div class='textData'>
        <h3>Dupâ suprimarea impulsului RF, nucleii își continuâ oscilația, emițând o undâ de radiofrecvență decelabilâ.</h3>
        <h3>Acest semnal este transmis unui computer, care îl transformă, prin prelucrare digitală, în semnale optice elementare (pixeli).</h3>
      </div>
      <img src="../assets/etapa4.svg">
    </div>
  </div>
</template>

<style scoped>

  #etapa1 img{
    max-width: 50%;
  }
  #etapa2 img{
    max-width: 50%;
  }

  #etapa3 img{
     max-width: 50%;
  }

  #etapa4 img{
      max-width: 50%;
  }

  #etapa4{
    padding-bottom:10%;
  }

  .dataContainer{
    opacity:0;
    transition:1s;
  }
  
  .show{
    opacity:1;
  }


  .dataContainer{
    height:auto;
    display:flex;
    align-items:center;
    padding-left:10%;
    padding-right:10%;
    padding-top:1%;
  }

  .dataContainer h3{
    font-size: 2vw;
    color:#D9CFBF;
  }


  @media only screen and (max-width:414px){ 

      .dataContainer{
        flex-direction: column-reverse;
        margin-bottom:5%; 
        border-bottom: 1px #D9CFBF solid;
        padding-bottom: 2%;
      }

      #etapeleContainer{
        margin-top:60%;
      }

      #etapeleContainer img{
        max-width: 100%;
      }

      #etapeleContainer h3{
        font-size:120%;
      }

     }
</style>



<script>


  export default{

    name:"etapele",

    mounted(){
      
      const scene1 = this.$scrollmagic.scene({
        triggerElement: '#etapa1'
      }).setClassToggle('#etapa1', 'show');

      const scene2 = this.$scrollmagic.scene({
        triggerElement: '#etapa2'
      }).setClassToggle('#etapa2', 'show');

      const scene3 = this.$scrollmagic.scene({
        triggerElement: '#etapa3'
      }).setClassToggle('#etapa3', 'show');

      const scene4 = this.$scrollmagic.scene({
        triggerElement: '#etapa4'
      }).setClassToggle('#etapa4', 'show');

      this.$scrollmagic.addScene(scene1);
      this.$scrollmagic.addScene(scene2);
      this.$scrollmagic.addScene(scene3);
      this.$scrollmagic.addScene(scene4);

    }

  }

</script>

