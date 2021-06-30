<template>
  <div>
    <h2>Category</h2>
  </div>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'

export default defineComponent({
  name: 'index',
  asyncData(ctx) {
    console.log(ctx.params);
  }
})
</script>

<style scoped>

</style>
