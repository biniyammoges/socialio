<template>
  <button
    class="rounded-lg py-2 px-3 font-bold h-10"
    :class="{
      ...(props.variant === 'default' && {
        'bg-si-primary': true,
        'text-white': true,
      }),
    }"
  >
    <slot></slot>
  </button>
</template>

<script lang="ts" setup>
import { PropType, defineProps } from "vue";

type Variant = "default" | "outlined";

const props = defineProps({
  variant: { type: String as PropType<Variant>, default: "default" },
});
</script>
