<template>
  <div class="outputUrl">
    <a
      v-if="phoneInputResults.isValid"
      class="link-button"
      :href="phoneInputResults.isValid ? 'https://api.whatsapp.com/send?phone=' + phoneInputResults.formattedNumber.substring(1) : ''"
      target="_blank"
    >Message</a>
    <p v-else class="link-button">Message</p>
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
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.link-button {
  padding: 10px 10px;
  border-style: solid;
  border-radius: 10px;
}
a.link-button {
  color: #42b983;
}

p.link-button {
  color: #c0c0c0;
}
</style>
