<template>
  <div>
    <v-container>
      <v-row>
        <v-col ><Header /></v-col>
        <v-col ><Post /></v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import Header from "../components/header.vue"
import Post from "../components/post.vue"

export default {
    components: {
        Header,
        Post,
    }
};
</script>
