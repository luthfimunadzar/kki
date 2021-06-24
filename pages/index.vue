<template>
  <div>
    <div class="hero">
      <v-container>
        <v-row>
          <v-col cols="12" md="10" offset-md="1" class="position-relative">
            <v-carousel :hide-delimiters="true" :cycle="true">
              <v-carousel-item v-for="headline in headlines" :key="headline.id">
                <h2>
                  {{ headline.text }}
                </h2>
              </v-carousel-item>
            </v-carousel>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="quiz-wrap">
      <v-container>
        <v-row>
          <v-col md="10" offset-md="1" cols="12">
            <nuxt-link class="go-quiz" to="/quiz">
              <p>Do you have what it takes to be a HYPER Founder?</p>
              <span>Start the Quiz!</span>
            </nuxt-link>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="hyper-wrap">
      <v-container>
        <v-row>
          <v-col md="10" offset-md="1" cols="12">
            <h3>What is HYPER Founder?</h3>
            <v-tabs v-model="tab" align-with-title>
              <v-tab v-for="item in tabItems" :key="item">
                {{ item }}
              </v-tab>
            </v-tabs>

            <v-tabs-items v-model="tab">
              <v-tab-item>
                <v-card flat>
                  <v-card-text>
                    <h5>High Conviction</h5>
                    <p>
                      High Conviction founders are willing to take risks, make
                      tough decisions and go the distance to the company's
                      vision and values. Their conviction also makes them calm
                      in facing problems, faithfully advance through each
                      milestone, and firmly believe in the process.
                    </p>
                  </v-card-text>
                </v-card>
              </v-tab-item>
              <v-tab-item>
                <v-card flat>
                  <v-card-text>
                    <h5 class="blue">Youthful Spirit</h5>
                    <p>
                      Age is just a number. Founders with youthful spirit are
                      always eager to learn something new, always open-minded,
                      can keep things fun, and know when to be playful. Such
                      demeanors will likely make people more open to them,
                      making the team can safely express themselves.
                    </p>
                  </v-card-text>
                </v-card>
              </v-tab-item>
              <v-tab-item>
                <v-card flat>
                  <v-card-text>
                    <h5 class="cyan">Persuasive Leadership</h5>
                    <p>
                      With the charisma to “move” people, the persuasive leader
                      is not necessarily the most skillful or the most senior of
                      the team. Through many or little words, the founder is
                      able to communicate their belief and messages in ways that
                      inspire action, invoke spirit, and even rally support.
                    </p>
                  </v-card-text>
                </v-card>
              </v-tab-item>
              <v-tab-item>
                <v-card flat>
                  <v-card-text>
                    <h5 class="yellow">Entrepreneurial</h5>
                    <p>
                      With high initiative and ability to see opportunities in
                      various situations, Entrepreneurial founders focus on
                      multiplying values through deep understanding of the
                      industry. Entrepreneurial founders are alo resourceful,
                      able to survive in dire situations, and know when to rely
                      on a team.
                    </p>
                  </v-card-text>
                </v-card>
              </v-tab-item>
              <v-tab-item>
                <v-card flat>
                  <v-card-text>
                    <h5 class="green">Rational</h5>
                    <p>
                      Foresee the future, act for the present. With a solid grip
                      on reality and analytical thinking, Rational founders can
                      break down their vision into actionable tasks. They know
                      the importance of building the fundamentals and solve
                      current problems before focusing on the future they are
                      trying to build.
                    </p>
                  </v-card-text>
                </v-card>
              </v-tab-item>
            </v-tabs-items>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="founder-wrap">
      <v-container>
        <v-row>
          <v-col md="10" offset-md="1" cols="12" class="pb-0">
            <h3>Our HYPER Founders</h3>
            <v-carousel :show-arrows="false">
              <v-carousel-item v-for="item in founders" :key="item.id">
                <h4>{{ item.name }}</h4>
                <p>{{ item.desc }}</p>
                <a>Founders Proﬁle</a>
                <div class="clearfix"></div>
                <img :src="item.img" alt="" />
              </v-carousel-item>
            </v-carousel>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="program-wrap">
      <v-container>
        <v-row>
          <v-col md="10" offset-md="1" cols="12" class="pb-0">
            <h3>Programs & Services</h3>
            <v-row>
              <v-col sm="6" cols="12">
                <div class="item-programs">
                  <h4>What we do</h4>
                  <img src="/what-we-do.png" alt="" />
                  <p>
                    Sure, we provide mentorship, access to resources, strategic
                    decisions, and other “high level” tasks. But we also work
                    with you. Like actually working with you.
                  </p>
                </div>
              </v-col>
              <v-col sm="6" cols="12">
                <div class="item-programs w-border">
                  <h4>What will you get</h4>
                  <img src="/what-will-you-get.png" alt="" />
                  <p>
                    Partners who know ways around the potholes and how to reach
                    the pots of gold. Together we’ll seize opportunities while
                    having some laughs along the way.
                  </p>
                </div>
              </v-col>
              <v-col cols="12">
                <h4 class="text-center">Our Specialties</h4>
                <v-row>
                  <v-col md="3" sm="6" cols="12">
                    <div class="item-service">
                      <h5>
                        Incubation<br />
                        Join the club
                      </h5>
                      <img src="/service-1.png" alt="" />
                    </div>
                  </v-col>
                  <v-col md="3" sm="6" cols="12">
                    <div class="item-service second">
                      <h5>
                        Phantom<br />
                        Back end assistance
                      </h5>
                      <img src="/service-2.png" alt="" />
                    </div>
                  </v-col>
                  <v-col md="3" sm="6" cols="12">
                    <div class="item-service third">
                      <h5>
                        Telepath<br />
                        Go to market
                      </h5>
                      <img src="/service-3.png" alt="" />
                    </div>
                  </v-col>
                  <v-col md="3" sm="6" cols="12">
                    <div class="item-service four">
                      <h5>
                        Metamorph<br />
                        Product development
                      </h5>
                      <img src="/service-4.png" alt="" />
                    </div>
                  </v-col>
                </v-row>
                <div class="text-center mt-8">
                  <a class="btn btn-primary d-inline-block red"
                    ><span>All Programs & Services</span></a
                  >
                </div>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="contact-wrap">
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
  </div>
</template>

<script>
import Vue from 'vue'

export default {
  data() {
    return {
      form: {
        name: null,
        email: null,
        message: null,
      },
      result: false,
      quiz: false,
      tab: null,
      tabItems: ['H', 'Y', 'P', 'E', 'R'],
      answer: [],
      hiddenQestion: [],
      headlines: [
        {
          id: 1,
          text: 'We help founders build their dream through venture building program',
        },
        {
          id: 2,
          text: 'Unleashing the HYPER in you.',
        },
        {
          id: 3,
          text: 'We guide founders.',
        },
        {
          id: 4,
          text: 'We grow founders.',
        },
        {
          id: 5,
          text: 'We work with founders.',
        },
      ],
      question: [
        {
          id: 1,
          quiz: 'How much risk do you like to take in life?',
          answer_a: 'As little as possible',
          answer_b: 'I get a buzz from taking crazy risks all the time',
        },
        {
          id: 2,
          quiz: 'Nam eget ornare mauris. In ultrices augue ac leo semper?',
          answer_a: 'vel ultricies eros cursus',
          answer_b: 'Sed non mauris vel velit aliquam',
        },
        {
          id: 3,
          quiz: 'bibendum velit at, placerat mauris?',
          answer_a: 'porttitor eget at felis',
          answer_b: 'Sed ut odio volutpat',
        },
        {
          id: 4,
          quiz: 'Pellentesque iaculis, risus sed mollis tempor?',
          answer_a: 'sapien massa auctor erat',
          answer_b: 'a eleifend tellus odio',
        },
      ],
      founders: [
        {
          id: 1,
          img: '/people.png',
          name: 'Rizky Fadhilah - Rational',
          desc: 'Rizky sees opportunity amidst the chaotic nature of city development. Equipped with his engineering skill in urban planning, he creates solutions & new business ecosystems to help government & business plan the city better with technology.',
        },
        {
          id: 2,
          img: '/people.png',
          name: 'Yohanes S. - High Conviction',
          desc: 'Yohanes “Oyong” believes that farmers are the leftovers & victims of economic development. He envision a future where empowered farmer become a significant player in the industry by equipping them with technology & entrepreneurial skills',
        },
        {
          id: 3,
          img: '/people.png',
          name: 'Wendy Pratama - Youthful spirit',
          desc: 'As an architecture graduate, he built his company like he built his home. Started by building his team, as the foundation. He built a family where people can have fun, pursue their passion, do things that they want to, while achieving the common goals of providing an alternative education program for people to upgrade their life & career.',
        },
        {
          id: 4,
          img: '/people.png',
          name: 'Ivan Lalamentik - Entrepreneurial',
          desc: 'As a lawyer, Ivan understands the legal industry is full of intrigue yet strictly regulated. but with his entrepreneurial point of view he found new business opportunities and swiftly pioneered a solution to the problem faced by the emerging market of legal services.',
        },
        {
          id: 5,
          img: '/people.png',
          name: 'Rhaka - Youthful spirit',
          desc: 'Rhaka is able to convert his trauma of addiction and dropping out of college into a positive energy to move forward. So he understands at heart, that business is not only about money, but more a meaningful and fulfilling way of living while helping other people to become a better person',
        },
        {
          id: 6,
          img: '/people.png',
          name: 'Firman - Entrepreneurial',
          desc: 'Firman is a resilient and resourceful educator/technocrat. He is able to withstand the ups and downs of Robonesia and able to fill multiple strategic roles to grow Robonesia. His ability to nimbly overcome many challenges further proves his spirit and versatility.',
        },
        {
          id: 7,
          img: '/people.png',
          name: 'Nuwi - Persuasive Leadership',
          desc: 'With experience in social enterprise, knowledge about economic development, and ability as a fluent public speaker. She is able to persuade and move stakeholders from government, private investors, to local business owners and give back to the village by co-establishing a social enterprise locally owned by the village community.',
        },
        {
          id: 8,
          img: '/people.png',
          name: 'Aisha - High Conviction',
          desc: 'Aisha believes early education is the most important yet often overlooked education sector in Indonesia. Combined with her passion of visual design, she combined education & content to be accessible for parents and kids anytime, anywhere.',
        },
      ],
    }
  },
  head() {
    return {
      title: 'Kolaborasi.co',
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        {
          hid: 'description',
          name: 'description',
          content:
            'Empowering HYPER Founders to build enduring great business that influence positive change for humanity.',
        },
        { hid: 'og:title', name: 'og:title', content: 'Kolaborasi.co' },
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
    pickQuiz(index, value) {
      Vue.set(this.answer, index, value)
      setTimeout(() => {
        Vue.set(this.hiddenQestion, index, 'hide')
        if (this.hiddenQestion[this.question.length - 1] === 'hide') {
          this.result = true
        }
      }, 1000)
    },
    resetTest() {
      this.answer = []
      this.hiddenQestion = []
      this.result = false
    },
    quizBack(index) {
      Vue.set(this.hiddenQestion, index - 1, null)
    },
    showQuiz() {
      this.quiz = true
    },
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
