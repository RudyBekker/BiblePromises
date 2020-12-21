<template>
<div>
    <app-header v-bind:title="title"></app-header>
    <app-blog v-bind:posts="posts" />
</div>
</template>

<script>
import JetApplicationLogo from "./../Jetstream/ApplicationLogo";
import PromiseCardList from "./components/PromiseCardList.vue";

export default {
    components: {
        JetApplicationLogo,
        "app-promiseCard": PromiseCardList
    },
}

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
