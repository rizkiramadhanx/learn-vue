<!-- methods -->
<template>
  <!-- from computed -->
  <h2>Full name - {{ fullName }}</h2>
  <div v-for="item in items" :key="item.id">
    <h2>{{ item.title }}</h2>
  </div>

  <h2>{{ getTotal() }}</h2>

  <button @click="addItem">Add Item</button>
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
  methods: {
    addItem() {
      this.items.push({
        id: 5,
        price: 200,
        title: 'Laptop',
      });
    },
    getTotal() {
      console.log('from methods');
      return this.items.reduce(
        (total, curr) => (total = total + curr.price),
        0
      );
    },
  },
  computed: {
    fullName() {
      return `${this.firstName} ${this.lastName} `;
    },
    total() {
      console.log('from computed');
      return this.items.reduce(
        (total, curr) => (total = total + curr.price),
        0
      );
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
