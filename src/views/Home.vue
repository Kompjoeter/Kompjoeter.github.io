<template>
  <div class="home">
    <div class="posts-container">
      <Post
      :actions="false"
      author="Joran de Boer"
      avatar="me.png"
      date="June 12, 2021"
      title="Dawn"
      eslint-disable-next-line
      text="This is no blog.
      This is a 'perpetual work-in-progress'. Welcome aboard."/>

      <Post
      :actions="false"
      author="Joran de Boer"
      avatar="me.png"
      date="June 12, 2021"
      title="Irrelevance"
      eslint-disable-next-line
      text="This is a temporary post. How has your day been?"/>

      <Post
      :actions="false"
      author="Joran de Boer"
      avatar="me.png"
      date="June 12, 2021"
      title="Obsolete"
      eslint-disable-next-line
      text="This is a temporary post. Have you tried Battlefield 1?"/>
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
      flex-direction: column-reverse;
      border-radius: 2px;
    }
  }
</style>
