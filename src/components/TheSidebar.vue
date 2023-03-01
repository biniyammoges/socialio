<template>
  <div
    class="bg-white rounded-lg mr-4 py-2 px-2 shadow-xl"
    style="width: 250px"
  >
    <router-link
      :class="{
        ...(link.id === '1'
          ? { 'bg-si-gray': true, 'text-si-primary': true }
          : { 'text-si-dark': true }),
      }"
      class="py-3 px-4 block rounded font-semibold hover:bg-si-gray flex items-center"
      v-for="link in links"
      :to="link.to"
      :key="link.id"
    >
      <img
        v-if="link.icon"
        :src="link.icon"
        alt="avatar"
        class="h-full w-full mr-2"
        style="object-fit: cover; height: 20px; width: 20px"
      />
      <p>{{ link.title }}</p></router-link
    >
  </div>
</template>

<script lang="ts" setup>
interface Link {
  id?: string;
  to: string;
  title: string;
  icon?: string;
}

const links: Link[] = [
  { to: "/", title: "Home", id: "1", icon: "/Home_fill.svg" },
  { to: "/", title: "Photos", id: "2", icon: "/Img_box.svg" },
  { to: "/", title: "Profile", id: "3", icon: "/User.svg" },
  { to: "/", title: "Freinds", id: "5", icon: "/User_add_alt.svg" },
  { to: "/", title: "Logout", id: "6", icon: "/Sign_in_squre.svg" },
];
</script>
