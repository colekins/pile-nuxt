<template>
  <b-container class="container content-container tour">
    <div class="page-title">Tour</div>
    <br />
    <br />
    <b-row>
      <b-col lg="9">
        <Widget />
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import Widget from '~/components/Widget.vue'

export default {
  components: {
    Widget,
  },
  data() {
    return {
      scriptLoaded: false,
    }
  },
}
</script>

<style></style>
