<template>
  <div>
    <h1>Category</h1>
    <p>
      Category: {{category}}
    </p>
    <NuxtChild />
  </div>
</template>

<script>
export default {
  asyncData(ctx) {
    return {
      category: ctx.params.category
    };
  }
}
</script>

<style scoped>

</style>
