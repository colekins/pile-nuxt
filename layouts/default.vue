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
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 15.75px;
  word-spacing: 1px;
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

.content-container {
  padding-top: 2em;
}

body a {
  color: #f76e56;
}

body * {
  color: white;
  font-family: Futura, 'Trebuchet MS', Arial, sans-serif;
}
</style>
