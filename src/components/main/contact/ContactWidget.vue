<template>
  <div class="flex-1">
    <h4 class="text-si-dark px-4">Active Friends</h4>
    <div class="bg-white rounded-lg mt-2 py-4 px-4">
      <TheContact v-for="friend in friends" :key="friend.id" :friend="friend" />
    </div>
  </div>
</template>

<script lang="ts" setup>
import { ref } from "vue";
import { Contact } from "./contact-interface";
import TheContact from "./TheContact.vue";

const friends = ref<Contact[]>([
  { id: "1", photo: "/story1.jpg", name: "Grand techs", status: "active" },
  {
    id: "2",
    photo: "/story2.jpg",
    name: "Tech Talk With Abdi",
    status: "active",
  },
  {
    id: "3",
    photo: "/story3.jpg",
    name: "Haile Fashion Show",
    status: "active",
  },
  { id: "4", photo: "/story4.jpg", name: "Bini Shoes", status: "active" },
]);
</script>
