<template>
<li>
    <h2>{{ post.title }}</h2>
    <div class="post-body">{{ post.body }}</div>
    <button type="button" class="delete-btn" @click="deletePost(post)">
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

    methods: {
        deletePost(post) {
            this.$emit("deletePost", post);
        }
    }
};
</script>

<style scoped>
li {
    flex-grow: 1;
    flex-basis: 300px;
    text-align: center;
    padding: 30px;
    border: 1px solid #222;
    margin: 10px;
    background-color: #fff;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

.post-body {
    padding: 10px 0;
}

.delete-btn {
    padding: 10px;
    cursor: pointer;
}
</style>
