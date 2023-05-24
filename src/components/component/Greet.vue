<template>
  <h1>Hello {{ name }}</h1>
</template>

<script lang="ts">
export default {
  name: 'Greet',
  props: {
    name: {
      type: String,
      required: true,
    },
  },
};
</script>
