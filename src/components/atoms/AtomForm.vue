<template>
  <div>
    <p>{{ hoge }}</p>
    <input
      type="text"
      class="input"
      @input="$emit('input', $event.target.value)"
      placeholder="入力フォーム"
    />
  </div>
</template>

<script>
export default {
  props: {
    hoge: {
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
