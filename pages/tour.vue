<template>
  <b-container class="container content-container tour">
    <div class="page-title">Tour</div>
    <br />
    <br />
    <b-row>
      <b-col lg="9">
        <a
          class="bit-widget-initializer"
          data-artist-name="pile"
          data-display-local-dates="false"
          data-display-past-dates="false"
          data-auto-style="true"
          data-text-color="#FFFFFF"
          data-link-color="#f36a52"
          data-background-color="rgba(0,0,0,0)"
          data-display-limit="20"
          data-widget-width="100%"
          data-display-logo="false"
          data-display-lineup="false"
          data-separator-color="rgba(255, 255, 255, 0.5)"
        >
        </a>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  data() {
    return {
      scriptLoaded: false,
    }
  },
  head() {
    return {
      script: [
        {
          src: 'https://widget.bandsintown.com/main.min.js',
          body: true,
        },
      ],
    }
  },
}
</script>
