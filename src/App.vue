<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <div>{{ count }}</div>
  <div>{{ double }}</div>
  <button @click="increase">👍+1</button>
</template>

<script lang="ts">
import { computed, defineComponent, reactive, ref } from 'vue';
import HelloWorld from './components/HelloWorld.vue';

export default defineComponent({
  name: 'App',
  setup() {
    const data = reactive({
      count: 0,
      double: computed(() => data.count * 2),
      increase: () => {
        data.count++;
      },
    });
  },
});
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
