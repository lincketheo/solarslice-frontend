<script setup>
  import { defineProps } from "vue"
defineProps(["text"])
</script>

<template>
  <h1 class="text-2xl font-bold dark:text-white">{{ text }}</h1>
</template>
