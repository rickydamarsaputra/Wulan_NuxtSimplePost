<template>
  <div class="mt-10">
    <div class="text-left uppercase text-3xl leading-tight">{{post.title}}</div>
    <div class="capitalize text-gray-700 mt-4">{{post.body}}</div>
  </div>
</template>

<script>
import axios from 'axios';
export default {
  head() {
    return {
      title: "Nuxt Post Detail Page",
    }
  },
  data() {
    return {
      post: {},
    }
  },
  async mounted() {
    const response = await axios.get(`https://jsonplaceholder.typicode.com/posts/${this.$route.params.show}`);
    this.post = response.data;
  },
}
</script>
