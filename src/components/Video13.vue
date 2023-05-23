<!-- List Rendering -->

<template>
  <div>Halo</div>
  <h2 v-for="(item, index) in names" v-bind:key="item">
    {{ index + 1 }}{{ item }}
  </h2>

  <h2 v-for="(item, index) in fullNames" v-bind:key="index">
    {{ item.first + ' ' + item.last }}
  </h2>

  <div v-for="(actor, index) in actors" :key="index">
    <h2>{{ actor.name }}</h2>
    <div
      :style="{
        display: 'flex',
        flexDirection: 'row',
      }"
    >
      <h3
        :style="{
          marginLeft: '10px',
        }"
        v-for="movie in actor.movies"
        :key="movie"
      >
        {{ movie }}
      </h3>
    </div>

    <h2 v-for="(value, key, index) in info" :key="index">
      {{ index + key + value }}
    </h2>
  </div>
</template>

<script lang="ts">
export default {
  name: 'Video 13',
  data() {
    return {
      names: ['Oji', 'Gita', 'Dyana'],
      fullNames: [
        {
          first: 'Bruce',
          last: 'Wayne',
        },
        {
          first: 'Ajay',
          last: 'Wayne',
        },
        {
          first: 'Singh',
          last: 'Wayne',
        },
      ],

      actors: [
        {
          name: 'Christian Bale',
          movies: ['Batman', 'Love and thunder', 'Poppins'],
        },
        {
          name: 'Ci Caprio',
          movies: ['Titanic', 'Inception'],
        },
      ],

      info: {
        name: 'Rizki',
        ig: 'rizkiramadhanx',
        framework: 'vue js',
      },
    };
  },
};
</script>
