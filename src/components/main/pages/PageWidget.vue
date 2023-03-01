<template>
  <div class="flex-1">
    <h4 class="text-si-dark px-4">Your pages</h4>
    <div class="bg-white rounded-lg mt-2 py-4 px-4">
      <ThePage v-for="page in pages" :key="page.id" :page="page" />
    </div>
  </div>
</template>

<script lang="ts" setup>
import { ref } from "vue";
import { Page } from "./page-interface";
import ThePage from "./ThePage.vue";

const pages = ref<Page[]>([
  { id: "1", photo: "/story1.jpg", name: "Grand techs", unreadCount: 9 },
  { id: "2", photo: "/story2.jpg", name: "Tech Talk With Abdi" },
  { id: "3", photo: "/story3.jpg", name: "Haile Fashion Show" },
  { id: "4", photo: "/story4.jpg", name: "Bini Shoes" },
]);
</script>
