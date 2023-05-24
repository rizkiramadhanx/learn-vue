<template>
  <div class="flex-component">
    <SlotWithNameVue>
      <template v-slot:header>
        <h3>Hahahah</h3>
      </template>
      <template v-slot:body>
        <h3>Body</h3>
      </template>
      <template v-slot:footer>
        <h3>Footer</h3>
      </template>
    </SlotWithNameVue>
  </div>
</template>

<script lang="ts">
import SlotWithNameVue from './component/SlotWithName.vue';
export default {
  name: 'Video36',
  components: {
    SlotWithNameVue,
  },
};
</script>

<style scoped>
.flex-component {
  display: flex;
  flex-direction: column;
  gap: 10px;
}
</style>
