<script setup lang="ts">
const postList = await getPosts(undefined, 5);
</script>

<template>
  <h1>Frontend Walrus</h1>
  <article>
    <PostList :postList="postList" />
  </article>
  <NuxtLink to="/posts" class="link-forward">Todos os posts</NuxtLink>
</template>
