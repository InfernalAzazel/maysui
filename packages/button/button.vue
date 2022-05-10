<template>
  <button :class="[type]">
    <slot name="icon"/>
    <slot/>
  </button>
</template>
<script setup lang="ts">
import { ref, } from 'vue'
const buttonType = ['primary','dashed', 'text', 'link']
interface Props{
  msg?:string
  type?:string
}
withDefaults(defineProps<Props>(), {
  msg: '900',
  type: 'primary'
})
defineEmits([])
defineExpose({})
</script>

<style scoped>
.primary{
  @apply dark:bg-sky-600;
  @apply w-32 h-10 text-white cursor-pointer;
  @apply border-dashed border-2 border-indigo-600;
  @apply border;
}
.dashed{
  @apply bg-sky-500 w-32 h-8 text-white;
  @apply border;
}
</style>
