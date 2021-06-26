<template>
<div class="card-container">
  <v-card>
    <div class="image-container">
    <Avatar :author="author" class="avatar"/>
    <v-img v-if="image" max-width="300" :src="require(`@/assets/${image}`)"></v-img>
    </div>

    <div class="text-container">
      <v-card-title>{{ title }}</v-card-title>
      <v-card-subtitle>By {{author}} on {{date}}</v-card-subtitle>
      <!-- eslint-disable-next-line-->
      <TextBlock :text="text"/>
       <div v-if="code" class="code">
        <v-card-subtitle>CSS</v-card-subtitle>
       <v-card-text>
        <pre>
          <code>
            {{code}}
          </code>
        </pre>
      </v-card-text>
       </div>
      <v-card-actions v-if="actions">
        <v-btn class="primary">Primary</v-btn>
        <v-btn class="secondary">Secondary</v-btn>
      </v-card-actions>
    </div>
  </v-card>
</div>
</template>

<script>
import Avatar from '@/components/Avatar.vue';
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
    Avatar,
    TextBlock,
  },
};
</script>

<style lang="scss">
@import '@/scss/_settings';
</style>
