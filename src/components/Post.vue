<template>
<div class="card-container">
  <v-card>
    <div class="image-container">
    <img v-if="avatar" class="avatar" :src="require(`@/assets/${avatar}`)">
    </div>

    <div class="text-container">
      <v-card-title>{{ title }}</v-card-title>
      <v-card-subtitle>By {{author}} on {{date}}</v-card-subtitle>
      <!-- eslint-disable-next-line-->
      <v-card-text>{{text}}</v-card-text>
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
};
</script>

<style lang="scss">
@import '../scss/_settings';
</style>
