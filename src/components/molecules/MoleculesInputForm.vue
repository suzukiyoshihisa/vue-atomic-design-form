<template>
  <div class="molecules">
    <h2>molecules</h2>
    <p>{{ inputValue }}</p>
    <atom-form :value="inputValue" @change="changeFromValue" />
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
  props: {
    inputValue: {
      type: String,
      require: true,
    },
  },
  methods: {
    changeFromValue: function(inputValue) {
      this.$emit("change", inputValue)
    },
  },
}
</script>
