<template>
  <router-link
    to="/"
    class="flex items-center justify-between text-si-dark py-2 px-3 rounded-lg hover:bg-si-gray-light"
  >
    <div class="flex items-center">
      <div class="rounded-lg h-8 w-8 overflow-hidden object-cover mr-3">
        <img
          :src="props.page.photo"
          alt="avatar"
          class="h-full w-full"
          style="object-fit: cover"
        />
      </div>

      <p>
        {{ props.page.name }}
      </p>
    </div>

    <div
      v-if="page.unreadCount"
      class="bg-si-primary rounded-lg p-1 text-white text-xs font-semibold"
    >
      {{ page.unreadCount }}+
    </div>
  </router-link>
</template>

<script lang="ts" setup>
import { PropType, defineProps } from "vue";
import { Page } from "./page-interface";

const props = defineProps({
  page: { type: Object as PropType<Page>, required: true },
});
</script>
