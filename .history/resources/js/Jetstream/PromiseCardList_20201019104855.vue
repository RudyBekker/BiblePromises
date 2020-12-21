<template>
  <li>
    <h2>{{ post.title }}</h2>
    <div class="post-body">{{ post.body }}</div>
    <button type="button" 
      class="delete-btn" 
      @click="deletePost(post)">
      Delete
    </button>  
  </li>
</template>

<script>
export default {
  props: {
    post: {
      type: Object,
      required: true
    }
  },

  data() {
    return {};
  },
};
</script>
