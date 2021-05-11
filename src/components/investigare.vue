<template>

  <div id="sclerozaContainer" class="hide">

    <div id="dataContainer">
      <h3>Scleroza multiplă (SM) este o entitate patologică neurologică invalidantă, frecventă în țările europene cu climă temperată.SM este o afecțiune inflamatorie ce implică sistemul imunitar, cu etiologie probabil virală, asociată unei susceptibilități genetice individuale. Nu s-a descoperit încă un agent responsabil, nu s-a nominalizat un factor ereditar implicat, deși s-au efectuat numeroase studii genetice.</h3>
      <img src="../assets/scleroza.jpg">
    </div>
  </div>
</template>

<style scoped>

  #sclerozaContainer{
      height:50%;
      width:100%;
      margin-top:10%;
  }
  .hide{
    opacity:0;
    transition:1s;
  }
  #dataContainer{
    height:auto;
    display:flex;
    align-items:center;
    margin-left:10%;
    margin-right:10%;
  }
  #dataContainer h3{
    font-size:2vw;
    color:#D9CFBF;
  }
  #dataContainer img{
    max-width:50%;
    height:auto;
  }
  .show{
    opacity:1
  }

  @media only screen and (max-width:414px){ 
    #sclerozaContainer{
    }
    #dataContainer{
      flex-direction: column-reverse;
    }
    #dataContainer img{
      max-width: 100%;
    }
    #dataContainer h3{
      font-size:120%;
    }
     }

</style>

<script>
export default{
    mounted(){
      const scene1 = this.$scrollmagic.scene({
        triggerElement: '#sclerozaContainer'
      }).setClassToggle('#sclerozaContainer', 'show');

      this.$scrollmagic.addScene(scene1);


    }
}

</script>
