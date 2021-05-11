<template>

  <div id="aplicationsContainer" class="hide">

    <div id="dataContainer">
      <h3>Imagistica medicală a înregistrat un progres real odată cu introducerea RMN-ului ca tehnică imagistică de diagnostic. Principalele caracteristice ale acestei tehnici sunt neinvazivitatea și calitatea marea a imaginii. Scleroza multiplă, boală neurologicâ demielinizantă, este un exemplu relevant de aplicație a RMN-ului în studiul sistemului nervos central. </h3>
      <img src="../assets/aplicatii.png">
    </div>
  </div>
</template>

<style scoped>

  #aplicationsContainer{
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
    align-items:center;
    margin-left:10%;
    margin-right:10%;
    margin-top:5%;
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
        triggerElement: '#aplicationsContainer'
      }).setClassToggle('#aplicationsContainer', 'show');

      this.$scrollmagic.addScene(scene1);


    }
}

</script>
