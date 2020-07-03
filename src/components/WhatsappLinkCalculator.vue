<template>
  <div id="whatsapp-link-calculator">
    <h4>Enter phone number:</h4>
    <VuePhoneNumberInput
      v-model="phoneNumber"
      @update="results = ($event)"
      default-country-code="IL"
    />
    <OutputUrl :phoneInputResults="results" />
  </div>
</template>

<script>
import VuePhoneNumberInput from "vue-phone-number-input";
import OutputUrl from "./OutputUrl.vue";

export default {
  name: "WhatsappLinkCalculator",
  components: {
    VuePhoneNumberInput,
    OutputUrl
  },
  data: () => {
    return {
      phoneNumber: "",
      results: {}
    };
  }
};
</script>

<style src="vue-phone-number-input/dist/vue-phone-number-input.css">
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
