<template>
  <div class="bg-si-gray min-h-screen w-screen">
    <the-header></the-header>
    <div class="container mx-auto flex items-start mt-4">
      <the-sidebar class="shrink"></the-sidebar>
      <router-view></router-view>
    </div>
  </div>
</template>

<script lang="ts" setup>
import TheHeader from "./components/TheHeader.vue";
import TheSidebar from "./components/TheSidebar.vue";
</script>
