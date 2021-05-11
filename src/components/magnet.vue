<template>

  <div id="magnetContainer" class='hide'>

    <div id="dataContainer">
      <div>
      <h3>Este piesa centrală a instalației IRM ; el trebuie să producă un câmp magnetic extern, cât mai uniform, evitând pe cât posibl variațiile.</h3>
      <h3>IRM realizează un foarte bun contrast între substanța albă și cea cenușie, imposibil de obținut prin altă metodă imagistică, ceea ce permite sesizarea unor procese patologice subtile, ce se produc la interfața acestora, de exemplu anomaliile de mielinizare ale copilului, scleroza multiplă și alte afecțiuni demielinizante. De asemenea, alte procese patologice pot fi reprezentate în imagine, precum edemul, infarctul, hemoragiile cerebrale. În cazul unor tumori cerebrale, diferențele între timpii de relaxare pe care le creează anumite variații histologice ( astrocitomul, meningiomul, metastazele) pot fi sugestive pentru natura acestora.</h3>
      </div>
      <img src="../assets/magnet.svg">
    </div>
  </div>
</template>

<style scoped>

  #magnetContainer{
      height:auto;
      width:100%;
      margin-bottom:30%;
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
      #magnetContainer{
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
        triggerElement: '#magnetContainer'
      }).setClassToggle('#magnetContainer', 'show');

      this.$scrollmagic.addScene(scene1);


    }
}

</script>
