<template>
  <div>
    <b-row class="header">
      <!-- <b-col > -->
      <NuxtLink to="/">
        <img
          class="band-name"
          alt="Pile"
          src="https://i.imgur.com/448IIH6.png"
        />
      </NuxtLink>
      <!-- </b-col> -->
    </b-row>
  </div>
</template>

<style>
.band-name {
  padding: 0;
  height: 140px;
}

.header {
  background-image: url(https://i.imgur.com/Tdlr3Fq.png);
  background-size: cover;
  background-position: bottom;
  padding: 0.7em 8em;
  display: flex;
  justify-content: flex-end;
  min-width: 100%;
  margin: 0 !important;
}

@media only screen and (max-width: 1440px) {
  .header {
    padding: 0.7em 6em;
  }
}

@media only screen and (max-width: 992px) {
  .header {
    justify-content: space-around;
  }
}

@media only screen and (max-width: 430px) {
  .band-name {
    height: 100px;
  }

  .header {
    background-position: unset;
  }
}

@media only screen and (min-width: 1550px) {
  .header {
    padding: 0.7em 12em;
  }
}
</style>
