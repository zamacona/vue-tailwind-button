<script>
import { defineComponent } from 'vue';
import VueTailwindButton from '@/vue-tailwind-button.vue';

export default defineComponent({
  name: 'ServeDev',
  components: {
    VueTailwindButton
  }
});
</script>

<template>
  <div id="app">
    <vue-tailwind-button />
  </div>
</template>
