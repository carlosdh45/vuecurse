<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <counter start="15" ></counter>

</template>

<script>
import counter from "@/components/counter.vue";

export default {
  name: "App",
  components: {
    counter,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
