<template>
  <div>
    <div class="hero">
      <v-container>
        <v-row>
          <v-col cols="12" md="10" offset-md="1" class="position-relative">
            <v-carousel
              :hide-delimiters="true"
              :show-arrows="false"
              :cycle="true"
              interval="6000"
            >
              <v-carousel-item>
                <h2>
                  We help founders build their dream through venture building
                  program
                </h2>
              </v-carousel-item>
              <v-carousel-item>
                <h2>Unleashing the HYPER in you.</h2>
              </v-carousel-item>
              <v-carousel-item>
                <h2>
                  We <em class="mr-2">guide</em> founders. <br />
                  We <em class="mr-2">grow</em> founders.<br />
                  We <em class="mr-2">work</em> with founders.
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
                <h4 class="mb-1">{{ item.name }}</h4>
                <p class="font-weight-bold">{{ item.title }}</p>
                <p>{{ item.desc }}</p>
                <a :href="item.link" target="_blank">Founders Proﬁle</a>
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
                  <h4>Join Hyper Founder Program</h4>
                  <img src="/what-we-do.png" alt="" />
                  <p>
                    We act as a venture partners providing mentorship, network
                    support & work assistance to help you get things done in
                    exchange of a small percentage of equity for a lifetime
                    support.
                  </p>
                </div>
              </v-col>
              <v-col sm="6" cols="12">
                <div class="item-programs w-border">
                  <h4>Get Our Service</h4>
                  <img src="/what-will-you-get.png" alt="" />
                  <p>
                    We provide professional agency service tailored to early
                    stage business in Creative Marketing, Back Office &
                    Financial Assistance with affordable monthly subscription.
                  </p>
                </div>
              </v-col>
              <v-col cols="12">
                <div class="text-center mt-8">
                  <nuxt-link
                    class="btn btn-primary d-inline-block red"
                    to="/programs"
                    ><span>All Programs & Services</span>
                  </nuxt-link>
                </div>
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
      result: false,
      quiz: false,
      tab: null,
      tabItems: ['H', 'Y', 'P', 'E', 'R'],
      answer: [],
      hiddenQestion: [],
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
          img: '/people6.png',
          name: 'Rizky Fadhilah',
          title: 'Founder and CEO at Cityplan Indonesia',
          desc: 'Rizky sees opportunity amidst the chaotic nature of city development. Equipped with his engineering skill in urban planning, he creates solutions & new business ecosystems to help government & business plan the city better with technology.',
          link: 'https://www.linkedin.com/in/rizki-fadhilah-6b351979/',
        },
        {
          id: 2,
          img: '/people9.png',
          name: 'Yohanes S.',
          title: 'CEO at CROWDE.CO',
          desc: 'Yohanes “Oyong” believes that farmers are the leftovers & victims of economic development. He envision a future where empowered farmer become a significant player in the industry by equipping them with technology & entrepreneurial skills',
          link: 'https://www.linkedin.com/in/yohanes-sugihtononugroho-aabb8b116/',
        },
        {
          id: 3,
          img: '/people10.png',
          name: 'Wendy Pratama',
          title: 'CEO at Lingkaran',
          desc: 'As an architecture graduate, he built his company like he built his home. Started by building his team, as the foundation. He built a family where people can have fun, pursue their passion, do things that they want to, while achieving the common goals of providing an alternative education program for people to upgrade their life & career.',
          link: 'https://www.linkedin.com/in/wndprtm/',
        },
        {
          id: 4,
          img: '/people5.png',
          name: 'Ivan',
          title: 'Managing Director of LEXAR.id',
          desc: 'As a lawyer, Ivan understands the legal industry is full of intrigue yet strictly regulated. but with his entrepreneurial point of view he found new business opportunities and swiftly pioneered a solution to the problem faced by the emerging market of legal services.',
          link: 'https://www.linkedin.com/in/ivan-lalamentik-81a04574/',
        },
        {
          id: 5,
          img: '/people.png',
          name: 'Rhaka',
          title: 'Co Founder at Menjadi Manusia',
          desc: 'Rhaka is able to convert his trauma of addiction and dropping out of college into a positive energy to move forward. So he understands at heart, that business is not only about money, but more a meaningful and fulfilling way of living while helping other people to become a better person',
          link: 'https://www.linkedin.com/in/rhaka-ghanisatria-b0924a108/',
        },
        {
          id: 6,
          img: '/people8.png',
          name: 'Firman',
          title: 'Founder & CEO Robonesia.ID',
          desc: 'Firman is a resilient and resourceful educator/technocrat. He is able to withstand the ups and downs of Robonesia and able to fill multiple strategic roles to grow Robonesia. His ability to nimbly overcome many challenges further proves his spirit and versatility.',
          link: 'https://www.linkedin.com/in/firman-alimuddin-69501a110/',
        },
        {
          id: 7,
          img: '/people7.png',
          name: 'Nuwi',
          title: 'Strategic Director of BerdayaKrui',
          desc: 'With experience in social enterprise, knowledge about economic development, and ability as a fluent public speaker. She is able to persuade and move stakeholders from government, private investors, to local business owners and give back to the village by co-establishing a social enterprise locally owned by the village community.',
          link: 'https://www.linkedin.com/in/safrina/',
        },
        {
          id: 8,
          img: '/people11.png',
          name: 'Mayumi',
          title: 'Founder of PiBo',
          desc: 'Mayumi believes early education is the most important yet often overlooked education sector in Indonesia. Combined with her passion for visual design, she combined education & content to be accessible for parents and kids anytime, anywhere.',
          link: 'https://www.linkedin.com/in/mayumi-haryoto-945213190/',
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
  },
}
</script>
