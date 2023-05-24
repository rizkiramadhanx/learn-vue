<!-- methods -->
<template>
  <Inject />
</template>

<script lang="ts">
import Inject from './component/Inject.vue';

export default {
  name: 'Video30',
  data() {
    return {
      author: 'Ojai',
    };
  },
  provide() {
    return {
      provideAuthor: this.author,
    };
  },
  components: { Inject },
};
</script>
