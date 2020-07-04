<template>
  <div id="app">
    <link href="https://fonts.googleapis.com/css?family=Cardo:400,700|Oswald" rel="stylesheet" />
    <h1>Send Messages to Unsaved Numbers Using WhatsApp</h1>
    <img class="whatsapp_logo" alt="WhatsApp logo" src="./assets/whatsapp_logo.png" />
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
  font-family: "Cardo", serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  color: #2c3e50;
  margin-top: 60px;
}

body {
  background-color: #eafeea;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: "Oswald", sans-serif;
  text-transform: uppercase;
}

.whatsapp_logo {
  width: 30vmin;
}
</style>
