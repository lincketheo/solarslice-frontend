<script setup>
  import {defineProps } from "vue"
defineProps(["text", "on_click_exit", "color"])
</script>

<template>
  <div class="w-96 flex flex-row justify-start mt-10">
    <p class="pr-10 font-bold" :class="color">{{ text }}</p>
    <button @click="on_click_exit">X</button>
  </div>
</template>
