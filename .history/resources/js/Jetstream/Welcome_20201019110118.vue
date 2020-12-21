<template>
<div>
    <app-promiseCard v-bind:posts="posts"</app-promiseCard>
</div>
</template>

<script>
import JetApplicationLogo from "./../Jetstream/ApplicationLogo";
import PromiseCardList from "./components/PromiseCardList";

export default {
    components: {
        JetApplicationLogo,
        "app-promiseCard": PromiseCardList,
    },
</script>