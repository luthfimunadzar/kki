<template>
  <v-app dark>
    <v-navigation-drawer v-model="drawer" left absolute temporary>
      <v-list nav dense>
        <v-list-item-group
          v-model="group"
          active-class="red--text text--darken-4"
        >
          <v-list-item>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-title>Programs & Services</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-title>Portofolio</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-title>Manifesto</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-title>Proﬁle</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-title>Contact Us</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
    <header>
      <a class="toggle" @click.stop="drawer = !drawer">
        <v-icon> mdi-menu </v-icon>
      </a>
      <img src="/logo.png" alt="" class="d-block mx-auto logo" />
      <ul class="main-menu">
        <li>
          <a href="#">Home</a>
        </li>
        <li>
          <a href="#">Programs & Services</a>
        </li>
        <li>
          <a href="#">Portofolio</a>
        </li>
        <li>
          <a href="#">Manifesto</a>
        </li>
        <li>
          <a href="#">Proﬁle</a>
        </li>
        <li>
          <a href="#">Contact Us</a>
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
                    <a href="">Contact Us</a>
                  </li>
                  <li>
                    <a href="">Home</a>
                  </li>
                  <li>
                    <a href="">Portofolio</a>
                  </li>
                  <li>
                    <a href="">Manifesto</a>
                  </li>
                  <li>
                    <a href="">Proﬁle</a>
                  </li>
                  <li>
                    <a href="">Programs & Services</a>
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
