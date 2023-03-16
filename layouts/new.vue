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
      <nuxt-link to="/">
        <img src="/logo.png" alt="" class="logo" />
      </nuxt-link>
      <ul class="main-menu">
        <li>
          <nuxt-link to="/">Home</nuxt-link>
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
                  <v-list dark>
                    <v-list-item link to="/venture-builder">
                      Venture Builder
                    </v-list-item>
                    <v-list-item link to="/portfolio"> Portofolio </v-list-item>
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
                  <v-list dark>
                    <v-list-item link to="/service/finance">
                      Financial & Tax
                    </v-list-item>
                    <v-list-item link to="/service/content-design">
                      Content & Design
                    </v-list-item>
                    <v-list-item link to="/service/human-resources">
                      Human Resources
                    </v-list-item>
                    <v-list-item link to="/service/impact-management">
                      Impact Management
                    </v-list-item>
                    <v-list-item link to="/service/fundraising-preparation">
                      Fundraising Preparation
                    </v-list-item>
                  </v-list></v-col
                >
              </v-row>
            </v-container>
          </v-menu>
        </li>
        <li>
          <v-menu offset-y content-class="dropdown-menu-new">
            <!-- eslint-disable-next-line vue/v-slot-style -->
            <template v-slot:activator="{ on, attrs }">
              <a href="javascript:void(0);" v-bind="attrs" v-on="on"
                >About Us <span class="caret"></span>
              </a>
            </template>
            <v-container>
              <v-row>
                <v-col cols="12">
                  <v-list dark>
                    <v-list-item link to="/manifesto"> Manifesto </v-list-item>
                    <v-list-item link to="/team"> Team </v-list-item>
                  </v-list></v-col
                >
              </v-row>
            </v-container>
          </v-menu>
        </li>
        <li>
          <nuxt-link to="">Contact Us</nuxt-link>
        </li>
      </ul>
      <a class="toggle d-none" @click.stop="drawer = !drawer">
        <v-icon> mdi-menu </v-icon>
      </a>
    </div>
    <v-main>
      <nuxt />
    </v-main>
    <div class="contact-wrap">
      <v-container>
        <v-row>
          <v-col md="10" offset-md="1" cols="12" class="pb-0">
            <h3>Contact Us</h3>
            <v-row>
              <v-col cols="12" md="6">
                <h5>Bandung Home Base</h5>
                <p>Jl. Taman Radio Dalam Raya no 28, Jakarta Selatan</p>
                <h5>Say something nice</h5>
                <a href="mailto:contact@kolaborasi.co"
                  ><v-icon>far fa-envelope</v-icon> Contact@kolaborasi.co</a
                >
                <div class="clearfix"></div>
                <a href="http://wa.link/pmub9a"
                  ><v-icon>fab fa-whatsapp</v-icon> 087828469295</a
                >

                <h5 class="mt-4">Social Media</h5>
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
              <v-col cols="12" md="6">
                <h5>Send Us a Message</h5>
                <validation-observer ref="observer">
                  <form id="contactForm" @submit.prevent="submit">
                    <validation-provider
                      v-slot="{ errors }"
                      name="Your Name"
                      rules="required"
                    >
                      <v-text-field
                        v-model="form.name"
                        :error-messages="errors"
                        label="Your Name"
                        name="name"
                        required
                      ></v-text-field>
                    </validation-provider>
                    <validation-provider
                      v-slot="{ errors }"
                      name="Your Email"
                      rules="required|email"
                    >
                      <v-text-field
                        v-model="form.email"
                        :error-messages="errors"
                        label="Your E-mail"
                        name="email"
                        required
                      ></v-text-field>
                    </validation-provider>
                    <validation-provider
                      v-slot="{ errors }"
                      name="Your Message"
                      rules="required"
                    >
                      <v-textarea
                        v-model="form.message"
                        :error-messages="errors"
                        label="Your Message"
                        name="message"
                        required
                        auto-grow
                      ></v-textarea>
                    </validation-provider>
                    <button class="btn btn-primary yellow mt-5" type="submit">
                      <span>Send Message</span>
                    </button>
                  </form>
                </validation-observer>
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
