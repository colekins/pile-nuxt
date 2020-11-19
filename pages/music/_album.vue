<template>
  <b-container class="container-fluid content-container album-page">
    <div class="page-title">
      {{ album.title }}
    </div>
    <br />
    <br />
    <b-row>
      <b-col md="6">
        <a
          :href="album.links.bandcamp"
          rel="noopener noreferrer"
          target="_blank"
        >
          <img
            class="album-page-cover"
            :src="album.images.cover"
            width="100%"
            :alt="album.title"
          />
        </a>
      </b-col>
      <b-col md="6">
        <span class="embed" v-html="album.embed"></span>
        <div class="release-date">Released {{ album.releaseDate }}.</div>
      </b-col>
    </b-row>
    <b-row>
      <b-col>
        <div class="credits">
          {{ album.credits }}
        </div>
      </b-col>
    </b-row>
    <b-row>
      <b-col>
        <div class="lyrics">
          <div
            class="song-lyrics"
            v-for="(song, index) in album.songs"
            :key="song.title"
            :song="song"
          >
            <span v-if="song.lyrics">
              <b>{{ index + 1 }}. {{ song.title }}</b
              ><br />
              <span> {{ song.lyrics }}</span>
            </span>
          </div>
        </div>
      </b-col>
    </b-row>
  </b-container>
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

<style>
.credits,
.lyrics {
  margin: 1.2em 0;
  padding: 0.5em;
  border-style: dotted;
  border-width: 2px;
  border-color: #eb9485;
  line-height: 1.8em;
}

.lyrics {
  border: none;
}

.song-lyrics {
  margin-bottom: 1em;
}
</style>
