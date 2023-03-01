<template>
  <router-link
    to="/"
    class="flex items-center justify-between text-si-dark py-2 px-3 rounded-lg hover:bg-si-gray-light"
  >
    <div class="flex items-center">
      <div class="rounded-lg h-8 w-8 overflow-hidden object-cover mr-3">
        <img
          :src="friend.photo"
          alt="avatar"
          class="h-full w-full"
          style="object-fit: cover"
        />
      </div>

      <p>
        {{ friend.name }}
      </p>
    </div>

    <div
      v-if="friend.status === 'active'"
      class="bg-green rounded-lg p-1 text-white text-xs font-semibold"
    ></div>
  </router-link>
</template>

<script lang="ts" setup>
import { PropType, defineProps } from "vue";
import { Contact } from "./contact-interface";

const props = defineProps({
  friend: { type: Object as PropType<Contact>, required: true },
});
</script>
