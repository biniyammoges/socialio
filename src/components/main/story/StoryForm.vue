<template>
  <div
    :style="{
      backgroundImage: `url('/avatar5.jpg'), linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.2), rgba(0, 0, 0, 0.3), rgba(0, 0, 0, 0.4))`,
      backgroundPosition: 'center',
      backgroundSize: 'cover',
    }"
    class="story rounded-lg flex flex-col justify-end py-2 bg-center bg-cover cursor-pointer"
  >
    <div class="text-center font-semibold text-white">CreateStory</div>
  </div>
</template>

<style scoped>
.story {
  height: 190px;
  width: 110px;
}
</style>
