<template>
  <b-row>
    <b-col>
      <h4 v-if="!isLink">{{ post.date.slice(0, -8) }}</h4>
      <h5 v-if="title">{{ title }}</h5>
      <Regular v-if="isRegular" :post="post"></Regular>
      <Photo v-if="isPhoto" :post="post"></Photo>
      <Video v-if="isVideo" :post="post">video</Video>
      <hr />
    </b-col>
  </b-row>
</template>

<script>
import Regular from '~/components/Regular.vue'
import Photo from '~/components/Photo.vue'
import Video from '~/components/Video.vue'

export default {
  components: {
    Regular,
    Video,
    Photo,
  },
  props: {
    // eslint-disable-next-line vue/require-default-prop
    post: Object,
  },
  data() {
    return {
      isRegular: this.post.type === 'regular' || this.post.type === '',
      isVideo: this.post.type === 'video',
      isPhoto: this.post.type === 'photo',
      isLink: this.post.type === 'link',
      title: this.post['regular-title'],
    }
  },
}
</script>

<style></style>
