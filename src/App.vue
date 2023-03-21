<script>
import AppHeader from "@/components/AppHeader.vue";
import ContactBook from "./views/ContactBook.vue";

export default {
  components: {
    AppHeader,
    ContactBook,
  },
};
</script>
<template>
  <div id="app">
    <app-header />
    <div class="container mt-3">
      <router-view />
    </div>
  </div>
</template>
<style>
.page {
  max-width: 400px;
  margin: auto;
}
</style>