<template>
  <div id="app">
    <h1>Pages</h1>
    <main>
      <MoleculesInputForm
        @pushSubmitButton="alertInputValue"
        @piyo="fun($event)"
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
  methods: {
    alertInputValue() {
      alert(this.inputValue)
    },
    fun(event) {
      console.log(event)
      this.inputValue = event
    },
  },
  data() {
    return {
      inputValue: "",
    }
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
