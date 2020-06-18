<template>
  <button class="button" @click="$emit('pushSubmitButton')">
    submit
  </button>
</template>

<style>
.button {
  appearance: none;
  border: 0;
  border-radius: 5px;
  background: #4676d7;
  color: #fff;
  padding: 8px 16px;
  font-size: 16px;
}
</style>
