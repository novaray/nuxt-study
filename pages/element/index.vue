<template>
  <div>
    <h1>Welcome Element UI</h1>
    <TextInput v-model="input1" />
    <SelectInput v-model="selectedValue" :options="users" label-name="name" valueName="id" />
  </div>
</template>

<script lang="ts">
import {defineComponent, useContext, ref, useFetch } from '@nuxtjs/composition-api'

export default defineComponent({
  name: 'index',
  data() {
    return {
      input1: '32425232',
      selectedValue: 1
    }
  },
  setup() {
    const { $axios } = useContext()
    const users = ref([])

    const { fetch, fetchState } = useFetch(async () => {
      users.value = (await $axios.get('/api/v1/users')).data
    })

    fetch()

    return { users }
  }
})
</script>

<style scoped>

</style>
