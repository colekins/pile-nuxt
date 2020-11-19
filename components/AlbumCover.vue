<template>
  <b-col
    :lg="onMusicPage ? 4 : 6"
    :md="onMusicPage ? 4 : 6"
    sm="6"
    class="album-cover"
  >
    <NuxtLink :to="'/music/' + album.title.replace(/\W/g, '').toLowerCase()">
      <img :src="album.images.cover" width="100%" :alt="album.title" />
    </NuxtLink>
    <div v-if="onMusicPage" class="item-title">
      <span class="album-title">{{ album.title }}</span
      ><br />
      <span class="album-year">({{ year }})</span>
    </div>
  </b-col>
</template>

<script>
export default {
  components: {},
  props: {
    // eslint-disable-next-line vue/require-default-prop
    album: Object,
  },
  data() {
    return {
      onMusicPage: this.$route.name === 'music',
      year: this.album.releaseDate.substring(this.album.releaseDate.length - 4),
    }
  },
}
</script>

<style>
.album-cover {
  margin-bottom: 2.1em;
  transition: transform 0.3s ease;
}

.album-year {
  font-size: 0.9em;
}

.item-title {
  margin-top: 0.5em;
  font-size: 16px;
  text-align: right;
  text-transform: capitalize;
}

.album-title {
  font-weight: bold;
}

.italic {
  font-style: italic;
}
</style>
