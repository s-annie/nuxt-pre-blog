<template>
  <article>
    <h1>{{ posts.title }}</h1>
    <dl>
      <dt>date</dt>
      <dd>{{ posts.date }}</dd>
    </dl>
    <div><img :src="posts.image" /></div>
    <div v-for="tag in posts.tags" :key="tag">{{tag}}</div>
    
    <nuxt-content :document="posts" />
  </article>
</template>

<script lang="ts">
export default {
  async asyncData ({ $content, params }) {
    const posts = await $content('posts', params.slug || 'index').fetch()
    return { posts }
  }
}
</script>