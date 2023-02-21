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
          <nuxt-link to="/telepath">Telepath</nuxt-link>
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
    <div class="header-new">
      <nuxt-link to="/new">
        <img src="/logo.png" alt="" class="logo" />
      </nuxt-link>
      <ul class="main-menu">
        <li>
          <nuxt-link to="/new">Home</nuxt-link>
        </li>
        <li>
          <v-menu offset-y content-class="dropdown-menu-new">
            <!-- eslint-disable-next-line vue/v-slot-style -->
            <template v-slot:activator="{ on, attrs }">
              <a href="javascript:void(0);" v-bind="attrs" v-on="on"
                >Builder <span class="caret"></span>
              </a>
            </template>
            <v-container>
              <v-row>
                <v-col cols="12">
                  <v-list>
                    <v-list-item link to=""> Programs & Services </v-list-item>
                    <v-list-item link to=""> Telepath </v-list-item>
                  </v-list>
                </v-col>
              </v-row>
            </v-container>
          </v-menu>
        </li>
        <li>
          <v-menu offset-y content-class="dropdown-menu-new">
            <!-- eslint-disable-next-line vue/v-slot-style -->
            <template v-slot:activator="{ on, attrs }">
              <a href="javascript:void(0);" v-bind="attrs" v-on="on"
                >Venture Services <span class="caret"></span>
              </a>
            </template>
            <v-container>
              <v-row>
                <v-col cols="12">
                  <v-list>
                    <v-list-item link to=""> Finance </v-list-item>
                    <v-list-item link to=""> Marketing </v-list-item>
                    <v-list-item link to=""> Human Resource </v-list-item>
                    <v-list-item link to=""> Fundraising </v-list-item>
                    <v-list-item link to=""> Legal </v-list-item>
                    <v-list-item link to=""> Impact Management </v-list-item>
                    <v-list-item link to=""> Community </v-list-item>
                  </v-list></v-col
                >
              </v-row>
            </v-container>
          </v-menu>
        </li>
        <li>
          <nuxt-link to="">About Us</nuxt-link>
        </li>
        <li>
          <nuxt-link to="">Contact Us</nuxt-link>
        </li>
      </ul>
      <a class="toggle" @click.stop="drawer = !drawer">
        <v-icon> mdi-menu </v-icon>
      </a>
    </div>
    <v-main>
      <nuxt />
    </v-main>
    <div class="footer-new">
      <v-container>
        <v-row>
          <v-col md="10" offset-md="1" cols="12" class="pb-0">
            <v-row>
              <v-col cols="12" md="6">
                <h5>Sitemap</h5>
                <nuxt-link to="" class="sitemap">Home</nuxt-link>
                <nuxt-link to="" class="sitemap">Builder</nuxt-link>
                <nuxt-link to="" class="sitemap">Venture Services</nuxt-link>
                <nuxt-link to="" class="sitemap">About Us</nuxt-link>
              </v-col>
              <v-col cols="12" md="6">
                <h5>Social Media</h5>
                <a href="" class="socmed mr-2">
                  <v-icon> fab fa-linkedin </v-icon>
                </a>
                <a href="" class="socmed mr-2">
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
    </div>
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
      form: {
        name: null,
        email: null,
        message: null,
      },
    }
  },

  watch: {
    group() {
      this.drawer = false
    },
  },

  methods: {
    submit() {
      const scriptURL =
        'https://script.google.com/macros/s/AKfycbyCXTRmP2pouGHRnULKJteXrHv7gHNqz0-aPj8sS4C_cBLOxSarSs__8fm5UWPMaIA53g/exec'
      const sendingData = new FormData()
      sendingData.append('name', this.form.name)
      sendingData.append('email', this.form.email)
      sendingData.append('message', this.form.message)

      fetch(scriptURL, { method: 'POST', body: sendingData })
        .then(
          () =>
            this.$swal.fire({
              type: 'success',
              title: 'Message Sent!',
              text: 'Thank you for contacting kolaborasi, we will contact you very soon.',
            }),
          this.reset()
        )
        .catch(() =>
          this.$swal.fire({
            type: 'error',
            title: 'Oops',
            text: 'Theres something error please try again later, or contacting us via social media.',
          })
        )
    },
    reset() {
      this.form.name = null
      this.form.email = null
      this.form.message = null
      this.$refs.observer.reset()
    },
  },
}
</script>
