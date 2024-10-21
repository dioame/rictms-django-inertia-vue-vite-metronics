<script setup lang="ts">
import { computed, ref } from "vue";

defineProps<{
  name: string;
}>();

const count = ref(0);
function increment() {
  count.value++;
}

const double = computed(() => count.value * 2);
</script>

<template>
  <div>
    <h1 class="title">Hello {{ name }} from Inertia + Django + Vite + Vue!</h1>
    <button type="button" class="btn btn-dark" @click="increment">Add</button>
    <hr>
    <h1>Count: {{ count }}</h1>
  </div>
</template>

<style scoped>
.title {
  color: green;
}
</style>
