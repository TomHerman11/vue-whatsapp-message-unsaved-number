<template>
  <div id="app">
    <img class="whatsapp_logo" alt="WhatsApp logo" src="./assets/whatsapp_logo.png" />
    <h1>Message Unsaved Number Using WhatsApp</h1>
    <WhatsappLinkCalculator />
  </div>
</template>

<script>
import WhatsappLinkCalculator from "./components/WhatsappLinkCalculator.vue";

export default {
  name: "App",
  components: {
    WhatsappLinkCalculator
  }
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

.whatsapp_logo {
  width: 30vmin;
}
</style>
