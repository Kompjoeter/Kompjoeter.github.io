<template>
<div class="card-container">
  <v-card>
    <div v-if="image" class="image-container">
    <v-img max-width="300px" :src="require('@/assets/'+image+'')"></v-img>
    </div>

    <div class="text-container">
      <v-card-title>{{ title }}</v-card-title>
      <v-card-subtitle>{{date}}</v-card-subtitle>
      <!-- eslint-disable-next-line-->
      <v-card-text>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Vitae illum sit provident nostrum dolore, nulla earum velit odio autem veritatis, nisi unde excepturi! Impedit qui suscipit totam commodi nihil dolorem aliquam distinctio labore, placeat voluptatibus quaerat accusantium? Facere, id nulla aspernatur eum iusto sunt harum dignissimos officiis itaque. Dolore?</v-card-text>
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
      <v-card-actions>
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
    code: String,
    date: String,
    image: String,
    title: String,
  },
};
</script>

<style lang="scss">
@import '../scss/_settings';
</style>
