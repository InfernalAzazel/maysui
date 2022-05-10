<template>
  <div id="d">
    <m-button>
      <template #icon>O</template>
      点击666
    </m-button>
    <input class="border-2 border-rose-600 ...">
  </div>
</template>

<script setup lang="ts">
import {MButton} from "../packages";
</script>

<style>
#d {
  @apply bg-amber-200 h-screen w-screen;
}
</style>
