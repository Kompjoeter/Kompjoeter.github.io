<template>
  <div class="home">
    <div class="posts-container">
      <Post
      :actions="false"
      date="12-06-2021"
      title="Dawn"
      text="This is not a blog. This is a 'perpetual work-in-progress'. Welcome aboard."
      subtext='"Earth to the internet! Do you read me?"'/>
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
