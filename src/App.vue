<template>
  <div id="app">
    <counterValue :value="count"></counterValue>
    <button v-on:click="increment">increment</button>
    <button v-on:click="decrement">decrement</button>
  </div>
</template>

<script>
import counterValue from "./Counter";

export default {
  name: "App",
  components: {
    counterValue
  },
  // state
  data() {
    return {
      count: 2
    };
  },
  // actions
  methods: {
    increment() {
      this.count++;
    },
    decrement() {
      this.count--;
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  font-size: 300%;
}
button {
  font-size: 2rem;
  margin: 0 0.5rem;
}
</style>
