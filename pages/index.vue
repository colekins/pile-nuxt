<template>
  <div class="container">
    <div>
      <Post v-for="post in posts" :key="post.title" :post="post"></Post>
      <div class="links"></div>
    </div>
  </div>
</template>

<script>
import Post from '~/components/Post.vue'
const cors = 'https://cors-anywhere.herokuapp.com/'
const tumblr =
  'https://oldpilewebsite.tumblr.com/api/read/json?callback=?&num=10'

export default {
  components: {
    Post,
  },
  async fetch() {
    this.posts = await fetch(cors + tumblr)
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
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
