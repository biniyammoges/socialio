<template>
  <div class="flex flex-col">
    <ThePost
      v-for="post in posts"
      :key="post.id"
      :post="post"
      class="mb-4"
      @addPost="addPost"
    />
  </div>
</template>

<script lang="ts" setup>
import { ref } from "vue";
import { Post } from "./post-interfaces";
import ThePost from "./ThePost.vue";

const posts = ref<Post[]>([
  {
    id: "1",
    caption:
      "This was one of the most epic journeys, that I've got my self involved",
    date: "12 hrs ago",
    photo: "/story4.jpg",
    userName: "Laura Fisher",
    userPhoto: "/avatar6.jpg",
    likes: "Abdi Urgessa, Aysanew Yonas and 2.4k others",
    comments: "1.1k comments",
  },
  {
    id: "2",
    caption: "I had such a beautifull yestorday!",
    date: "1 min ago",
    photo: "/story2.jpg",
    userName: "Biniyam Moges",
    userPhoto: "/avatar5.jpg",
    likes: "Haile Melaku, Aysanew Yonas and 44k others",
    comments: "12k comments",
  },
  {
    id: "3",
    caption: "Life is not about finding ur self! it's about creating ur self",
    date: "1 day ago",
    photo: "/story3.jpg",
    userName: "Haile Melaku",
    userPhoto: "/avatar6.jpg",
    likes: "Biniyam Moges, Solomon and 44k others",
    comments: "45 comments",
  },
]);

const addPost = (post: Post) => {
  posts.value.push(post);
};
</script>
