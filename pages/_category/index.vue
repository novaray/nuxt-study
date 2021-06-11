<template>
  <div>
    <h2>Category</h2>
  </div>
</template>

<script>
export default {
  name: 'index',
  asyncData(ctx) {
    console.log(ctx.params);
  }
}
</script>

<style scoped>

</style>
