<template>

  <div id="mainContainer">

    <div id="dataContainer">
      <div id="topHalf" class="hide">
        <h5>Durata semnalului RMN, este impusă de două procese fizice, care acționează în sens limitativ: </h5>
      </div>
      <div id="bottomHalf">
        <div id="leftPart" class='hide'>
          <div class="data">
            <h5>Revenirea nucleilor oscilanți la poziția lor inițială:</h5>
            <h5>Aceasta se însoțește de scăderea exponențială în timp a amplitudinii semnalului. Are ca substrat transferul de energie de la nucleii în precesie către moleculele mari ale vecinătății.</h5>
            <h5>Aceste molecule formează în jurul nucleilor rezonanți o veritabilă rețea, căreia îi este cedată energia dobândită de nucleii respectivi prin pulsul RF.</h5>
          </div>
          <div>
            <img src="../assets/Head.png"/>
          </div>
        </div>



        <div id="rightPart" class='hide'>
          <div> 
            <img src="../assets/rmn2.jpg"/>
          </div>
           <div>
            <h5>Durata semnalului restrănsă prin interacția nucleilor rezonanți (posesori de spin) cu rețeaua structurilor moleculare înconjurătoare este denumită timp de relaxare spin-rețea sau constantă de scădere exponențială T1.</h5>
            <h5>Un alt termen folosit în exprimarea acestui timp este timpul de relaxare longitudinală .</h5>
          </div>
       </div>
      </div>
    </div>
  </div>
</template>

<style scoped>

  #dataContainer{
    height:100%;
    display:flex;
    flex-direction:column;
    align-items:center;
    text-align: left;

  }

  .hide{
    opacity:0;
    transition:1s;
  }

  .show{
    opacity:1;
  }

  #rightPart{
    display:flex;
    width:85%;
    margin-top: 1%;
  }

  #rightPart img,#leftPart img{
    max-width: 100%;
  }

  #leftPart img{
    max-width: 200%;
  }

  #leftPart{
    
    display:flex;
    margin-top:1%;
    width:85%;

  }

  #dataContainer h5{
    font-size:2vw;
    color:#D9CFBF;
  }

  #bottomHalf{
    display:flex;
    justify-content:center;
    flex-direction:column;
    align-items:center;

  }

  @media only screen and (max-width:414px){ 

    #leftPart{
      display: flex;
      flex-direction: column-reverse;
      align-items:center ;
    }

    #rightPart{
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    #leftPart h5, #rightPart h5{
      font-size: 120%;
      text-align: center;
    }


     }
</style>


<script>
export default {
   mounted(){
      
      const scene1 = this.$scrollmagic.scene({
        triggerElement: '#leftPart'
      }).setClassToggle('#leftPart', 'show');

      const scene2 = this.$scrollmagic.scene({
        triggerElement: '#rightPart'
      }).setClassToggle('#rightPart', 'show');


      this.$scrollmagic.addScene(scene1);
      this.$scrollmagic.addScene(scene2);
  },
}
</script>

