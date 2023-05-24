<!-- methods -->
<template>
  <h3>Current volume - {{ volume }}</h3>
  <button @click="increaseVolume">Increase</button>
  <button @click="decreaseVolume">Decrease</button>
</template>

<script lang="ts">
export default {
  name: 'Video 16',
  data() {
    return {
      volume: 0,
    };
  },
  methods: {
    increaseVolume() {
      this.volume = this.volume + 1;
    },
    decreaseVolume() {
      this.volume = this.volume - 1;
    },
  },
  watch: {
    volume(newValue, oldValue) {
      console.log(oldValue, newValue);
      if (newValue === 16) {
        alert('tidak boleh');
      }
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
