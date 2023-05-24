<template>
  <Popup v-if="showPopup" @close="fromPop" />
  <button @click="setShowPopup">Open Popup</button>
</template>

<script lang="ts">
import Popup from './component/Popup.vue';
export default {
  name: 'Video34',
  components: {
    Popup,
  },
  data() {
    return {
      showPopup: false,
    };
  },
  methods: {
    setShowPopup() {
      this.showPopup = true;
    },
    fromPop(name: string) {
      console.log('halo', name);
      this.showPopup = false;
    },
  },
};
</script>
