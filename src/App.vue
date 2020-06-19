<template>
  <div id="app">
    <h1>Pages</h1>
    <main>
      <MoleculesInputForm
        :inputValue="inputValue"
        @pushSubmitButton="alertInputValue"
        @input="updateValue($event)"
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
      inputValue: "jo",
    }
  },
  methods: {
    alertInputValue() {
      // ここでAPIコールを行うイメージ
      alert(this.inputValue)
    },
    updateValue(event) {
      // データの更新
      this.inputValue = event
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
