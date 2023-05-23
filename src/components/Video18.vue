<!-- methods -->
<template>
  <h1>Count : {{ count }}</h1>
  <button @click="increment(5, $event)">Add 5</button>

  <button @click="increment(undefined, $event)">Add</button>
  <button @click="decrement()">Minus</button>
  <button @click="decrement(5)">Minus 5</button>

  <hr />
  <h2>{{ name }}</h2>

  <button @click="changeName">Change Name</button>
</template>

<script lang="ts">
export default {
  name: 'Video 16',
  data() {
    return {
      name: 'Oji',
      count: 0,
      baseMultiplier: 5,
    };
  },
  methods: {
    changeName(Event: MouseEvent) {
      console.log(Event);
      this.name = 'Batman';
    },
    increment(num: number = 1, Event: MouseEvent) {
      console.log(Event);
      this.count = this.count + num;
    },
    decrement(num: number = 1) {
      this.count = this.count - num;
    },
  },
};
</script>
