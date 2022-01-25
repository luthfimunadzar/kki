<template>
  <div>
    <div class="contact-wrap white">
      <v-container>
        <v-row>
          <v-col md="10" offset-md="1" cols="12" class="pb-0">
            <div class="yellow-wrap">
              <v-row align="center" justify="center">
                <v-col cols="10" md="8" sm="8" class="text-center">
                  <h3 class="mb-4">Join our Hyper Hunt trial session!</h3>
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
                        name="Your Phone Number"
                        rules="required"
                      >
                        <v-text-field
                          v-model="form.phone"
                          :error-messages="errors"
                          label="Your Phone Number"
                          name="phone"
                          required
                        ></v-text-field>
                      </validation-provider>
                      <validation-provider
                        v-slot="{ errors }"
                        name="Your business website and/or social media"
                        rules="required"
                      >
                        <v-text-field
                          v-model="form.website_social"
                          :error-messages="errors"
                          label="Your business website and/or social media"
                          name="website_social"
                          required
                        ></v-text-field>
                      </validation-provider>
                      <validation-provider
                        v-slot="{ errors }"
                        name="Short description about your business
"
                        rules="required"
                      >
                        <v-textarea
                          v-model="form.description"
                          :error-messages="errors"
                          label="Short description about your business
"
                          name="message"
                          required
                          auto-grow
                        ></v-textarea>
                      </validation-provider>
                      <validation-provider
                        v-slot="{ errors }"
                        name="Your google drive link to your business deck"
                        rules="required"
                      >
                        <v-text-field
                          v-model="form.link_business"
                          :error-messages="errors"
                          label="Your google drive link to your business deck"
                          name="link_business"
                          required
                        ></v-text-field>
                      </validation-provider>
                      <button
                        class="btn btn-primary d-inline-block red mt-5"
                        type="submit"
                      >
                        <span>Send Message</span>
                      </button>
                    </form>
                  </validation-observer>
                </v-col>
              </v-row>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        name: null,
        email: null,
        phone: null,
        website_social: null,
        description: null,
        link_business: null,
      },
    }
  },
  head() {
    return {
      title: 'Kolaborasi.co | Hyper Hunt',
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        {
          hid: 'description',
          name: 'description',
          content:
            'Empowering HYPER Founders to build enduring great business that influence positive change for humanity.',
        },
        {
          hid: 'og:title',
          name: 'og:title',
          content: 'Kolaborasi.co | Hyper Hunt',
        },
        {
          hid: 'keywords',
          name: 'keywords',
          content:
            'kolaborasi, kolaborasi kapital indonesia, startup, incubator',
        },
        {
          hid: 'og:description',
          name: 'og:description',
          content:
            'Empowering HYPER Founders to build enduring great business that influence positive change for humanity.',
        },
      ],
    }
  },
  methods: {
    submit() {
      const scriptURL =
        'https://script.google.com/macros/s/AKfycbzQ2tl6awEZIqhnnSpgmQbegScB27R0Ov7limadQH24BnsNYYJNKLS91BgTmVwKBpiUYA/exec'
      const sendingData = new FormData()
      sendingData.append('name', this.form.name)
      sendingData.append('email', this.form.email)
      sendingData.append('phone', this.form.phone)
      sendingData.append('website_social', this.form.website_social)
      sendingData.append('description', this.form.description)
      sendingData.append('link_business', this.form.link_business)

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
      this.form.phone = null
      this.form.website_social = null
      this.form.description = null
      this.form.link_business = null
      this.$refs.observer.reset()
    },
  },
}
</script>
