<!-- methods -->
<template>
  <Greet name="Oji" />
  <Greet name="Agil" />
  <Greet :name="name" />
</template>

<script lang="ts">
import Greet from './component/Greet.vue';

export default {
  name: 'Video30',
  data() {
    return {
      name: 'Data Oji',
    };
  },
  components: { Greet },
};
</script>
