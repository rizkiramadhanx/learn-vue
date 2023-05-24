<!-- methods -->
<template>
  <h3>Current volume - {{ movie }}</h3>
  <input type="text" v-model="movie" />
  <input type="text" v-model="movieInfo.title" />
  <input type="text" v-model="movieInfo.actor" />
</template>

<script lang="ts">
export default {
  name: 'Video 16',
  data() {
    return {
      movie: 'Batman',
      movieInfo: {
        title: '',
        actor: '',
      },
    };
  },
  methods: {},
  watch: {
    movie: {
      handler(newValue) {
        console.log(`Calling API with movie, with name = ${newValue}`);
      },
      immediate: true,
    },

    movieInfo: {
      handler(newValue) {
        console.log(
          `Calling API with movie title = ${newValue.title} and actor = ${newValue.actor}`
        );
      },
      deep: true,
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
