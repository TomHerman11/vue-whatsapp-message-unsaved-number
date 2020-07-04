<template>
  <div id="whatsapp-link-calculator">
    <h3>Enter phone number:</h3>
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
import "vue-phone-number-input/dist/vue-phone-number-input.css";
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

<style scoped>
</style>
