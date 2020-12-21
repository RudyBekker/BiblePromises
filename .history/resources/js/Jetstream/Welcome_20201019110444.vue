<template>
<div>
    <t v-bind:posts="posts" />
</div>
</template>

<script>
import JetApplicationLogo from "./../Jetstream/ApplicationLogo";
import PromiseCardList from "./components/PromiseCardList";

export default {
    components: {
        JetApplicationLogo,
        PromiseCardList,
    },
</script>