<template>
  <div class="flex-component">
    <Slot>Cuaks</Slot>
    <Slot></Slot>
    <Slot>
      <img src="https://dummyimage.com/600x400/000/fff" />
    </Slot>
  </div>
</template>

<script lang="ts">
import Slot from './component/Slot.vue';
export default {
  name: 'Video35',
  components: {
    Slot,
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
