<template>
  <header class="relative">
    Header

    <button class="bg-green-100 p-2 rounded" @click="counterStore.increment">+1</button>
  </header>

  <router-view />
</template>

<script>
import { useCounterStore } from './stores/counter';

export default {
  name: 'App',
  setup() {
    const counterStore = useCounterStore();

    return {
      counterStore,
    };
  },
};
</script>

<style>
@import '@/styles/index.scss';
</style>
