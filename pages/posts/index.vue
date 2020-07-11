<template>
  <div class="mt-10">
    <div class="text-center uppercase text-3xl">posts page</div>
    <div class="grid grid-cols-3 gap-5">
      <div v-for="post in posts" :key="post.id" class="bg-white shadow-md rounded-md p-5">
        <nuxt-link :to="{name: 'posts-show', params: {show: post.id}}" class="text-sm font-medium text-gray-700 hover:text-gray-800">{{post.title}}</nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios';
export default {
  head() {
    return {
      title: "Nuxt Posts Page",
    }
  },
  data() {
    return {
      posts: [],
    }
  },
  async mounted() {
    const response = await axios.get('https://jsonplaceholder.typicode.com/posts');
    this.posts = response.data;
  },
}
</script>
