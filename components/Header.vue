<template>
  <header>
    <div class="w-4/5 mx-auto flex justify-between items-center mt-10">
      <div class="text-2xl uppercase">nuxt app</div>
      <div class="flex flex-row space-x-5">
        <nuxt-link :to="{ name: 'index' }" class="text-sm uppercase font-medium" exact>home</nuxt-link>
        <nuxt-link :to="{ name: 'about' }" class="text-sm uppercase font-medium">about</nuxt-link>
        <nuxt-link :to="{ name: 'posts' }" class="text-sm uppercase font-medium">posts</nuxt-link>
      </div>
    </div>
  </header>
</template>

<script>
export default {}
</script>
