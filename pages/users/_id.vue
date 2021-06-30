<template>
  <div><h1>User</h1>
    <p> User ID : {{ id }} </p></div>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'

export default defineComponent({
  asyncData({params}) {
    console.log(params);
    return {id: params.id};
  },
  validate({params}) {
    return /^\d+$/.test(params.id);
  }
})
</script>
