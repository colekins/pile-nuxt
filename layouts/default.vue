<template>
  <div>
    <Header />
    <Nav />
    <transition name="fade">
      <Nuxt />
    </transition>
    <Footer />
  </div>
</template>

<script>
import Nav from '~/components/Nav.vue'
import Header from '~/components/Header.vue'
import Footer from '~/components/Footer'

export default {
  components: {
    Nav,
    Header,
    Footer,
  },
}
</script>

<style>
html {
  font-family: Futura, 'Trebuchet MS', Arial, sans-serif;
  font-size: 15.75px;
  /* word-spacing: 1px; */
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

.page-title {
  font-size: 2em;
  display: inline;
  text-decoration: overline;
  text-decoration-color: #eb9485;
  text-decoration-style: dotted;
}

.fade-enter-active,
.fade-leave-active {
  transition-duration: 0.3s;
  transition-property: opacity;
  transition-timing-function: ease;
}

.fade-enter,
.fade-leave-active {
  opacity: 0;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

body {
  background-color: rgb(8, 8, 8);
}

h2 {
  font-size: 1.48em;
}

.content-container {
  padding-top: 2em;
  padding-bottom: 5em;
}

body a {
  color: #f76e56;
  word-wrap: break-word;
}

body a:hover {
  color: #ffb9ad;
}

body * {
  color: white;
  font-family: Futura, 'Trebuchet MS', Arial, sans-serif;
}

@media only screen and (max-width: 992px) {
  .content-container {
    padding-bottom: 2.5em;
  }

  .page-title {
    display: block;
    text-align: center;
  }
}
</style>
