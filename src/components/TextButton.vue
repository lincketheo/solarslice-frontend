<script setup>
  import { defineProps } from "vue"
defineProps(["on_click", "text"])
</script>

<template>
  <div class="flex flex-row justify-end my-2">
    <button @click="() => on_click()" class="dark:text-white">{{ text }}</button>
  </div>
</template>
