<template>
  <div class="container">
    <nav class="navbar" role="navigation" aria-label="main navigation">
      <div class="navbar-brand">
        <a class="navbar-item" href="/">Portfolio</a>
        <button 
          class="button navbar-burger" 
          v-bind:class="{ 'is-active': showMobileMenu }"
          v-on:click="showMobileMenu = !showMobileMenu"
        >
          <span></span>
          <span></span>
          <span></span>
        </button>
      </div>
      <div 
        class="navbar-menu"
        v-bind:class="{ 'is-active': showMobileMenu }"
      >
        <div class="navbar-end">
          <nuxt-link 
            class="navbar-item" 
            to="/"
            v-on:click.native="showMobileMenu = !showMobileMenu"
          >
            Home
          </nuxt-link>
          <nuxt-link 
            class="navbar-item" 
            to="/about"
            v-on:click.native="showMobileMenu = !showMobileMenu"
          >
            About
          </nuxt-link>
          <nuxt-link 
            class="navbar-item" 
            to="/projects"
            v-on:click.native="showMobileMenu = !showMobileMenu"
          >
            Projects
          </nuxt-link>
          <nuxt-link 
            class="navbar-item" 
            to="/contact"
            v-on:click.native="showMobileMenu = !showMobileMenu"
          >
            Contact
          </nuxt-link>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
module.exports = {
  data: function () {
    return {
      showMobileMenu: false
    }
  }
}
</script>
