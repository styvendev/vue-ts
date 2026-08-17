<template>
  <section class="text-center m-5">
    <h3 class="text-lg">Valor {{ count }}</h3>
    <h3 class="text-lg">Cuadrado {{ squared }}</h3>
    <!-- v-on:click -->
    <button class="btn" @click="count++">+1</button>
    <button class="btn" @click="count--">-1</button>
  </section>
</template>

<script lang="ts" setup>
import { ref, computed } from 'vue';

/* JS
const props = defineProps({
  value: { type: Number, required: true },
});
*/

/* Typescript */
interface Props {
  value: number;
}
const props = defineProps<Props>();

/* Variable reactiva */
const count = ref(props.value);
/* Variable computada */
const squared = computed(() => count.value * count.value);
</script>
