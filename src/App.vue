<template>
  <div id="app">
    <button @click="currentComponent = HelloWorld">HelloWorld</button>
    <button @click="currentComponent = HelloVue">HelloVue</button>
    <component :is="currentComponent"/>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import HelloVue from "./components/HelloVue";

export default {
  name: "App",
  data() {
    return {
      HelloWorld,
      HelloVue,
      currentComponent: HelloWorld
    };
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
}
</style>
