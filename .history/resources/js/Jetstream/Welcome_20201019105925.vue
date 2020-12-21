<template>
<div>
    <app-header v-bind:title="title"></app-header>
    <app-blog v-bind:posts="posts" />
</div>
</template>

<script>
import PromiseCardList from "./components/PromiseCardList";

export default {
    components: {
        "app-header": Header,
        "app-blog": BlogList
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

<!-- global styles -->

<style>
body {
    margin: 0;
    font-family: "Nunito SemiBold";
}
</style>
