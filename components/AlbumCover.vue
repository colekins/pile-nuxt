<template>
  <b-col
    :lg="onMusicPage ? 3 : 6"
    :md="onMusicPage ? 4 : 6"
    sm="6"
    class="album-cover"
  >
    <n-link :to="'/music/' + album.title.replace(/ /g, '').toLowerCase()">
      <img :src="album.images.small" width="100%" :alt="album.title" />
    </n-link>
    <div v-if="onMusicPage" class="item-title">
      <span class="album-title">{{ album.title }}</span
      ><br />
      <span class="album-title">{{ year }}</span>
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

.item-title {
  font-size: 16px;
  text-align: right;
  text-transform: capitalize;
}

.italic {
  font-style: italic;
}
</style>
