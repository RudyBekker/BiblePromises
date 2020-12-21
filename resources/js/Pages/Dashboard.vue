<template>
  <app-layout>
    <div class="justify-center">
      <welcome />
    </div>
  </app-layout>
</template>

<script>
import AppLayout from "./../Layouts/AppLayout";
import Welcome from "./../Jetstream/Welcome";

export default {
  components: {
    AppLayout,
    Welcome,
  },
};
</script>
