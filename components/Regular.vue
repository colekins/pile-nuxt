/* eslint-disable vue/no-v-html */

<template>
  <b-row>
    <b-col>
      <span v-html="post['regular-body']"></span>
      <img v-if="photo" class="post-image" alt="blog-post-image" :src="photo" />
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
      photo: this.post['photo-url-500'],
    }
  },
}
</script>

<style></style>
