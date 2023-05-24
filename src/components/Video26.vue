<!-- methods -->
<template>
  <h2>{{ fullName }}</h2>
  <button @click="changeFullName">Change Fullname</button>
</template>

<script lang="ts">
export default {
  name: 'Video 16',
  data() {
    return {
      firstName: 'Oji',
      lastName: 'Ramadhan',
    };
  },
  methods: {
    changeFullName() {
      this.fullName = 'Clark Kent';
    },
  },
  computed: {
    fullName: {
      get() {
        return `${this.firstName} ${this.lastName}`;
      },
      set(value: string) {
        const names = value.split(' ');
        this.firstName = names[0];
        this.lastName = names[1];
      },
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
