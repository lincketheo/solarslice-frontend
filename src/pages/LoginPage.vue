<script setup>
import {ref} from "vue";

import SubmitButton from "@/components/SubmitButton.vue";
import MainLabel from "@/components/MainLabel.vue";
import InputField from "@/components/InputField.vue";

const username = ref("")
const password = ref("")

function on_click_login(_username, _password) {
  localStorage.setItem("Login", _username + ":" + _password)
}
</script>

<template>
  <div class="flex min-h-screen flex-row justify-center items-center">
  <div class="w-96 flex flex-col">
    <MainLabel text="Login:"/>
    <InputField v-model="username" type="text" id="username" label_text="Username" placeholder="Username"/>
    <InputField v-model="password" type="password" id="password" label_text="Password" placeholder="•••••••••"/>
    <div class="flex flex-row justify-end my-5">
      <SubmitButton :on_click="() => on_click_login(username, password)" text="Submit"/>
    </div>
  </div>
  </div>
</template>

