<template>
  <v-app dark>
    <v-main>
      <nuxt />
    </v-main>
    <div v-if="$route.fullPath.indexOf('contact') - 1" class="contact-wrap">
      <v-container>
        <v-row>
          <v-col md="10" offset-md="1" cols="12" class="pb-0">
            <h3>Contact Us</h3>
            <v-row>
              <v-col cols="12" md="6">
                <h5>Bandung Home Base</h5>
                <p>
                  Freenovation Dago<br />
                  Perumahan Kampung Padi B11<br />
                  Dago Pojok, Bandung, West Java,<br />
                  Indonesia 40135
                </p>
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
    <Top />
    <nuxt-link to="/" class="back-to-kolaborasi">
      <label for="">Back to </label>
      <img src="/logo.png" alt="" />
    </nuxt-link>
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
