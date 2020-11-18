<template>
  <div class="container-fluid content-container album-page">
    <h2 class="album-title">
      {{ album.title }}
    </h2>
    <b-row>
      <b-col md="6"> hiiiiii </b-col>
    </b-row>
  </div>
</template>

<script>
import data from '~/data/albums.js'
const albums = data.albums

export default {
  asyncData({ params, payload }) {
    return {
      album: albums.filter(
        (album) => album.title.replace(/ /g, '').toLowerCase() === params.album
      )[0],
    }
  },
  data() {
    return {}
  },
}
</script>

<style></style>
