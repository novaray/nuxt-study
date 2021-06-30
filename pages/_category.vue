<template>
  <div>
    <h1>Category</h1>
    <p>
      Category: {{category}}
    </p>
    <NuxtChild />
  </div>
</template>

<script lang="ts">
import {Context} from '@nuxt/types';
import { defineComponent } from '@nuxtjs/composition-api'

export default defineComponent({
  asyncData(ctx: Context): Promise<object | void> | object | void {
    return {
      category: ctx.params.category
    };
  }
})
</script>

<style scoped>

</style>
