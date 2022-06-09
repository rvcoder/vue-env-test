<template>
  <div id="app">
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <H2>{{ title }}</H2>
    <p>URL:{{ url }}</p>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
  },
  data() {
    console.log(process.env);
    return {
      url: process.env.VUE_APP_URL,
      title: process.env.VUE_APP_TITLE,
    };
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
