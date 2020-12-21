<template>
  <div>
    <app-header v-bind:title="title"></app-header>
    <app-blog
      v-bind:posts="posts"      
    />
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
</script>
