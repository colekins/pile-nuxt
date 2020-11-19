<template>
  <b-container class="container content-container news">
    <div class="page-title">News</div>
    <br />
    <br />
    <span v-if="posts">
      <Post v-for="post in posts" :key="post.title" :post="post"></Post>
    </span>
  </b-container>
</template>

<script>
import Post from '~/components/Post.vue'
const cors = 'https://pile-cors-anywhere.herokuapp.com/'
// const cors = 'http://0.0.0.0:8080/'
const api = 'https://oldpilewebsite.tumblr.com/api/read/json?callback=?&num=10'
const endpoint = cors + api

export default {
  components: {
    Post,
  },
  async fetch() {
    this.posts = await fetch(endpoint)
      .then((res) => res.text())
      .then((data) => JSON.parse(data.slice(1, data.length - 2)))
      .then((data) => data.posts)
  },
  fetchOnServer: false,
  data() {
    return {
      posts: null,
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
