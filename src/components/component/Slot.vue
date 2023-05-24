<template>
  <div class="card">
    <slot>Default Value</slot>
  </div>
</template>

<script lang="ts">
export default {
  name: 'Slot',
};
</script>

<style scoped>
.card {
  padding: 20px;
  border: 2px solid;
}
</style>
