<template>
  <div>{{ provideAuthor }}</div>
</template>

<script lang="ts">
export default {
  name: 'Inject',
  inject: ['provideAuthor'],
};
</script>
