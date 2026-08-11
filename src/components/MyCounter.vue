<template>
  <section>
    <h3>Contador {{ count }}</h3>
    <h3>Cuadrado {{ squared }}</h3>
    <!-- v-on:click -->
    <button @click="count++">+1</button>
    <button @click="count--">-1</button>
  </section>
</template>

<script lang="ts" setup>
import { ref, computed } from 'vue';

/* Typescript */
interface Props {
  value: number;
}
const props = defineProps<Props>();

/* JS
const props = defineProps({
  value: { type: Number, required: true },
});
*/

/* Variable reactiva */
const count = ref(props.value);
/* Variable computada */
const squared = computed(() => count.value * count.value);
</script>
