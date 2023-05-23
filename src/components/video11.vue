<!-- Conditional Rendering -->

<template>
  <h1 v-if="num === 0">The number is zero</h1>
  <h1 v-else-if="num < 0">The number is negatif</h1>
  <h1 v-else="num === 0">The number is not zero</h1>

  <h1 v-show="show">This is V-SHOW</h1>
</template>

<script lang="ts">
export default {
  // name: 'Video11',
  data() {
    return {
      num: -1,
      show: true,
    };
  },
};
</script>
