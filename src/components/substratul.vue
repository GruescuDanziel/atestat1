<template>
  <div id="substratulContainer" class="hide">

    <div id="etapa1" class="dataContainer">
      <div class='textData'> 
        <h3>
          Semnalele provin de la protonii corpului uman examinat; însă nu toți participă la producerea lor ;
        </h3>
        <h3>Nucleii implicați în apariția semnalelor sunt din apa celulară, care constituie cea mai mare proporție a protonilor din corpul uman și din lipide . </h3>
      </div>
        <img src="../assets/RMN4.jpg" />
    </div>

    <div id="etapa2" class="dataContainer">
        <img src="../assets/Rmn3.jpg" />
      <div class='textData'>
        <h3>În celule și țesuturi, o proporție din apă este legată la suprafața proteinelor ; mișcarea de precesie a nucleilor de hidrogen va fi rapid încetinită datorită vecinătății moleculelor mari, ceea ce va avea ca rezultat un T1 scurt.</h3>
      </div>
    </div>
     <div id="etapa3" class="dataContainer">
      <div class='textData'>
        <h3>Se acceptă așa-numitul concept al apei libere și legate care poate constitui o explicație satisfăcătoare pentru T1.</h3>
      </div>
    </div>
     <div id="etapa4" class="dataContainer">
      <div class='textData'>
        <h3>Este de așteptat ca starea apei tisulare să determine, pe lângă intensitatea semnalelor respective și valorile T1 și T2 </h3>
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
    padding-bottom:2%;
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


  #substratulContainer{

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;


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

  @media only screen and (max-width:414px){ 
    
    #substratulContainer{
      flex-direction: column;
    }

    #etapa1{
      flex-direction: column-reverse;
    }

    #etapa1 img{
      max-width: 100%;
    }

    #etapa1 h3{
      font-size:150%;
    }

    #etapa2 img{
      max-width: 100%;
    }

    #etapa2{
      flex-direction: column;
    }

    #etapa2 h3{
      font-size:150%;
    }

    #etapa4 h3, #etapa3 h3{
      font-size:150%;
    }


     }

</style>



<script>


  export default{

    name:"etapele",

    mounted(){
      
      const scene1 = this.$scrollmagic.scene({
        triggerElement: '#substratulContainer'
      }).setClassToggle('#substratulContainer', 'show');

      this.$scrollmagic.addScene(scene1);

    }

  }

</script>

