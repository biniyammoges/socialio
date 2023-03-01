<template>
  <div class="bg-white w-full p-4 rounded-lg">
    <div class="flex justify-between items-start">
      <div class="flex">
        <button class="rounded-lg h-10 w-10 overflow-hidden object-cover mr-2">
          <img
            :src="props.post.userPhoto"
            :alt="props.post.userName"
            class="h-full w-full"
            style="object-fit: cover"
          />
        </button>
        <div class="flex flex-col">
          <p class="mb-1">{{ props.post.userName }}</p>
          <p class="text-grey text-sm">{{ props.post.date }}</p>
        </div>
      </div>
      <button class="button py-3 px-3 border border-si-black rounded-lg">
        <img src="/three-dot.svg" alt="menu" class="" />
      </button>
    </div>

    <!-- caption -->
    <div class="mt-4" v-if="props.post?.caption">
      <p class="text-si-gray-dark">{{ props.post?.caption }}</p>
    </div>

    <!-- Image -->
    <div
      class="rounded-lg overflow-hidden mt-4 cursor-pointer"
      style="max-height: 600px"
      v-if="props.post.photo"
    >
      <img
        :src="props.post.photo"
        alt="post"
        class="w-full h-full"
        style="object-fit: cover"
      />
    </div>

    <!-- Likes -->
    <div class="mt-4">
      <div class="flex justify-between items-center">
        <div class="flex items-center">
          <img
            src="/like-button.svg"
            alt=""
            class="mr-2"
            style="height: 20px; width: 20px"
          />
          <router-link
            to="/"
            class="text-sm text-si-gray-dark hover:underline"
            >{{ props.post.likes }}</router-link
          >
        </div>
        <router-link to="/" class="text-sm text-si-gray-dark hover:underline">{{
          props.post.comments
        }}</router-link>
      </div>

      <!-- Post actions -->
      <div
        class="flex items-center justify-between mt-4 border-t border-b border-si-border py-1"
      >
        <button
          class="flex-1 justify-center py-2 text-si-gray-dark flex items-center hover:bg-si-gray-light rounded-lg"
        >
          <img
            src="/like-icon.svg"
            alt="icon"
            style="height: 20px; width: 20px"
            class="mr-2"
          />
          <p>Like</p>
        </button>
        <button
          class="flex-1 justify-center py-2 text-si-gray-dark flex items-center hover:bg-si-gray-light rounded-lg"
        >
          <img
            src="/message-icon.svg"
            alt="icon"
            style="height: 20px; width: 20px"
            class="mr-2"
          />
          <p>Comment</p>
        </button>
        <button
          class="flex-1 justify-center py-2 text-si-gray-dark flex items-center hover:bg-si-gray-light rounded-lg"
        >
          <img
            src="/share-icon.svg"
            alt="icon"
            style="height: 20px; width: 20px"
            class="mr-2"
          />
          <p>Share</p>
        </button>
      </div>

      <!-- Comment -->
      <div
        class="bg-white flex items-center justify-between rounded-lg py-1 px-2 mt-4 shadow-sm"
      >
        <button class="rounded-lg h-10 w-10 overflow-hidden object-cover mr-2">
          <img
            :src="props.post.userPhoto"
            alt="avatar"
            class="h-full w-full"
            style="object-fit: cover"
          />
        </button>
        <input
          type="text"
          placeholder="write a comment.."
          style="height: 100%"
          class="focus:outline-none flex-1 px-3 py-3 bg-si-gray-light rounded-lg"
        />
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { PropType, defineProps, defineEmits, ref } from "vue";
import { Post } from "./post-interfaces";

const props = defineProps({
  post: { type: Object as PropType<Post>, required: true },
});
const emits = defineEmits(["addPost"]);

const name = ref("");
</script>
