<template>
  <div>
    <h1>Having fun with loaders</h1>
  </div>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'

export default defineComponent({
  /*
   ** programmatically start the loader so we force the page to take x2seconds to load
   */
  loading: false,
  transition: 'fade',
  mounted() {
    this.$nextTick(() => {
      this.$nuxt.$loading.start();
      setTimeout(() => this.$nuxt.$loading.finish(), 2000);
    });
  },
})
</script>
