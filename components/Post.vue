<template>
  <b-row>
    <b-col lg="10">
      <h4 v-if="!isLink" class="date">
        {{ post.date.slice(0, -8) }}
      </h4>
      <h5 class="post-title" v-if="title">{{ title }}</h5>
      <br />
      <div class="post-container">
        <Regular v-if="isRegular" :post="post"></Regular>
        <Photo v-if="isPhoto" :post="post"></Photo>
        <Video v-if="isVideo" :post="post">video</Video>
      </div>
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

<style>
.post-title {
  margin-top: 1em;
}

.post-container {
  margin-left: 1em;
}

@media only screen and (max-width: 992px) {
  .post-container {
    margin-left: 0.5em;
  }
}

@media only screen and (max-width: 430px) {
  .post-container {
    margin-left: 0;
  }
}
</style>
