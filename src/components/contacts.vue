<template>

  <div id="downloadContainer" class="hide">

    <div id="dataContainer">
      <h3>Site-ul a fost realizat de către: Gruescu Ipatie Daniel și Lorena Maria Vitan.</h3>
      <h3>Aici se poate găsi documentația și datele din site în format PDF</h3>
      <div id="downloadLinks">
        <a href="../../documentation/mainFile.pdf" download>Documentație</a>
        <a href="../../documentation/mainFile.pdf" download>Datele din Site</a>
      </div>
    </div>
  </div>
</template>

<style scoped>

  #downloadLinks{
    
    width:60%;
    display:flex;
    justify-content: space-between;

  }

  a{
    font-size:200%;
    text-decoration: none;
    color:#D9CFBF;
  }

  #downloadContainer{
      height:50%;
      width:100%;
      margin-bottom:5%;
  }
  .hide{
    opacity:0;
    transition:1s;
  }
  #dataContainer{
    height:auto;
    display:flex;
    flex-direction: column;
    align-items:center;
    margin-left:10%;
    margin-right:10%;
    margin-top:5%;
  }
  #dataContainer h3{
    font-size:2vw;
    color:#D9CFBF;
    width:100%;
  }
  #dataContainer img{
    max-width:50%;
    height:auto;
  }
  .show{
    opacity:1
  }


  @media only screen and (max-width:414px){ 
      #aplicationsContainer{
        margin-bottom:100%;
      }
      #dataContainer{
        flex-direction: column-reverse;
      }

      #dataContainer img{
        max-width: 100%;
      }

      #dataContainer h3{
        font-size: 150%;
      }

     }
</style>

<script>
export default{
    mounted(){
      const scene1 = this.$scrollmagic.scene({
        triggerElement: '#downloadContainer'
      }).setClassToggle('#downloadContainer', 'show');

      this.$scrollmagic.addScene(scene1);


    }
}

</script>
