<template>
  <div id="app">
    <img class="imagem-vainaweb" src="./assets/imagens/vainaweb.svg">
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'app' ,
}

</script>

<style>
#app {
  background-color: #F16421;
  padding: 2%;
}
.imagem-vainaweb{
  width: 12%;
  display: flex;
  justify-content: flex-start;
  margin-left: 9%;

}
</style>
