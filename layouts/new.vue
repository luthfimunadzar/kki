<template>
  <v-app dark class="overflow-x-hidden">
    <v-navigation-drawer v-model="drawer" right absolute temporary>
      <ul class="main-menu-sidebar">
        <li>
          <nuxt-link to="/">Home</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/venture-builder">Venture Builder</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/portfolio">Portofolio</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/service/finance">Financial & Tax</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/service/content-design">Content & Design</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/service/human-resources">Human Resources</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/service/impact-management"
            >Impact Management</nuxt-link
          >
        </li>
        <li>
          <nuxt-link to="/service/fundraising-preparation"
            >Fundraising Preparation</nuxt-link
          >
        </li>
        <li>
          <nuxt-link to="/manifesto">Manifesto</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/team">Team</nuxt-link>
        </li>
        <li>
          <nuxt-link to="">Contact Us</nuxt-link>
        </li>
      </ul>
    </v-navigation-drawer>
    <div class="header-new">
      <nuxt-link to="/">
        <img src="/logo.png" alt="" class="logo" />
      </nuxt-link>
      <a class="toggle" @click.stop="drawer = !drawer">
        <v-icon> mdi-menu </v-icon>
      </a>
      <ul class="main-menu">
        <li>
          <nuxt-link to="/">Home</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/portfolio">Portofolio</nuxt-link>
        </li>
        <li>
          <nuxt-link to="/venture-builder">Venture Builder</nuxt-link>
        </li>
        <!-- <li>
          <v-menu offset-y content-class="dropdown-menu-new">
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
        </li> -->
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
          <a
            href="https://api.whatsapp.com/send?phone=6287828469295&text=Hello%20Kolaborasi%2C%20saya%20tertarik%20dengan%20..."
            target="_blank"
            >Contact Us</a
          >
        </li>
      </ul>
      <a class="toggle d-none" @click.stop="drawer = !drawer">
        <v-icon> mdi-menu </v-icon>
      </a>
    </div>
    <v-main>
      <nuxt />
    </v-main>
    <div class="subscribe">
      <v-container>
        <v-row>
          <v-col cols="12" sm="12">
            <div id="mc_embed_shell">
              <link
                href="//cdn-images.mailchimp.com/embedcode/classic-061523.css"
                rel="stylesheet"
                type="text/css"
              />
              <style type="text/css">
                #mc_embed_signup{background:#fff; false;clear:left; font:14px Helvetica,Arial,sans-serif; width: px;}
                /* Add your own Mailchimp form style overrides in your site stylesheet or in this style block.
                  We recommend moving this block and the preceding CSS link to the HEAD of your HTML file. */
              </style>
              <div id="mc_embed_signup">
                <h2>Subscribe now</h2>
                <form
                  id="mc-embedded-subscribe-form"
                  action="https://kolaborasi.us21.list-manage.com/subscribe/post?u=9a6607fc67bd55e6301ed4d89&amp;id=64211357f3&amp;f_id=0018fee6f0"
                  method="post"
                  name="mc-embedded-subscribe-form"
                  class="validate"
                  target="_blank"
                >
                  <div id="mc_embed_signup_scroll">
                    <div class="mc-field-group">
                      <input
                        id="mce-EMAIL"
                        type="email"
                        name="EMAIL"
                        class="required email"
                        required=""
                        value=""
                        placeholder="youremail@gmail.com"
                      />
                      <input
                        id="mc-embedded-subscribe"
                        type="submit"
                        name="subscribe"
                        class="button"
                        value="Subscribe"
                      />
                    </div>
                    <div id="mce-responses" class="clear foot">
                      <div
                        id="mce-error-response"
                        class="response"
                        style="display: none"
                      ></div>
                      <div
                        id="mce-success-response"
                        class="response"
                        style="display: none"
                      ></div>
                    </div>
                    <div
                      aria-hidden="true"
                      style="position: absolute; left: -5000px"
                    >
                      /* real people should not fill this in and expect good
                      things - do not remove this or risk form bot signups */
                      <input
                        type="text"
                        name="b_9a6607fc67bd55e6301ed4d89_64211357f3"
                        tabindex="-1"
                        value=""
                      />
                    </div>
                  </div>
                </form>
              </div>
              <script
                type="text/javascript"
                src="//s3.amazonaws.com/downloads.mailchimp.com/js/mc-validate.js"
              ></script>
            </div>
          </v-col>
          <v-col cols="12" sm="12">
            <h4>We'll send you 1-2 newsletter per month about :</h4>
          </v-col>
          <v-col cols="12" sm="4">
            <h6>Program Information</h6>
            <p>
              We'll inform you about our upcoming Venture Builder program &
              Venture Service promotion that can be beneficial for your business
            </p>
          </v-col>
          <v-col cols="12" sm="4">
            <h6>Business & Portfolio Updates</h6>
            <p>
              We'll update you on our startup portfolio latest progress &
              milestone, so you can understand how venture are growing with us
              over the time
            </p>
          </v-col>
          <v-col cols="12" sm="4">
            <h6>Program Information</h6>
            <p>
              We'll share many upcoming opportunities of collaboration and
              partnership with our portfolios companies, so you can be part of
              it
            </p>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <footer class="footer-new">
      <v-container>
        <v-row>
          <v-col cols="12" sm="3" md="3">
            <img src="/kki-white.png" alt="" class="logo" />
          </v-col>
          <v-col cols="12" sm="3" md="4">
            <h3>Contact Us</h3>
            <p>
              Jakarta HQ - Jl Taman Radio Dalam Raya no28, Gandaria Utara,
              Jakarta Selatan 12140
            </p>
            <p>
              Bandung HQ - Komplek Kampung Padi no B11, Dago Pojok, Bandung
              40135
            </p>
          </v-col>
          <v-col cols="12" sm="3" md="3">
            <h3>Site Links</h3>
            <ul>
              <li>
                <nuxt-link to="/venture-builder">Venture Builder</nuxt-link>
              </li>
              <li>
                <nuxt-link to="/venture-service">Venture Service</nuxt-link>
              </li>
              <li><nuxt-link to="/manifesto">Manifesto </nuxt-link></li>
              <li><nuxt-link to="/team">Team </nuxt-link></li>
              <li><nuxt-link to="/portfolio">Portfolios </nuxt-link></li>
            </ul>
          </v-col>
          <v-col cols="12" sm="3" md="2" class="pr-md-0">
            <h3>Follow Us</h3>
            <a
              href="https://www.linkedin.com/company/kolaborasico/mycompany/?viewAsMember=true"
              target="_blank"
              class="socmed"
            >
              <v-icon> fab fa-linkedin </v-icon>
            </a>
            <a
              href="https://www.instagram.com/kolaborasico/"
              target="_blank"
              class="socmed"
            >
              <v-icon> fab fa-instagram </v-icon>
            </a>
            <a href="mailto:contact@kolaborasi.co" class="socmed"
              ><v-icon>far fa-envelope</v-icon></a
            >
            <a
              href="https://api.whatsapp.com/send?phone=6287828469295&text=Hello%20Kolaborasi%2C%20saya%20tertarik%20dengan%20..."
              class="socmed"
              ><v-icon>fab fa-whatsapp</v-icon></a
            >
          </v-col>
        </v-row>
      </v-container>
    </footer>
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
