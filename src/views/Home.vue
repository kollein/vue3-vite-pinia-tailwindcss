<template>
  <div class="home-page">
    <h1>Home Page</h1>

    <div>Value: {{ counterStore.counter }}</div>
    <div>Double Value: {{ counterStore.doubleCount }}</div>
  </div>
</template>

<script>
import { useCounterStore } from '../stores/counter';

export default {
  name: 'HomeView',
  setup() {
    const counterStore = useCounterStore();

    return {
      counterStore,
    };
  },
};
</script>
