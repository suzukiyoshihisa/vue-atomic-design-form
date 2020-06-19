<template>
  <div>
    <h2>atom</h2>
    <p>{{ inputValue }}</p>
    <input
      type="text"
      class="input"
      :value="inputValue"
      @input="$emit('input', $event.target.value)"
      placeholder="入力フォーム"
    />
  </div>
</template>

<script>
export default {
  props: {
    inputValue: {
      type: String,
      require: true,
    },
  },
}
</script>

<style>
.input {
  width: 380px;
  padding: 12px 15px;
  margin: 20px;
  border-radius: 6px;
  border: 1px solid #aaa;
  font-size: 16px;
}
</style>
