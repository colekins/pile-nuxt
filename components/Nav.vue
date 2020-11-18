<template>
  <b-navbar class="navbar" type="dark" sticky="true">
    <!-- Right aligned nav items -->
    <b-navbar-nav class="ml-auto">
      <b-nav-item>
        <NuxtLink class="nav-link" to="/">News</NuxtLink>
      </b-nav-item>
      <b-nav-item>
        <NuxtLink class="nav-link" to="/music">Music</NuxtLink>
      </b-nav-item>
      <b-nav-item>
        <NuxtLink class="nav-link" to="/videos">Videos</NuxtLink>
      </b-nav-item>
      <b-nav-item>
        <NuxtLink class="nav-link" to="/tour">Tour</NuxtLink>
      </b-nav-item>
      <b-nav-item>
        <NuxtLink class="nav-link" to="/new">Contact</NuxtLink>
      </b-nav-item>
    </b-navbar-nav>
  </b-navbar>
</template>

<style>
.band-name {
  padding: 0;
  height: 140px;
}

.navbar {
  width: 100%;
  padding: 0 8em;
  height: 2.92em;
  border: 0;
  border-top: 5.5px;
  border-radius: 1.5px;
  border-style: solid;
  border-color: #341a0b;
  background-color: #140e0e;
  align-items: center;
}

.nav-link a {
  color: #f36a52 !important;
  text-transform: uppercase;
  font-size: 1.1em;
}
</style>
