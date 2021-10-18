<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <Demo />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <DemoVue content="Xin chào Vue" />
    <CauDieuKien/>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import DemoVue from "./components/DemoVue.vue";
import Demo from "./components/ColorChange.vue";
import CauDieuKien from "./components/V_IF.vue";
export default {
  name: "App",
  components: {
    HelloWorld,
    DemoVue,
    Demo,
    CauDieuKien,
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
