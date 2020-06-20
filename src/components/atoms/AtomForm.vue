<template>
  <div>
    <h2>atom</h2>
    <p>{{ value }}</p>
    <input type="text" class="input" v-model="inputText" />
  </div>
</template>

<script>
export default {
  props: {
    value: {
      type: String,
      require: true,
    },
  },
  computed: {
    inputText: {
      get: function() {
        return this.value
      },
      set: function(value) {
        // inputに入力があった場合にイベントを発行
        this.$emit("change", value)
      },
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
