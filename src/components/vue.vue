<script setup>
const props = defineProps({
        entries: Object
    });
</script>

<template>
<ul>
    <li v-for="blog in entries">
      <a :href="`/my-blog-url/${blog.slug}`">{{blog.data.title}}</a>
      <img :src="blog.data.image.src">
    </li>
</ul>
</template>