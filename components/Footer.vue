<template>
  <footer class="footer">
    <div class="container">
      <div v-if="show" class="sub-form">
        <form
          id="mc-embedded-subscribe-form"
          action="https://pilemusic.us7.list-manage.com/subscribe/post?u=aab58cace920f07848013de9d&amp;id=80ecb0b8c0"
          method="post"
          name="mc-embedded-subscribe-form"
          class="validate"
          target="_blank"
          novalidate
        >
          <div id="mc_embed_signup_scroll" class="d-flex email-form">
            <label for="mce-EMAIL"></label>
            <input
              id="mce-EMAIL"
              type="email"
              value=""
              name="EMAIL"
              class="email"
              placeholder="email address"
              required
            />
            <div style="position: absolute; left: -5000px" aria-hidden="true">
              <input
                id="email-text"
                type="text"
                name="b_aab58cace920f07848013de9d_80ecb0b8c0"
                tabindex="-1"
                value=""
              />
            </div>
            <div class="clear">
              <input
                id="mc-embedded-subscribe"
                type="submit"
                value="Subscribe"
                name="subscribe"
                class="button"
                @click="
                  preventDefault()
                  counter += 1
                "
              />
            </div>
          </div>
        </form>
      </div>
      <div v-if="!show" class="subscribe d-flex">
        <a @click="show = !show">Subscribe to our mailing list</a>
      </div>
      <div class="d-flex icons">
        <span>
          <a
            href="https://open.spotify.com/artist/44pUNjqg4mExLyFHnB3Bqf?si=uN19KRh5Sui6h7S10q7vJw"
            target="_blank"
            rel="noopener noreferrer"
          >
            <img
              src="https://i.imgur.com/09kaFGx.png"
              alt="Spotify"
              height="26"
              class="image-link"
          /></a>
          <a
            href="https://itunes.apple.com/us/artist/pile/1397539894"
            target="_blank"
            rel="noopener noreferrer"
          >
            <img
              src="https://i.imgur.com/6EjHQuq.png"
              alt="Apple"
              height="26"
              class="image-link"
          /></a>
          <a
            href="https://pile.bandcamp.com"
            target="_blank"
            rel="noopener noreferrer"
          >
            <img
              src="https://i.imgur.com/mRbxYxa.png"
              alt="bandcamp"
              height="26"
              class="image-link"
          /></a>
          <a
            href="https://www.facebook.com/pileof"
            target="_blank"
            rel="noopener noreferrer"
            ><img
              src="https://i.imgur.com/Wj5BGsH.png"
              alt="facebook"
              height="26"
              class="image-link"
          /></a>
          <a
            href="https://twitter.com/pilemusic"
            target="_blank"
            rel="noopener noreferrer"
            ><img
              src="https://i.imgur.com/XAq1BHO.png"
              alt="twitter"
              height="26"
              class="image-link"
          /></a>
          <a
            href="https://www.instagram.com/pilemusic/"
            target="_blank"
            rel="noopener noreferrer"
            ><img
              src="https://i.imgur.com/4k4qtaG.png"
              alt="instagram"
              height="26"
              class="image-link"
          /></a>
        </span>
      </div>
    </div>
    <Widget class="hide-widget" />
  </footer>
</template>

<script>
import Widget from '~/components/Widget'

export default {
  components: {
    Widget,
  },
  data() {
    return { show: false }
  },
}
</script>

<style>
.hidge-widget {
  display: none;
}
footer {
  position: fixed;
  height: 100px;
  bottom: -2.4em;
  right: 0;
  width: 100%;
  margin-bottom: 0.5em;
}
.icons,
.subscribe,
.email-form {
  justify-content: flex-end;
}

.subscribe {
  font-size: 0.92em;
  cursor: pointer;
  color: #f36a52;
}

.button {
  margin-left: 4px;
  background-color: #f36a52;
  border-radius: 4px;
  font-size: 1em;
  font-style: italic;
  color: white;
  transition: all 0.3s ease;
}

.subscribe a {
  padding: 0.3em 0.33em;
  border-radius: 3px;
  background: rgba(8, 8, 8, 0.84);
}

.image-link {
  margin: 0 2px;
}

.email-form {
  font-size: 0.78em;
  margin-bottom: 0.8em;
  padding: 0;
}
</style>
