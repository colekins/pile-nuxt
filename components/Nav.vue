<template>
  <b-navbar class="navbar" type="dark" sticky="true">
    <!-- Right aligned nav items -->
    <b-navbar-nav>
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
        <NuxtLink class="nav-link" to="/contact">Contact</NuxtLink>
      </b-nav-item>
    </b-navbar-nav>
  </b-navbar>
</template>

<style>
.navbar {
  min-width: 100%;
  padding: 0 8em;
  height: 3.2em;
  border: 0;
  border-top: 5.5px;
  border-radius: 1.5px;
  border-style: solid;
  border-color: #341a0b;
  background-color: #140e0e;
  align-items: center;
  justify-content: flex-end;
}

.navbar-expand .navbar-nav .nav-link {
  padding-right: 0;
  padding-left: 0.6em;
}

.nav-link a {
  color: #f76e56 !important;
  text-transform: uppercase;
  font-size: 1.14em;
}

.nav-link a:hover {
  color: #ffb9ad !important;
  text-decoration: underline;
}

@media only screen and (max-width: 992px) {
  .navbar {
    justify-content: space-around;
    text-align: center;
    padding: 0;
  }

  .navbar-expand .navbar-nav .nav-link {
    padding: 0 0.5em;
  }
}

@media only screen and (max-width: 430px) {
  .nav-link a:hover {
    color: #f76e56 !important;
    text-decoration: none;
  }
  .navbar {
    height: 2.9em;
  }
  .nav-link a {
    font-size: 1em;
  }
  .navbar-expand .navbar-nav .nav-link {
    padding-right: 0;
    padding-left: 0;
    padding: 0 0.3em;
  }
}

@media only screen and (max-width: 1440px) {
  .navbar {
    padding: 0 6em;
  }
}

@media only screen and (max-width: 370px) {
  .nav-link a {
    font-size: 0.9em;
  }
  .navbar-expand .navbar-nav .nav-link {
    padding: 0 0.2em;
  }
}

@media only screen and (min-width: 1550px) {
  .navbar {
    padding: 0 12em;
  }
}

@media only screen and (min-width: 1680px) {
  .navbar {
    padding: 0 14em;
  }
}
</style>
