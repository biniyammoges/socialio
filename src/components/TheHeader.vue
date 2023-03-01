<template>
  <div class="py-4 bg-white">
    <div class="container mx-auto flex justify-between items-center">
      <router-link to="/" class="font-bold text-black text-xl"
        >Socialio</router-link
      >
      <div class="flex items-center">
        <div class="bg-si-gray h-10 rounded-lg mr-3">
          <input
            type="text"
            placeholder="Search"
            class="bg-transparent py-2 px-3 focus:outline-none h-full"
          />
        </div>

        <si-button class="mr-3" variant="default">Create Post</si-button>

        <!-- Profile Pic -->
        <button class="rounded-lg h-10 w-10 overflow-hidden object-cover">
          <img
            src="/avatar5.jpg"
            alt="avatar"
            class="h-full w-full"
            style="object-fit: cover"
          />
        </button>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import SiButton from "./shared/SiButton.vue";
</script>
