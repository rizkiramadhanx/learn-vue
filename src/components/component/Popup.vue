<template>
  <div class="box-popup">
    <div>this popup</div>
    <button @click="$emit('close', 'Vishwas')">close pop</button>
  </div>
</template>

<script lang="ts">
export default {
  name: 'Popup',
  data() {
    return {};
  },
  emits: ['close'],
};
</script>

<style scoped>
.box-popup {
  border: 2px solid;
  padding: 10px;
}
</style>
