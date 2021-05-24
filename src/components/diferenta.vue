<template>

  <div id="diferentialContainer" class='hide'>

    <div id="dataContainer">
      <div id="topHalf">
        <h5>Structurile examinate interacționează cu un factor fizic exterior ( radiația X, ultrasunetele), atenuându-l sau reflectându-l, în IRM structurile sunt stimulate pentru a produce ele însele semnale utilizabile în producerea unei imagini. </h5>
      </div>
      <div id="bottomHalf">
        <h5>Ca și ultrasonografia, IRM recurge la un factor fizic neionizant, lipsit de nocivitate, aparținând metodelor de exploarare neinvazive. </h5>
      </div>
    </div>
  </div>
</template>

<style scoped>

  #diferentialContainer{
      width:100%;

  }

  #dataContainer{
    height:100%;
    margin-left:10%;
    margin-right:10%;

  }

  #dataContainer h5{
    font-size:2vw;
    color:#D9CFBF;
  }

  #bottomHalf{
    display:flex;
    justify-content:center;
    align-items:center;
    width:75%;
    margin-top:1%;
  }

  #topHalf{
    display:flex;
    flex-direction: column;
    justify-content: center;
    width:75%;
    align-items:center;

  }

  #topHalf h5{
    font-size:2vw;

  }
  
  .hide{
    opacity:0;
    transition:1s;
  }

  .show{
    opacity:1;
  }

  @media only screen and (max-width:414px){ 

    #diferentialContainer{
        display: flex;
        flex-direction: column-reverse;
        text-align:center;
        align-items: center;
        justify-content: center;
        border-bottom: 1px #D9CFBF solid;
        border-top: 1px #D9CFBF solid;
    }

    #diferentialContainer h5{
      font-size:150%;
    }

    #bottomHalf, #topHalf{
      width: 100%;
    }

     }
</style>


<script>
export default {
  mounted(){
      const scene1 = this.$scrollmagic.scene({
triggerElement: '#diferentialContainer'
}).setClassToggle('#diferentialContainer', 'show');

this.$scrollmagic.addScene(scene1);



  }
}
</script>

