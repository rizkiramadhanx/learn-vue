<template>
  <header v-bind:style="[headerStyleObject, headerStyleObject2]">1</header>
  <div v-bind:style="{ color: higlightColor, fontSize: fontSize }">1</div>
</template>

<script lang="ts">
export default {
  name: 'app',
  data() {
    return {
      higlightColor: 'orange',
      fontSize: '40px',
      headerStyleObject: {
        backgroundColor: 'orange',
        height: '200px',
      },
      headerStyleObject2: {
        color: 'red',
      },
    };
  },
};
</script>
