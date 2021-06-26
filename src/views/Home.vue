<template>
  <div class="home">
    <div class="posts-container">
      <span v-for="(item, index) in posts" :key="index">
        <Post
        author="Joran de Boer"
        :avatar="true"
        :date="item.date"
        :text="item.text"
        :title="item.title"
        />
      </span>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Post from '@/components/Post/Post.vue';

export default {
  name: 'Home',
  data() {
    return {
      posts: [],
    };
  },
  components: {
    Post,
  },
  created() {
    this.getPosts();
  },
  methods: {
    getPosts() {
      fetch('https://raw.githubusercontent.com/Kompjoeter/kompjoeter.github.io/main/posts/posts.json')
        .then((response) => response.json())
        .then((data) => {
          this.posts = data;
          this.getPostContent();
        });
    },
    getPostContent() {
      this.posts.forEach((post, index) => {
        fetch(post.file)
          .then((response) => response.text())
          .then((content) => {
            this.posts[index].text = content;
          });
      });
    },
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
