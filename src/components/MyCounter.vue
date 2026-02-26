<template>
  <section>
    <h3>Counter: {{ count }}</h3>
    <h3>Square: {{ square }}</h3>
    <div>
      <button @click="increment">+1</button>
      <button @click="decrement">-1</button>
    </div>
  </section>
</template>

<script lang="ts" setup>
import { ref, computed } from 'vue';

const count = ref(0);
const square = computed(() => count.value * count.value);

const increment = () => {
  count.value++;
};

const decrement = () => {
  count.value--;
};
</script>
