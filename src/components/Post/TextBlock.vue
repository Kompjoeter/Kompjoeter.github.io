<template>
  <v-card-text id="text-container">
      <span v-html="text">
      </span>
  </v-card-text>
</template>

<script>
export default {
  props: {
    text: String,
  },
};
</script>

<style>

</style>
