<template>
  <div class="molecules">
    <h2>molecules</h2>
    <atom-form v-model="value" @input="$emit('piyo', value)" />
    <atom-button @pushSubmitButton="$emit('pushSubmitButton')" />
  </div>
</template>

<script>
import AtomButton from "../atoms/AtomButton"
import AtomForm from "../atoms/AtomForm"

export default {
  components: {
    AtomButton,
    AtomForm,
  },
  data() {
    return {
      value: "",
    }
  },
}
</script>
