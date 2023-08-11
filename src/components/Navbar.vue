<template>
  <div class="container" >
    <div>
      <b-navbar toggleable="lg" type="light ">
        <b-navbar-brand href="#">Kulineran</b-navbar-brand>
        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
              <li class="nav-item">
                <router-link class="nav-link" to="/">Home</router-link>
              </li>
              <li class="nav-item">
                <router-link class="nav-link" to="/foods">Foods</router-link>
              </li>
              <li class="nav-item">
                <router-link class="nav-link" to="/drink">Drink</router-link>
              </li>
            </ul>
          </b-navbar-nav>
          <b-navbar-nav class="ms-auto">
            <li class="nav-item">
              <router-link class="nav-link" to="/keranjang">
                Keranjang
                <b-icon-bag></b-icon-bag>
                <span class="badge badge-success bg-success ms-2">0</span>
              </router-link>
            </li>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>
  </div>
</template>

<script>
export default {
  name: "NavbarItems",
};
</script>

<style>
</style>