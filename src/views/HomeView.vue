<script setup lang="ts">
import { ref } from 'vue'

const model = ref()
if(location.host.split(".").indexOf("cool") > -1) {
  model.value = "cool"
} else if (location.host.split(".").indexOf("66988") > -1) {
  model.value = "咔咔就是发"
} else if (location.host.split(".").indexOf("127") > -1) {
  model.value = "本地"
}
</script>

<template>
  <main>
    <h1>{{model}}</h1>

    <a v-if="model === 'cool'" class="cool" href="https://coo1.cool">coo1.cool</a>
    <a v-if="model === '咔咔就是发'" class="cool" href="http://66988.cn">66988.cn</a>
    <a v-if="model === '本地'" class="cool" href="http://127.0.0.1:5173/">http://127.0.0.1:5173/</a>
  </main>
</template>

<style scoped>
.cool{
  font-size: 20px;
}
</style>