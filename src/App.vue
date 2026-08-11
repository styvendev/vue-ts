<template>
  <h1>Contador</h1>
  <!-- v-bind -->
  <MyCounter :value="5" />
</template>

<script lang="ts" setup>
import MyCounter from './Components/MyCounter.vue';
</script>
