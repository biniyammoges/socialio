<template>
  <div class="flex items-start flex-1">
    <div style="max-width: 600px" class="mr-4">
      <!-- storeies -->

      <StoryWidget />
      <!-- post form -->
      <div
        class="bg-white flex items-center justify-between rounded-lg py-3 px-2 mt-4 shadow-sm"
      >
        <button class="rounded-lg h-10 w-10 overflow-hidden object-cover">
          <img
            src="/avatar5.jpg"
            alt="avatar"
            class="h-full w-full"
            style="object-fit: cover"
          />
        </button>
        <input
          type="text"
          placeholder="What's new today?"
          class="focus:outline-none h-full flex-1 px-3"
        />
        <SiButton class="whitespace-nowrap">Post It!</SiButton>
      </div>

      <!-- posts -->
      <PostWidget class="mt-4" />
    </div>

    <div class="flex-1">
      <PageWidget />
      <!-- <PageWidget class="mt-4" /> -->
    </div>
  </div>
</template>

<script lang="ts" setup>
import StoryWidget from "../components/main/story/StoryWidget.vue";
import PostWidget from "../components/main/post/PostWidget.vue";
import PageWidget from "../components/main/pages/PageWidget.vue";
import SiButton from "../components/shared/SiButton.vue";
</script>
