<template>
  <div class="h-screen flex flex-col justify-center items-center">
    <h1 class="text-xl font-bold text-blue-900">Contador</h1>
    <!-- v-bind -->
    <MyCounter :value="5" />
    <MyCounter :value="5" />
  </div>
</template>

<script lang="ts" setup>
import MyCounter from './Components/MyCounter.vue';
</script>
