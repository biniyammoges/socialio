<template>
  <div
    :style="{
      backgroundImage: `url(${props.story.photo}), linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.2), rgba(0, 0, 0, 0.3), rgba(0, 0, 0, 0.4))`,
      backgroundPosition: 'center',
      backgroundSize: 'cover',
    }"
    class="story rounded-lg flex flex-col justify-between py-2 bg-center bg-cover cursor-pointer"
  >
    <div
      style="height: 40px; width: 40px"
      class="rounded-lg p-1 overflow-hidden border-2 border-white ml-3"
    >
      <img
        :src="props.story.userPhoto"
        :alt="props.story.userName"
        class="w-full h-full rounded-lg"
        style="object-fit: cover"
      />
    </div>
    <div class="text-center font-semibold text-white">
      {{ props.story.userName }}
    </div>
  </div>
</template>

<script lang="ts" setup>
import { PropType, defineProps } from "vue";
import { Story } from "./story-interfaces";

const props = defineProps({
  story: { type: Object as PropType<Story>, required: true },
  new: { type: Boolean },
});
</script>

<style scoped>
.story {
  height: 190px;
  width: 110px;
}
</style>
