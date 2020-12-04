<!-- eslint-disable -->
<template>
  <b-row>
    <b-col>
      <img
        v-if="onePhoto"
        class="post-image"
        alt="blog-post-image"
        :src="image"
      />
      <span v-if="caption && onePhoto" v-html="caption"></span>
      <span v-if="!onePhoto">
        <span v-if="caption" v-html="caption"></span>
        ><img
          v-for="(photo, index) in photos"
          :key="index"
          class="post-image"
          alt="blog-post-image"
          :src="photo['photo-url-500']"
      /></span>
    </b-col>
  </b-row>
</template>

<script>
export default {
  props: {
    // eslint-disable-next-line vue/require-default-prop
    post: Object,
  },
  data() {
    return {
      onePhoto: this.post.photos.length === 0,
      image: this.post['photo-url-500'],
      photos: this.post.photos,
      caption: this.post['photo-caption'],
    }
  },
}
</script>

<style>
.post-image {
  margin: 1em 1em 1em 0;
  max-width: 100%;
}

@media only screen and (max-width: 992px) {
  .post-image {
    margin: 0.5em 0;
  }
}
</style>
