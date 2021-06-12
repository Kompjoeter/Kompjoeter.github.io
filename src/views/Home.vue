<template>
  <div class="home">
    <div class="posts-container">
      <Post date="06-09-2021" title="Regular Post Title"/>
      <Post date="06-08-2021" title="Image Post Title" image="arrow.png"/>
      <Post date="05-30-2021" title="Another Post Title"/>
      <Post code="
      pre {
        display: flex;

        code {
            width: 100% !important;
            border: 1px solid #222;
            color: #a5a714;
            display: block;
            }
      }"
      date="05-29-2021" title="A Nother Post Title"/>
      <Post date="05-22-2021" title="This Is A Post Title" image="face.png"/>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Post from '@/components/Post.vue';

export default {
  name: 'Home',
  components: {
    Post,
  },
};
</script>

<style lang="scss">
@import '../scss/_settings';

  .home {
    display: flex;
    justify-content: center;
    padding: 32px;

    .posts-container {
      display: flex;
      flex-direction: column;
      box-shadow: $shadow-main-light;
      border-radius: 2px;
    }
  }
</style>
