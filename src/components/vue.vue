<script setup>
import { getCollection } from 'astro:content';
const blogEntries = await getCollection('posts');
</script>

<template>
<ul>
    <li v-for="blog in blogEntries">
      <a :href="`/my-blog-url/${blog.slug}`">{{blog.data.title}}</a>
      <img :src="blog.data.image.src">
    </li>
</ul>
</template>