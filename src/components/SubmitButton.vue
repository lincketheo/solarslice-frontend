<script setup>
  import { defineProps } from "vue"
defineProps(["on_click", "text", "disabled"])
</script>

<template>
  <button @click="() => on_click()"
          :disabled="disabled"
          class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
    {{ text }}
  </button>
</template>
