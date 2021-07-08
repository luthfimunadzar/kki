<template>
  <v-app dark>
    <v-navigation-drawer v-model="drawer" left absolute temporary>
      <ul class="main-menu-sidebar">
        <li>
          <nuxt-link to="/">Home</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/programs">Programs & Services</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/portfolio">Portofolio</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/manifesto">Manifesto</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/profile">Proﬁle</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/contact">Contact Us</nuxt-link>
        </li>
      </ul>
    </v-navigation-drawer>
    <header>
      <a class="toggle" @click.stop="drawer = !drawer">
        <v-icon> mdi-menu </v-icon>
      </a>
      <nuxt-link to="/">
        <img src="/logo.png" alt="" class="d-block mx-auto logo" />
      </nuxt-link>
      <ul class="main-menu">
        <li>
          <nuxt-link to="/">Home</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/programs">Programs & Services</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/portfolio">Portofolio</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/manifesto">Manifesto</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/profile">Proﬁle</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/contact">Contact Us</nuxt-link>
        </li>
      </ul>
    </header>
    <v-main>
      <nuxt />
    </v-main>
    <v-footer app>
      <v-container>
        <v-row>
          <v-col md="10" offset-md="1" cols="12">
            <v-row>
              <v-col sm="6" cols="12">
                <h5>Sitemap</h5>
                <ul class="sitemap">
                  <li>
                    <nuxt-link to="/contact">Contact Us</nuxt-link>
                  </li>
                  <li>
                    <nuxt-link to="/">Home</nuxt-link>
                  </li>
                  <li>
                    <nuxt-link to="/portfolio">Portofolio</nuxt-link>
                  </li>
                  <li>
                    <nuxt-link to="/manifesto">Manifesto</nuxt-link>
                  </li>
                  <li>
                    <nuxt-link to="/profile">Proﬁle</nuxt-link>
                  </li>
                  <li>
                    <nuxt-link to="/programs">Programs & Services</nuxt-link>
                  </li>
                </ul>
              </v-col>
              <v-col sm="6" cols="12">
                <h5>Social Media</h5>
                <a href="" class="socmed">
                  <v-icon> fab fa-linkedin </v-icon>
                </a>
                <a href="" class="socmed">
                  <v-icon> fab fa-instagram </v-icon>
                </a>
                <a href="" class="socmed">
                  <v-icon> fab fa-twitter </v-icon>
                </a>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </v-footer>
    <Top />
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      group: null,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire',
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js',
    }
  },

  watch: {
    group() {
      this.drawer = false
    },
  },
}
</script>
