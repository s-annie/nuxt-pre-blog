<template>
    <div class="default-view">
      <img class="header-image" src='../assets/walle.png' width="160" />
      <p class="blog-title">The Robots of Dawn</p>

      <v-btn text class="navi-button" @click="goToHome()">Home</v-btn>
      <v-btn text class="navi-button" @click="goToTechArticles()">Technology</v-btn>
      <v-btn text class="navi-button">Life</v-btn>
      <v-btn text class="navi-button">Gallery</v-btn>
      <v-btn text class="navi-button">About</v-btn>
    </div>
</template>


<script>
export default {
  name: 'Header',
  methods: {
    goToHome() {
      this.$router.push('/')
    },
    goToTechArticles() {
      this.$router.push('/technology')
    },
  }
}
</script>

<style scoped>
.default-view{
    text-align: center;
    margin-top: 120px;
}
.header-image {
    margin-left: 41%;
    margin-bottom: 10px;
}
.blog-title{
    font-family: 'Raleway';
    font-size: 24px;
    margin-bottom: 10px;
}
</style>