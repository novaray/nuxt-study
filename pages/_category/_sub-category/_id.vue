<template>
  <div>
    <h2>Sub-Category: ID</h2>
    <p>
      ID: {{id}}
    </p>
  </div>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'

export default defineComponent({
  asyncData({params}) {
    console.log(params);
    return {
      id: params.id
    };
  }
})
</script>

<style scoped>

</style>
