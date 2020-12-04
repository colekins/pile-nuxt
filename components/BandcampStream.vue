<template>
  <div class="floater">
    <iframe
      style="border: 0; width: 100%; height: 42px"
      src="https://bandcamp.com/EmbeddedPlayer/album=2694995507/size=small/bgcol=141414/linkcol=f36a52/artwork=false/transparent=true/"
      seamless
      ><a href="http://pile.bandcamp.com/album/green-and-gray"
        >Green and Gray by Pile</a
      ></iframe
    >
  </div>
</template>

<style>
.floater {
  position: absolute;
  top: 15em;
  right: 8em;
  width: 24em;
  z-index: 12;
  opacity: 0.9;
}

@media only screen and (max-width: 1440px) {
  .floater {
    right: 6em;
  }
}

@media only screen and (min-width: 1550px) {
  .floater {
    right: 12em;
  }
}

@media only screen and (min-width: 1680px) {
  .floater {
    right: 14em;
  }
}
</style>
