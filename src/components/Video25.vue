<!-- methods -->
<template>
  <h2>Without computed</h2>
  <template v-for="item in items" :key="item.id">
    <h2 v-if="item.price > 100">{{ item.title }}</h2>
  </template>

  <h2>With computed</h2>
  <template v-for="item in expensiveItems" :key="item.id">
    <h2 v-if="item.price > 100">{{ item.title }}</h2>
  </template>
</template>

<script lang="ts">
export default {
  name: 'Video 16',
  data() {
    return {
      firstName: 'Oji',
      lastName: 'Ramadhan',
      items: [
        {
          id: 1,
          title: 'TV',
          price: 100,
        },
        {
          id: 2,
          title: 'Phone',
          price: 200,
        },
        {
          id: 3,
          title: 'CD',
          price: 400,
        },
      ],
    };
  },
  methods: {},
  computed: {
    expensiveItems() {
      return this.items.filter((item) => item.price > 100);
    },
  },
};
</script>

<style scoped>
input {
  padding: 4px;
}
input:focus {
  outline: none;
}

.tall-select {
  height: 100px;
}

select {
  height: 30px;
}

select:focus {
  outline: none;
}

.form-group {
  display: flex;
  flex-direction: column;
  gap: 4px;
}
</style>
