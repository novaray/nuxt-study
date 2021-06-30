<template>
    <el-input class="text-input" placeholder="Please Ip..." :value="value" @input="handleInput">
    </el-input>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'

export default defineComponent({
  name: 'TextInput',
  props: {
    value: String,
  },
  methods: {
    handleInput(data: string) {
      this.$emit('input', data)
    }
  }
})
</script>
