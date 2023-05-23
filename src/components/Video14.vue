<template>
  <template v-for="(data, index) in names" v-bind:key="data">
    <h2>{{ data + index }}</h2>
    <input type="text" placeholder="last name" />
    <hr />
  </template>
  <button @click="shuffle">Ha</button>
</template>

<script lang="ts">
import _ from 'lodash';
export default {
  name: 'video14',
  data() {
    return {
      names: ['Oji', 'Gita', 'Dyana'],
    };
  },
  methods: {
    shuffle() {
      console.log(this.names);
      this.names = _.shuffle(this.names);
    },
  },
};
</script>
