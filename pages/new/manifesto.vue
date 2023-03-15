<template>
  <div>
    <div class="hero-new short">
      <div class="wrap">
        <div class="breadcrumb-new">
          About Us <span class="circle"></span> Portfolio
        </div>
        <h1>We are true to our values</h1>
        <p>
          We work closely with our founders to understand their needs and goals,
          and we involve them in every step of the process, from ideation to
          execution. We take a partnership approach, working alongside our
          founders as a trusted and reliable resource.
        </p>
      </div>
    </div>
    <div class="manifest-wrap">
      <v-container>
        <v-row class="d-flex align-center">
          <v-col cols="12" md="6" order-md="2">
            <div
              class="circle-img"
              style="background-image: url('/Manifesto-Empower-Founder.png')"
            ></div>
          </v-col>
          <v-col cols="12" md="6" order-md="1">
            <h2>We <span class="bg-reds">empower</span> founders</h2>
            <p>
              We are founded by entrepreneurs, for entrepreneurs. We know what
              it takes to build a successful business, and we are dedicated to
              helping our founders achieve their visions. We take a hands-on
              approach, providing guidance, mentorship, and strategic support to
              help our founders overcome challenges and capitalize on
              opportunities.
            </p>
          </v-col>
        </v-row>
        <v-row class="d-flex align-center">
          <v-col cols="12" md="6">
            <div
              class="circle-img second"
              style="background-image: url('/Manifesto-Collaboration.png')"
            ></div>
          </v-col>
          <v-col cols="12" md="6">
            <h2>We seek out <span class="bg-reds">collaboration</span></h2>
            <p>
              We believe in building strong and collaborative partnerships with
              our founders, working together as a team to achieve their goals.
              We take the time to get to know our founders and their unique
              needs, and we involve them in every step of the process, from
              initial ideation to final execution. We believe that open
              communication and collaboration is the key to success, and we are
              committed to building long-term relationships with our founders.
            </p>
          </v-col>
        </v-row>
        <v-row class="d-flex align-center">
          <v-col cols="12" md="6" order-md="2">
            <div
              class="circle-img"
              style="background-image: url('/Manifesto-Great-Vision.png')"
            ></div>
          </v-col>
          <v-col cols="12" md="6" order-md="1">
            <h2>We focus on <span class="bg-reds">great vision</span></h2>
            <p>
              We take a long-term approach to venture building, focused on
              creating sustainable and successful businesses that will stand the
              test of time. We are not just interested in quick wins, but in
              building enduring companies that can make a real impact in the
              world. We believe that by taking a patient and strategic approach,
              we can create real value for our founders and investors alike.
            </p>
          </v-col>
        </v-row>
        <v-row class="d-flex align-center">
          <v-col cols="12" md="6">
            <div
              class="circle-img second"
              style="background-image: url('/Manifesto-Growth.png')"
            ></div>
          </v-col>
          <v-col cols="12" md="6">
            <h2>We strive for <span class="bg-reds">growth</span></h2>
            <p>
              Our team brings a wealth of experience and network to the table,
              having successfully built and scaled multiple companies. We
              leverage this experience and network to help our founders overcome
              challenges, identify opportunities, and connect with the right
              people. We believe that the right network and experience can make
              all the difference in the success of a startup, and we are
              committed to sharing our knowledge and resources with our
              founders.
            </p>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<script>
import Vue from 'vue'

export default {
  layout: 'new',
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
          img: '/people12.png',
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
    scrollToElement(val) {
      const el = this.$el.querySelector(val)

      if (el) {
        // Use el.scrollIntoView() to instantly scroll to the element
        el.scrollIntoView({ behavior: 'smooth' })
      }
    },
  },
}
</script>
