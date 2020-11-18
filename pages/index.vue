<template>
  <b-container class="container-fluid">
    <div class="page-title">News</div>
    <br />
    <br />
    <Post v-for="post in posts" :key="post.title" :post="post"></Post>
  </b-container>
</template>

<script>
import Post from '~/components/Post.vue'
const cors = 'https://cors-anywhere.herokuapp.com/'
const api = 'https://oldpilewebsite.tumblr.com/api/read/json?callback=?&num=10'

export default {
  components: {
    Post,
  },
  async fetch() {
    this.posts = await fetch(cors + api)
      .then((res) => res.text())
      .then((data) => JSON.parse(data.slice(1, data.length - 2)))
      .then((data) => data.posts)
  },
  data() {
    return {
      posts: {},
    }
  },
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
}
</style>
