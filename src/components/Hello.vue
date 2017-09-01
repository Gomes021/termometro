<template>
  <main class="">
    <section class="caixa">
      <h1 class=""> COMO ESTÁ A AULA ?!</h1>
      <button class="imagens-icons"><img src="../assets/faces/chata.png"><p>CHATA</p></button>
      <button class="imagens-icons"><img src="../assets/faces/devagar.png"><p>DEVAGAR</p></button>
      <button class="imagens-icons"><img src="../assets/faces/ok.png"><p>OK</p></button>
      <button class="imagens-icons"><img src="../assets/faces/animada.png"><p>ANIMADA</p></button>
      <button class="imagens-icons"><img src="../assets/faces/incrivel.png"><p>IN-CRÍ-VEL</p></button>
    </section>
    <section>
      <p class="">MEU NOME É</p>
      <input type="text" name="MEU_NOME_É">
      <button class=""><img src="../assets/imagens/button.png"></button>
      <p class="">ESTOU TRAVADO !</p>
    </section>
  </main>

</template>

<script>
export default {
  name: '',
  data () {
    return {
      
    }
  }
}
</script>
<style>
  .caixa{
    width: 100%;
  }
  .imagens-icons{
    width: 30px;
  }
</style>
