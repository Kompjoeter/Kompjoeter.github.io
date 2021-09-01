<template>
  <div class="post-header">
    <div class="header-container">
      <div class="avatar-container">
          <Avatar :author="author" :img="avatar" class="avatar"/>
        </div>
        <div class="titles-container">
          <v-card-title>{{ title }}</v-card-title>
          <v-card-subtitle>By {{author}} on {{date}}</v-card-subtitle>
        </div>
    </div>
  </div>
</template>

<script>
import Avatar from '@/components/Avatar.vue';

export default {
  components: {
    Avatar,
  },
  props: {
    author: String,
    avatar: String,
    date: String,
    title: String,
    post: Object,
  },
};
</script>

<style lang="scss">
@import '@/scss/_settings';

</style>
