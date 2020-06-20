<template>
  <div id="app">
    <h1>Pages</h1>
    <main>
      <MoleculesInputForm
        :inputValue="inputValue"
        @pushSubmitButton="alertInputValue"
        @change="updateValue"
      />
    </main>
  </div>
</template>

<script>
import MoleculesInputForm from "./components/molecules/MoleculesInputForm"

export default {
  components: {
    MoleculesInputForm,
  },
  data() {
    return {
      // Pagesでデータの保持
      inputValue: "",
    }
  },
  methods: {
    alertInputValue() {
      // ここでAPIコールを行うイメージ
      alert(this.inputValue)
    },
    updateValue(newValue) {
      // データの更新
      this.inputValue = newValue
    },
  },
}
</script>

<style>
#app {
  display: flex;
  justify-content: center;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

main {
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
}
</style>
