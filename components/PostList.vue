<script setup lang="ts">
const props = defineProps<{
  postList: any;
}>();
</script>

<template>
  <ul class="post-list">
    <li v-for="post in postList">
      <NuxtLink :to="post._path"
        ><h2>{{ post.title }}</h2>
      </NuxtLink>
      <time :datetime="post.publishDate">{{
        getFormattedDate(post.publishDate)
      }}</time>
      <ul class="tag-list">
        <li v-for="tag in post.tags">
          <NuxtLink class="tag" :to="'/tags/' + tag">{{ tag }}</NuxtLink>
        </li>
      </ul>
    </li>
  </ul>
</template>
