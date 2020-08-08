<template>
  <div id="app" :style="{backgroundColor: pageColor}">
    <div class="titulo">
      <h1>Teste de Border Radius</h1>
    </div>
    <div class="inputText">
        <div>
          <p>Conteúdo do Texto </p>
          <input type="text" v-model="text">
        </div>
    </div>
    <div class="inputColor">
      <div>
        <p>Cor do Texto </p>
        <input type="text" v-model="textColor">
      </div>
      <div>
        <p>Cor da Bloco </p>
        <input type="text" v-model="backgroundColor">
      </div>
      <div>
        <p>Cor da Margem </p>
        <input type="text" v-model="borderColor">
      </div>
    </div>

    <div class="bolder">
      <div class="box" :style="{backgroundColor : backgroundColor, borderColor : borderColor}">
        <div :style="{color: textColor}">{{text}}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      pageColor:'',
      borderColor:'',
      text : '',
      textColor: '',
      color : 'blue',
      backgroundColor: 'red',
    };
  }
};
</script>

<style >
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: sans-serif;
}
.titulo {
  display: flex;
  justify-content: center;
  padding: 30px;
}
.inputText {
  display: flex;
  justify-content: center;
  align-items: center;
}
.inputText div input{
  width: 500px;
}
.inputColor {
  display: flex;
  justify-content: center;
  padding: 15px;
}
.inputColor div {
  padding: 15px;
  margin: 0 15px;
}
.inputColor input {
  width: 100px;
}
.bolder {
  display: flex;
  justify-content: center;
}
.box {
  width: 500px;
  height: 300px;
  border: 3px solid black;
  margin: 30px;
  display: flex;
  align-items: center;
  justify-content: center;
}


</style>