<template>
  <v-card-text>
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
