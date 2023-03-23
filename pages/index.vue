<template>
  <div>
    <div class="hero-new">
      <div class="wrap">
        <h1>Best Partner for Founders</h1>
        <p>
          Empowering founders to build enduring great <br />
          business that inﬂuence positive change for humanity.
        </p>
      </div>
      <a
        href="javascript:void(0);"
        class="scroll-bot"
        @click="scrollToElement('#growth')"
        ><img src="/arrow-bot.png" alt=""
      /></a>
    </div>
    <div id="growth" class="growth-new">
      <v-container>
        <v-row>
          <v-col sm="8" md="6" offset-sm="2" offset-md="3" cols="12">
            <h4>We are a venture builder company, offering a better</h4>
            <h5>way to build & grow your business</h5>
            <p>
              Built by founders for founders. We believe founders are the
              ultimate agents of positive and transformational change across
              every aspect of our society & economy. Our mission is to spur this
              progress forward. So every single aspect of our company, every
              part of our culture, and every decision we take, is designed with
              the ambition of helping founders succeed.
            </p>
            <div class="stat">
              <h3>9+</h3>
              <span>Years of experience</span>
            </div>
            <div class="stat">
              <h3>12+</h3>
              <span>Portfolios supported</span>
            </div>
            <div class="stat">
              <h3>30+</h3>
              <span>Cofounder involved </span>
            </div>
            <div class="stat big">
              <h3>USD 10 Mio</h3>
              <span>External investment raised in all portfolios combined</span>
            </div>
          </v-col>
          <v-col cols="12">
            <div class="portfolio-new">
              <h5>Our Portfolios</h5>
              <div class="portfolio-item">
                <img src="/p1.png" alt="" />
                <p>Menjadimanusia.id</p>
                <span>Media + Content</span>
              </div>
              <div class="portfolio-item">
                <img src="/p2.png" alt="" />
                <p>Crowde.co</p>
                <span>Agritech + Fintech</span>
              </div>
              <div class="portfolio-item">
                <img src="/p3.png" alt="" />
                <p>Lingkaran.co</p>
                <span>Edtech</span>
              </div>
              <div class="portfolio-item">
                <img src="/p4.png" alt="" />
                <p>@suneatercoven</p>
                <span>Music Agency</span>
              </div>
              <div class="portfolio-item">
                <img src="/p5.png" alt="" />
                <p>Cityplan.id</p>
                <span>SaaS + Proptech</span>
              </div>
              <div class="portfolio-item">
                <img src="/p6.png" alt="" />
                <p>Lexar.id</p>
                <span>Regulation Technology</span>
              </div>
              <div class="portfolio-item">
                <img src="/p7.png" alt="" />
                <p>@tenniskuy</p>
                <span>Sports Community</span>
              </div>
              <div class="portfolio-item">
                <img src="/p8.png" alt="" />
                <p>Brocode Barbershop</p>
                <span>Lifestyle Service</span>
              </div>
              <div class="portfolio-item">
                <img src="/p9.png" alt="" />
                <p>bacapibo.com</p>
                <span>Edtech + Content</span>
              </div>
              <div class="portfolio-item">
                <img src="/p10.png" alt="" />
                <p>Robonesia.id</p>
                <span>Education + Robotics</span>
              </div>
              <div class="portfolio-item">
                <img src="/p11.png" alt="" />
                <p>Berdaya.co</p>
                <span>Village Development</span>
              </div>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="image-sect-new">
      <div class="bg" style="background-image: url('/sect1.png')"></div>
      <v-container>
        <v-row>
          <v-col sm="6">
            <h2>Venture Builder</h2>
            <h5>Building Tomorrow, Today</h5>
            <p>
              Our signature program, where we partner up with ambitious founder,
              the rule-breakers who want to be the leader in their category, the
              world-shapers who want to fundamentally shift the way we live
              today. Venture Builder Is a lifetime support for early to product
              stage startup. We’ll act as a venture partner for your company.
              Get our skins in the game and work directly with your team within
              multiple role to achieve your next growth objectives.
            </p>
            <nuxt-link to="/venture-builder" class="btn-circle"
              >Learn More</nuxt-link
            >
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="image-sect-new reverse">
      <div class="bg" style="background-image: url('/sect2.png')"></div>
      <v-container>
        <v-row>
          <v-col sm="6" offset-sm="6">
            <h2>Venture Service</h2>
            <h5>Get Things Done, Better</h5>
            <p>
              Our signature service, where we provide a Business Process
              Outsourcing (BPO) service tailored to early stage business. With
              monthly subscription scheme, you can get professional services in
              Marketing, Finance, HR, Legal, Fundraising & Impact Management
              tailored to your business needs. With the best practices gathered
              from our 10 years of experiences handling businesses in various
              industries, we know exactly what needs to be done, and how to do
              it better & faster.
            </p>
            <nuxt-link to="/venture-service" class="btn-circle"
              >Learn More</nuxt-link
            >
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
