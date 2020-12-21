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
    export default {
        components: {
            JetApplicationLogo,
        },
    }
</script>
