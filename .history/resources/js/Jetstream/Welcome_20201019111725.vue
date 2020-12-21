<template>
<div>
    <PromiseCardList v-bind:posts="posts" />
</div>
</template>

<script>
import JetApplicationLogo from "./../Jetstream/ApplicationLogo";
import JetApplicationLogo from "./../Jetstream/PromiseCardList";


export default {
    components: {
        JetApplicationLogo,
        PromiseCardList,
    },
      data() {
    return {
      title: "Posts",
      posts: []
    };
  },

  methods: {
    fetchPosts() {
      fetch("https://jsonplaceholder.typicode.com/posts")
        .then(response => response.json())
        .then(posts => {
          this.posts = posts;
        });
    }
  },

  created() {
    this.fetchPosts();
  }
};
</script>