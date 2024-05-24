<script setup>
  import { defineProps, defineModel } from "vue"
defineProps(["type", "id", "label_text", "placeholder"])
const model = defineModel()
</script>

<template>
  <div class="mb-6">
    <label :for="id" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">{{
        label_text
      }}</label>
    <input v-model="model" :type="type" :id="id"
           class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
           :placeholder="placeholder" required/>
  </div>
</template>
