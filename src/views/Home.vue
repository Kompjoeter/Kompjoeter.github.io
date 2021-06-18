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
      This is a <i>'perpetual work-in-progress'.</i> Welcome aboard."/>

    <Post
      :actions="false"
      author="Joran de Boer"
      avatar="me.png"
      date="June 17, 2021"
      title="TIL: Raw-HTML"
      :text="post"
    />
      </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Post from '@/components/Post/Post.vue';

export default {
  name: 'Home',
  components: {
    Post,
  },
  created() {
    fetch('https://raw.githubusercontent.com/Kompjoeter/Github-Hosted-Blog/master/posts.json')
      .then((response) => response.json())
      .then((data) => console.log(data));
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
