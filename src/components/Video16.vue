<!-- methods -->
<template>
  <template v-for="data in names" v-bind:key="data">
    <h2 v-if="data === 'Dyana' || data === 'Oji'">{{ data }}</h2>
  </template>
  <h2>Add Method - {{ addThree(2, 3, 4) }}</h2>
  <h2>Add Method - {{ addThree(1, 3, 4) }}</h2>
  <h2>Add Method - {{ multiply(10) }}</h2>
</template>

<script lang="ts">
export default {
  name: 'Video 16',
  data() {
    return {
      names: ['Oji', 'Gita', 'Dyana'],
      baseMultiplier: 5,
    };
  },
  methods: {
    addThree(a: number, b: number, c: number) {
      return a + b + c;
    },
    multiply(num: number) {
      return num * this.baseMultiplier;
    },
  },
};
</script>
