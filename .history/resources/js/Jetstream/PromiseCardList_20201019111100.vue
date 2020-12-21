<template>
<div class="posts-wrapper">
    <ul>
        <blog-item v-for="post in posts" :key="post.id" :post="post" @deletePost="deletePost" />
    </ul>
</div>
</template>

<script>
import PromiseCard from "./PromiseCard.vue";

export default {
    props: {
        posts: {
            type: Array,
            required: true
        }
    },

    components: {
        PromiseCard
    },

    data() {
        return {};
    },

    methods: {
        deletePost(post) {
            let ind = this.posts.indexOf(post);

            if (ind !== -1) {
                this.posts.splice(ind, 1);
            }
        }
    }
};
</script>

<style scoped>
.posts-wrapper {
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 40px 20px;
    box-sizing: border-box;
    min-height: 600px;
    background-color: #eee;
}

ul {
    display: flex;
    flex-wrap: wrap;
    list-style-type: none;
    padding: 0;
}
</style>
