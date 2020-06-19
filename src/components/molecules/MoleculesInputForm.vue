<template>
  <div class="molecules">
    <h2>molecules</h2>
    <p>{{ inputValue }}</p>
    <atom-form
      v-model="value"
      :inputValue="inputValue"
      @input="$emit('input', value)"
    />
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
  props: {
    inputValue: {
      type: String,
      require: true,
    },
  },
}
</script>
