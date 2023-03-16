<template>
  <div class="sebat">
    <div class="hero-wrap">
      <v-container>
        <v-row>
          <v-col cols="12">
            <img
              src="/logo-sbat.png"
              alt=""
              class="mx-auto my-3 d-block"
              width="131"
            />
            <h1>So you’re a startup founder?</h1>
          </v-col>
          <v-col cols="12" lg="8" offset-lg="2">
            <v-row>
              <v-col cols="12" md="4">
                <v-card>
                  <img src="/sbat-hero1.png" alt="" />
                  <h5>Feeling Lonely</h5>
                  <p>No one understands your struggle</p>

                  <v-icon> fas fa-check </v-icon>
                </v-card>
              </v-col>
              <v-col cols="12" md="4">
                <v-card>
                  <img src="/sbat-hero2.png" alt="" />
                  <h5>Stuck in Tunnel Vision</h5>
                  <p>Day-to-day tasks narrow your perspective</p>

                  <v-icon> fas fa-check </v-icon>
                </v-card>
              </v-col>
              <v-col cols="12" md="4">
                <v-card>
                  <img src="/sbat-hero3.png" alt="" />
                  <h5>Doing everything</h5>
                  <p>Finance, Marketing, Operations, you’re doing it all!</p>

                  <v-icon> fas fa-check </v-icon>
                </v-card>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </div>

    <div class="chill">
      <v-container>
        <v-row>
          <v-col cols="12">
            <h5>You need to chill and</h5>
            <img src="/img-rokok.png" alt="" class="rokok" />
            <img src="/logo-sbat.png" alt="" class="logo-sbat" />
          </v-col>
        </v-row>
      </v-container>
    </div>

    <div class="program-inner">
      <v-container>
        <v-row class="d-flex align-center">
          <v-col cols="12" md="6">
            <h3>We will be your</h3>
          </v-col>
          <v-col cols="12" md="6">
            <div class="switch-text">
              <img
                src="/text1.png"
                alt=""
                :class="[{ show: word[0] === true }]"
              />
              <img
                src="/text2.png"
                alt=""
                :class="[{ show: word[1] === true }]"
              />
              <img
                src="/text3.png"
                alt=""
                :class="[{ show: word[2] === true }]"
              />
              <img
                src="/text4.png"
                alt=""
                :class="[{ show: word[3] === true }]"
              />
              <img
                src="/text5.png"
                alt=""
                :class="[{ show: word[4] === true }]"
              />
            </div>
          </v-col>
        </v-row>
        <v-row>
          <v-col lg="8" offset-lg="2">
            <h4>10-Sessions Program consists of</h4>
            <div class="item-program first">
              <v-row class="d-flex align-center">
                <v-col cols="12" sm="4">
                  <img
                    src="/program1.png"
                    alt=""
                    class="d-block mx-auto my-0"
                  />
                </v-col>
                <v-col cols="12" sm="8">
                  <h5>Strategic Brainstorming And Troubleshooting</h5>
                  <p>Investigate your issues.</p>
                </v-col>
              </v-row>
            </div>
            <div class="item-program">
              <v-row class="d-flex align-center">
                <v-col cols="12" sm="4">
                  <img
                    src="/program2.png"
                    alt=""
                    class="d-block mx-auto my-0"
                  />
                </v-col>
                <v-col cols="12" sm="8">
                  <h5>Sharing Burden And Tips</h5>
                  <p>Provide and execute actionable insights.</p>
                </v-col>
              </v-row>
            </div>
            <div class="item-program">
              <v-row class="d-flex align-center">
                <v-col cols="12" sm="4">
                  <img
                    src="/program3.png"
                    alt=""
                    class="d-block mx-auto my-0"
                  />
                </v-col>
                <v-col cols="12" sm="8">
                  <h5>Santai Bareng Anak Tongkrongan</h5>
                  <p>Connect, share, and play.</p>
                </v-col>
              </v-row>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="program-output">
      <v-container>
        <v-row>
          <v-col lg="8" offset-lg="2">
            <v-row>
              <v-col cols="12">
                <h4>Program output</h4>
              </v-col>
              <v-col cols="12" sm="4">
                <div class="output-item">
                  <img src="/program4.png" alt="" class="mb-3" />
                  <h5>
                    We can be your cofounder, or we can be at your service
                  </h5>
                </div>
              </v-col>
              <v-col cols="12" sm="4">
                <div class="output-item sec">
                  <img src="/program5.png" alt="" class="mb-3" />
                  <h5>Venture build</h5>
                  <p>We take small equity and do business with you.</p>
                </div>
              </v-col>
              <v-col cols="12" sm="4">
                <div class="output-item thi">
                  <img src="/program6.png" alt="" class="mb-3" />
                  <h5>Service provider</h5>
                  <p>Hire us as your Financial / HR / Marketing Manager.</p>
                </div>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="apply">
      <v-container>
        <v-row>
          <v-col lg="8" offset-lg="2">
            <h4>SBAT application opens in</h4>
            <no-ssr>
              <div class="cd-wrap">
                <countdown
                  :time="new Date(2022, 6, 1) - new Date()"
                  class="countdown"
                >
                  <template slot-scope="props">
                    <v-row>
                      <v-col cols="3">
                        <h6>{{ props.days }}</h6>
                        <span>Days</span>
                      </v-col>
                      <v-col cols="3" class="position-relative">
                        <span class="dots">:</span>
                        <h6>{{ props.hours }}</h6>
                        <span>Hours</span>
                      </v-col>
                      <v-col cols="3" class="position-relative">
                        <span class="dots">:</span>
                        <h6>{{ props.minutes }}</h6>
                        <span>Minutes</span>
                      </v-col>
                      <v-col cols="3" class="position-relative">
                        <span class="dots">:</span>
                        <h6>{{ props.seconds }}</h6>
                        <span>Seconds</span>
                      </v-col>
                    </v-row>
                  </template>
                </countdown>
              </div>
            </no-ssr>

            <validation-observer ref="observer">
              <form id="contactForm" class="form-sbat" @submit.prevent="submit">
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
                    hide-details="auto"
                    required
                  ></v-text-field>
                </validation-provider>
                <button
                  class="btn btn-primary d-inline-block red"
                  type="submit"
                >
                  <span>Notify Me</span>
                </button>
              </form>
            </validation-observer>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<script>
export default {
  layout: 'blank',
  data() {
    return {
      form: {
        email: null,
      },
      works: [
        {
          id: 1,
          img: '/works1.png',
          title: 'Cityplan',
        },
        {
          id: 2,
          img: '/works2.png',
          title: 'Kolaborasi',
        },
        {
          id: 3,
          img: '/works3.png',
          title: 'Lexar',
        },
        {
          id: 4,
          img: '/works4.png',
          title: 'SIAP',
        },
        {
          id: 5,
          img: '/works5.png',
          title: 'MGEE',
        },
      ],
      builds: ['Brand Book', 'Campaign', 'Visual Activation'],
      heros: [
        'enthralling',
        'exciting',
        'funny',
        'memorable',
        'dramatic',
        'lovely',
        'digestible',
        'playful',
        'trustworthy',
      ],
      word: [],
      index: -1,
    }
  },
  head() {
    return {
      title: 'Kolaborasi.co | SBAT',
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
          content: 'Kolaborasi.co | SBAT',
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
  mounted() {
    window.setInterval(() => {
      if (this.index < 4) {
        this.index++
      } else {
        this.word = []
        this.index = 0
      }
      this.word[this.index] = true
      this.$forceUpdate()
    }, 1000)
  },
  methods: {
    changeBuild() {
      const first = this.builds.shift()
      this.builds = this.builds.concat(first)
    },
    changeHeros() {
      const first = this.heros.shift()
      this.heros = this.heros.concat(first)
    },
    submit() {
      const scriptURL =
        'https://script.google.com/macros/s/AKfycbwUQB-VcqHE4UAbiJxw5n1cc5UVkdpZZn-7BV36Q7mfGQvfaqoh6FW3YjBR3Sf2HwYc/exec'
      const sendingData = new FormData()
      sendingData.append('email', this.form.email)

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
      this.form.email = null
      this.$refs.observer.reset()
    },
  },
}
</script>
