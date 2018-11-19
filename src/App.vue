<template>
  <div id="app"><img width="25%" src="./assets/logo.png" /> <HelloWorld /></div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import EventHandler from "@/components/EventHandler";
import FormInput from "@/components/EventHandler";

export default {
  name: "App",
  components: {
    HelloWorld,
    EventHandler,
    FormInput
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
