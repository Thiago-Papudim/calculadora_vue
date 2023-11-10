<script>
  export default {
    data() {
      return {
        num1: 0,
        num2: 0,
        operation: 'add',
      };
    },
    computed: {
      result() {
        switch (this.operation) {
          case 'add':
            return this.num1 + this.num2;
          case 'subtract':
            return this.num1 - this.num2;
          case 'multiply':
            return this.num1 * this.num2;
          case 'divide':
            return this.num1 / this.num2;
          default:
            return 0;
        }
      },
    },
  };
</script>

<template>
  <div id="app">
    <h1>Calculadora Aritmética</h1>

    <div>
      <label for="num1">Número 1:</label>
      <input type="number" v-model="num1">
    </div>

    <div>
      <label for="num2">Número 2:</label>
      <input type="number" v-model="num2">
    </div>

    <div>
      <label for="operation">Operação:</label>
      <select v-model="operation">
        <option value="add">Adição (+)</option>
        <option value="subtract">Subtração (-)</option>
        <option value="multiply">Multiplicação (*)</option>
        <option value="divide">Divisão (/)</option>
      </select>
    </div>

    <div>
      <h2>Resultado: {{ result }}</h2>
    </div>
  </div>
</template>

<style scoped>
  #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

label {
  display: block;
  margin-bottom: 5px;
}

input, select {
  padding: 10px;
  margin-bottom: 15px;
  width: 100%;
  box-sizing: border-box;
}

h1 {
  margin-bottom: 20px;
}

h2 {
  color: #3498db;
}
</style>