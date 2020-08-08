<template>
  <div id="app">
    <div class="titulo">
      <h1>Teste de Border Radius</h1>
    </div>
    <div class="inputTop">
      <input type="text" v-model="color">
      <input type="text" v-model="color">
    </div>
    <div class="bolder">
      <div :style="{color: color}">Banana</div>
    </div>
    <div class="inputBottom">
      <input type="text" v-model="color">
      <input type="text" v-model="color">
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      color : 'blue'
    };
  }
};
</script>

<style >
.titulo {
  display: flex;
  justify-content: center;
}
.inputTop {
  display: flex;
  justify-content: space-around;
}
.bolder {
  display: flex;
  justify-content: center;
}
.inputBottom {
  display: flex;
  justify-content: space-around;
}

</style>