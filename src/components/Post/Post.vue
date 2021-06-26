<template>
<div class="card-container">
  <v-card>
    <HeaderPost
    :author="author"
    :avatar="avatar"
    :date="date"
    :title="title" />

    <div class="text-container">
      <!-- eslint-disable-next-line-->
      <TextBlock :text="text"/>
    </div>
  </v-card>
</div>
</template>

<script>
import HeaderPost from '@/components/Post/HeaderPost.vue';
import TextBlock from '@/components/Post/TextBlock.vue';

export default {
  props: {
    actions: Boolean,
    author: String,
    avatar: String,
    code: String,
    date: String,
    image: String,
    subtext: String,
    text: String,
    title: String,
  },
  components: {
    HeaderPost,
    TextBlock,
  },
};
</script>

<style lang="scss">
@import '@/scss/_settings';
</style>
