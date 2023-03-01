<template>
  <div class="flex">
    <story-form class="mr-3"></story-form>
    <the-story
      class="mr-3"
      v-for="story in stories"
      :key="story.id"
      :story="story"
    ></the-story>
  </div>
</template>

<script lang="ts" setup>
import { Story } from "./story-interfaces";
import TheStory from "./TheStory.vue";
import StoryForm from "./StoryForm.vue";

const stories: Story[] = [
  {
    id: "1",
    photo: "/story1.jpg",
    userName: "Biniyam",
    userPhoto: "/avatar5.jpg",
  },
  {
    id: "2",
    photo: "/story2.jpg",
    userName: "Haile",
    userPhoto: "/avatar5.jpg",
  },
  {
    id: "3",
    photo: "/story3.jpg",
    userName: "Abdi",
    userPhoto: "/avatar5.jpg",
  },
  {
    id: "4",
    photo: "/story4.jpg",
    userName: "Samuel",
    userPhoto: "/avatar5.jpg",
  },
];
</script>
