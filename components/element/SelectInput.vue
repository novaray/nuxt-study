<template>
  <el-select :value="value" @change="handleChange" placeholder="Select User">
    <el-option v-for="(option, index) in options" :key="index" :label="option[labelName]" :value="option[valueName]">
    </el-option>
  </el-select>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'

export default defineComponent({
  name: 'SelectInput',
  props: {
    options: Array,
    labelName: String,
    valueName: String,
    value: [String, Number]
  },
  methods: {
    handleChange(data: any) {
      this.$emit('input', data)
    }
  }
})
</script>

<style scoped>

</style>
