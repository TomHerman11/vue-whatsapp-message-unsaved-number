<template>
  <div class="outputUrl">
    <button v-if="phoneInputResults.isValid" class="link-button" v-on:click="onButtonClick">Message</button>
    <button v-else class="link-button" disabled>Message</button>
  </div>
</template>

<script>
export default {
  name: "OutputUrl",
  props: {
    phoneInputResults: {
      type: Object,
      default: () => ({ type: "" })
    }
  },
  methods: {
    onButtonClick: function() {
      window.open(
        "https://api.whatsapp.com/send?phone=" +
          this.phoneInputResults.formattedNumber.substring(1),
        "_blank"
      );
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.link-button {
  margin: 2.5vh 0px;
  padding: 10px 100px;
  border-style: solid;
  border-radius: 10px;
  outline: none;
  cursor: pointer;
  background-color: #aaffba;
}
button:disabled,
button[disabled] {
  cursor: default;
  background-color: #fafafa;
  border-color: #d2d2d2;
  color: #d2d2d2;
}
</style>
