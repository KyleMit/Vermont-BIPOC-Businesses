<template>
  <v-app dark>
    <v-app-bar fixed app>
      <nuxt-link class="unstyled-link" to="/">
        <v-toolbar-title v-text="title" />
      </nuxt-link>
      <v-spacer></v-spacer>
      <v-btn class="white mr-5">
        <nuxt-link class="unstyled-link" to="/">Home</nuxt-link>
      </v-btn>
      <v-btn class="white">
        <nuxt-link class="unstyled-link" to="/FAQ">FAQ</nuxt-link>
      </v-btn>
    </v-app-bar>

    <!-- catch injected content -->
    <v-content>
      <v-container class="col-lg-8">
        <nuxt />
      </v-container>
    </v-content>

    <!-- footer here -->
    <v-footer app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  head: {
    title: 'Vermont BIPOC Businesses',
    script: [
      { src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }
    ]
  },

  data() {
    return {
      title: 'VT BIPOC Owned'
    }
  }
}
</script>

<style>
.unstyled-link {
  text-decoration: none;
}

.page-enter-active,
.page-leave-active {
  transition: all 0.2s ease;
}
.page-enter,
.page-leave-to {
  opacity: 0;
  transform: translateX(100vw);
}
</style>
