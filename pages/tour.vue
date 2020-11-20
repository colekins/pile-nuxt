<template>
  <b-container class="container content-container tour">
    <div class="page-title">Tour</div>
    <br />
    <br />
    <b-row>
      <b-col lg="9">
        <!-- <Widget /> -->
        <iframe
          src="/shows.html"
          style="height: 100vh; width: 100%"
          frameBorder="0"
        ></iframe>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
// import Widget from '~/components/Widget.vue'

export default {
  components: {
    // Widget,
  },
  data() {
    return {
      // scriptLoaded: false,
    }
  },
  // head() {
  //   return {
  //     script: [
  //       {
  //         src: 'https://widget.bandsintown.com/main.min.js',
  //         body: true,
  //         async: true,
  //         callback: () => (this.scriptLoaded = true),
  //       },
  //     ],
  //   }
  // },
}
</script>

<style></style>
