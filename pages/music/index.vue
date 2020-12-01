<template>
  <b-container class="container content-container discography">
    <div class="page-title">Music</div>
    <div class="subtitle">
      For all available physical goods, go
      <a href="https://pile.bandcamp.com/merch">here</a>.
    </div>
    <br />

    <b-row>
      <AlbumCover
        v-for="album in albums"
        :key="album.title"
        :album="album"
      ></AlbumCover>
    </b-row>
  </b-container>
</template>

<script>
import AlbumCover from '~/components/AlbumCover'
import data from '~/data/albums.js'

export default {
  components: {
    AlbumCover,
  },
  data() {
    return { albums: data.albums }
  },
  head() {
    return {
      title: 'Pile - Music',
    }
  },
}
</script>

<style>
.subtitle {
  display: block;
  margin-top: 1em;
}
@media only screen and (max-width: 992px) {
  .subtitle {
    display: block;
    text-align: center;
  }
}
</style>
