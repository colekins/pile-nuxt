<template>
  <b-container class="container content-container tour">
    <div class="page-title">Tour</div>
    <br />
    <br />
    <b-row>
      <b-col lg="9">
        <iframe
          src="/shows.html"
          style="min-height: 50vh; width: 100%"
          frameBorder="0"
        ></iframe>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  head() {
    return {
      title: 'Pile - Tour',
    }
  },
}
</script>

<style></style>
