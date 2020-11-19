<!-- eslint-disable -->
<template>
  <b-row>
    <b-col>
      <div class="video-container"><span v-html="video"> </span></div>
      <span v-if="caption" v-html="caption"></span>
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
      video: this.post['video-player-500'],
      caption: this.post['video-caption'],
    }
  },
}
</script>

<style></style>
