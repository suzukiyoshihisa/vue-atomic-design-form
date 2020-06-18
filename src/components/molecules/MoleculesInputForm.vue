<template>
  <div class="molecules">
    <h2>molecules</h2>
    <p>v:{{ value }}</p>
    <p>hoge:{{ hoge }}</p>
    <atom-form v-model="value" @input="fuga" />
    <atom-button @pushSubmitButton="$emit('pushSubmitButton')" />
  </div>
</template>

<script>
import AtomButton from '../atoms/AtomButton';
import AtomForm from '../atoms/AtomForm';

export default {
  components: {
    AtomButton,
    AtomForm,
  },
  props: {
    hoge: {
      type: String,
      default: '',
    },
  },
  data() {
    return {
      value: '',
    };
  },
  methods: {
    fuga() {
      this.$emit('piyo', this.value);
    },
  },
};
</script>
