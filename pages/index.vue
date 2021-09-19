<template>
  <div>
    <div v-for="p in posts" :key="p.slug" >
      <v-row>
        <p class="post-date">category: {{ p.category }}</p>
      </v-row>
      <v-row>
        <div v-for="tag in p.tags" :key="tag" class="post-date">
          <v-card>{{tag}}</v-card>  
        </div>
      </v-row>
      <v-row>
        <div class="post-title">
          <nuxt-link :to="p.slug">{{p.title}}</nuxt-link>
        </div>
      </v-row>
      <v-row>
        <p class="post-date">{{ p.date }}</p>
      </v-row>
      <v-row>
        <v-divider></v-divider>
      </v-row>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData ({ $content, params }) {
    const query = await $content('posts' || 'index').limit(15)
    const posts = await query.fetch()
    return { posts }
  }
}
</script>

<style>
.post-title {
  font-family: 'Noto Sans SC', sans-serif;
  font-size: 24px;
}
.post-date{
  font-family: RaleWay;
  font-size: 15px;
}
</style>