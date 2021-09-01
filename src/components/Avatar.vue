<template>
      <v-avatar
      color="orange"
      size="42"
    >
      <v-img v-if="img" :src="img"></v-img>
      <span v-if="!img" class="white--text text-h5">{{initials}}</span>
    </v-avatar>
</template>

<script>
export default {
  props: {
    author: String,
    img: String,
  },
  computed: {
    initials() {
      const i = this.author.match(/\b(\w)/g);
      return i.join('');
    },
  },
};
</script>

<style>

</style>
