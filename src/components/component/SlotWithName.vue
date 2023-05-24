<template>
  <div class="card">
    <slot name="header">Default Value</slot>
  </div>
  <div class="card">
    <slot name="body">Default Value</slot>
  </div>
  <div class="card">
    <slot name="footer">Default Value</slot>
  </div>
</template>

<script lang="ts">
export default {
  name: 'Video36',
};
</script>

<style scoped>
.flex-component {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
</style>
