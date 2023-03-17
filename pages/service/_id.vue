<template>
  <div>
    <div class="service-head-new">
      <v-container>
        <v-row class="d-flex align-center">
          <v-col cols="12" md="7">
            <div class="breadcrumb-new">
              Venture services <span class="circle"></span> {{ title }}
            </div>
            <h2 class="title-service">{{ slogan }}</h2>
            <p>
              {{ p1 }}
            </p>
            <p>
              {{ p2 }}
            </p>
          </v-col>
          <v-col cols="12" md="5">
            <div
              class="image-circle"
              :class="[
                { cd: $route.params.id === 'content-design' },
                { hr: $route.params.id === 'human-resources' },
                { ft: $route.params.id === 'finance' },
                { fp: $route.params.id === 'fundraising-preparation' },
              ]"
              :style="{ backgroundImage: `url(${bgLanding})` }"
            ></div>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div
      class="service-business"
      :class="[
        { cd: $route.params.id === 'content-design' },
        { hr: $route.params.id === 'human-resources' },
        { ft: $route.params.id === 'finance' },
        { fp: $route.params.id === 'fundraising-preparation' },
      ]"
    >
      <v-container>
        <v-row>
          <v-col cols="12">
            <h2 class="title-service text-center">
              {{ bTitle }}
            </h2>
          </v-col>
        </v-row>
        <v-row class="d-flex align-center">
          <v-col cols="12" md="4">
            <div
              class="image-circle"
              :style="{ backgroundImage: `url(${bgWhy})` }"
            ></div>
          </v-col>
          <v-col cols="12" md="8">
            <div
              v-for="(item, i) in bItem"
              :key="i"
              class="business-item"
              :class="{ active: i === index }"
              @click="setActive(i)"
            >
              <h4>{{ item.title }}</h4>
              <p>{{ item.desc }}</p>
            </div>
          </v-col>
        </v-row>
        <v-row class="d-flex justify-center">
          <v-col cols="12">
            <h2 class="title-service text-center mt-16">Our Services</h2>
          </v-col>
          <v-col v-for="(ser, i) in services" :key="i" cols="4">
            <div class="service-item">
              <h6>{{ ser.title }}</h6>
              <vue-markdown :source="ser.list" />
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="subscribe">
      <v-container>
        <v-row class="d-flex justify-center">
          <v-col cols="12">
            <h2 class="title-service text-center black--text">
              {{ suTitle }}
            </h2>
          </v-col>
          <v-col v-for="(sub, i) in suItem" :key="i" cols="12" md="6">
            <div class="subscribe-item">
              <div
                class="image-wrap"
                :style="{ backgroundImage: `url(${sub.img})` }"
              ></div>
              <h5>{{ sub.title }}</h5>
              <p>
                {{ sub.subtitle }}
              </p>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div
      class="price-new"
      :class="[
        { cd: $route.params.id === 'content-design' },
        { hr: $route.params.id === 'human-resources' },
        { ft: $route.params.id === 'finance' },
        { fp: $route.params.id === 'fundraising-preparation' },
      ]"
    >
      <v-container>
        <v-row>
          <v-col cols="12">
            <h2 class="title-service text-center white--text">
              Packages Prices & Scope of Work
            </h2>
          </v-col>
          <v-col v-if="$route.params.id === 'impact-management'" cols="12">
            <div class="price-wrap">
              <v-row>
                <v-col cols="3">
                  <div class="title no-border"></div>
                  <ul class="scope">
                    <li>First Consultation</li>
                    <li>Impact & Program Advisory</li>
                    <li>Impact Metrics Creationg</li>
                    <li>Framework Creation</li>
                    <li>Data Collection Tools</li>
                    <li>Data Cleansing & Processing</li>
                    <li>Data Visualisation</li>
                    <li>Impact Reporting</li>
                    <li class="text-price font-weight-bold">Pricing</li>
                  </ul>
                </v-col>
                <v-col cols="3" class="border-left">
                  <div class="title">
                    <h5>Package 1</h5>
                    <h3>Entry Level</h3>
                  </div>
                  <ul>
                    <li>Free</li>
                    <li>Weekly</li>
                    <li>6 Hours Consultation</li>
                    <li>-</li>
                    <li>1 Tools</li>
                    <li>-</li>
                    <li>1 Visualisation</li>
                    <li>-</li>
                    <li class="text-price font-weight-bold">
                      IDR7,000,000/Month
                    </li>
                  </ul></v-col
                >
                <v-col cols="3" class="border-left">
                  <div class="title">
                    <h5>Package 2</h5>
                    <h3>Intermediate</h3>
                  </div>
                  <ul>
                    <li>Free</li>
                    <li>Weekly</li>
                    <li>10 Hours Consultation</li>
                    <li>
                      <img src="/bcheck.png" alt="" class="d-block mx-auto" />
                    </li>
                    <li>2 Tools</li>
                    <li>-</li>
                    <li>2 Visualisation</li>
                    <li>2 Pages report</li>
                    <li class="text-price font-weight-bold">
                      IDR10,000,000/Month
                    </li>
                  </ul></v-col
                >
                <v-col cols="3" class="border-left">
                  <div class="title">
                    <h5>Package 3</h5>
                    <h3>Advance</h3>
                  </div>
                  <ul>
                    <li>Free</li>
                    <li>Weekly</li>
                    <li>15 Hours Consultation</li>
                    <li>
                      <img src="/bcheck.png" alt="" class="d-block mx-auto" />
                    </li>
                    <li>3 Tools</li>
                    <li>
                      <img src="/bcheck.png" alt="" class="d-block mx-auto" />
                    </li>
                    <li>3 Visualisation</li>
                    <li>6 Pages report</li>
                    <li class="text-price font-weight-bold">
                      IDR15,000,000/Month
                    </li>
                  </ul></v-col
                >
              </v-row>
            </div>
          </v-col>
          <v-col v-if="$route.params.id === 'content-design'" cols="12">
            <div class="price-wrap">
              <v-row>
                <v-col cols="4">
                  <div class="title">
                    <h3>New Branding Package</h3>
                  </div>
                  <ul>
                    <li>1 Logo & 1 Brand Book</li>
                    <li>10 Marketing Design Template</li>
                    <li>2 Set of Stationary Design</li>
                    <li>5 Set of Illustrative / Icon Assets</li>
                    <li class="text-price font-weight-bold">
                      1 Months @Rp18.000.000
                    </li>
                  </ul></v-col
                >
                <v-col cols="4" class="border-left">
                  <div class="title">
                    <h3>Report & Presentation Design Package</h3>
                  </div>
                  <ul>
                    <li>10 pages of presentation designs</li>
                    <li>10 pages of business copywriting</li>
                    <li>2 Mini infographic</li>
                    <li>2 Unique Graphic Assets / Custom Illustration</li>
                    <li class="text-price font-weight-bold">
                      1 Months @Rp12.000.000
                    </li>
                  </ul></v-col
                >
                <v-col cols="4" class="border-left">
                  <div class="title">
                    <h3>Socmed Content Package</h3>
                  </div>
                  <ul>
                    <li>
                      15 social media images
                      <em>(feed, story, poster, ad banner)</em>
                    </li>
                    <li>
                      15 social media copywriting
                      <em>(caption, poster copy) </em>
                    </li>
                    <li>1 Content guideline</li>
                    <li class="text-price font-weight-bold">
                      1 Months @Rp4.000.000
                    </li>
                  </ul></v-col
                >
              </v-row>
            </div>
          </v-col>
          <v-col v-if="$route.params.id === 'finance'" cols="12">
            <div class="price-wrap">
              <v-row>
                <v-col cols="3">
                  <div class="title no-border"></div>
                  <ul class="scope">
                    <li>First Consultation</li>
                    <li>Bookkeeping</li>
                    <li>Tax Handling</li>
                    <li>Secretarial Documents</li>
                    <li>Cash flow Management</li>
                    <li>Strategic Finance</li>
                    <li>Service Limit</li>
                    <li>Dedicated Team</li>
                    <li class="text-price font-weight-bold">Pricing</li>
                  </ul>
                </v-col>
                <v-col cols="3" class="border-left">
                  <div class="title">
                    <h5>Package 1</h5>
                    <h3>Hands-on Service</h3>
                  </div>
                  <ul>
                    <li>Free</li>
                    <li>
                      <img src="/bcheck4.png" alt="" class="d-block mx-auto" />
                    </li>
                    <li>
                      <img src="/bcheck4.png" alt="" class="d-block mx-auto" />
                    </li>
                    <li>
                      <img src="/bcheck4.png" alt="" class="d-block mx-auto" />
                    </li>
                    <li>
                      <img src="/bcheck4.png" alt="" class="d-block mx-auto" />
                    </li>
                    <li>
                      <img src="/bcheck4.png" alt="" class="d-block mx-auto" />
                    </li>
                    <li>2 Services</li>
                    <li>1</li>
                    <li class="text-price font-weight-bold">
                      IDR3,500,000 (exclude Jurnal account)
                    </li>
                  </ul></v-col
                >
                <v-col cols="3" class="border-left">
                  <div class="title">
                    <h5>Package 2</h5>
                    <h3>On-Demand Service</h3>
                  </div>
                  <ul>
                    <li>Free</li>
                    <li>
                      <img src="/bcheck4.png" alt="" class="d-block mx-auto" />
                    </li>
                    <li>
                      <img src="/bcheck4.png" alt="" class="d-block mx-auto" />
                    </li>
                    <li>
                      <img src="/bcheck4.png" alt="" class="d-block mx-auto" />
                    </li>
                    <li>
                      <img src="/bcheck4.png" alt="" class="d-block mx-auto" />
                    </li>
                    <li>
                      <img src="/bcheck4.png" alt="" class="d-block mx-auto" />
                    </li>
                    <li>5 Services</li>
                    <li>2</li>
                    <li class="text-price font-weight-bold">
                      IDR6,000,000 (exclude Jurnal account)
                    </li>
                  </ul></v-col
                >
                <v-col cols="3" class="border-left">
                  <div class="title">
                    <h5>Package 3</h5>
                    <h3>Advisory / Chief Services</h3>
                  </div>
                  <ul>
                    <li>Free</li>
                    <li>-</li>
                    <li>-</li>
                    <li>-</li>
                    <li>
                      <img src="/bcheck4.png" alt="" class="d-block mx-auto" />
                    </li>
                    <li>
                      <img src="/bcheck4.png" alt="" class="d-block mx-auto" />
                    </li>
                    <li>-</li>
                    <li>1</li>
                    <li class="text-price font-weight-bold">
                      IDR1,500,000/slot or IDR5,000,000/month
                    </li>
                  </ul></v-col
                >
              </v-row>
            </div>
          </v-col>
          <v-col v-if="$route.params.id === 'human-resources'" cols="12">
            <v-row>
              <v-col cols="9">
                <div class="price-wrap">
                  <v-row>
                    <v-col cols="4">
                      <div class="title no-border"></div>
                      <ul class="scope">
                        <li>Employee Administration</li>
                        <li>Employee Management</li>
                        <li>Organization Development</li>
                        <li class="text-price font-weight-bold">Pricing</li>
                      </ul>
                    </v-col>
                    <v-col cols="4" class="border-left">
                      <div class="title">
                        <h5>Package 1</h5>
                        <h3>(up to 15 employees)</h3>
                      </div>
                      <ul>
                        <li>Rp200,000/employee</li>
                        <li>Rp200,000/employee</li>
                        <li>Rp2,500,000/month</li>
                        <li class="text-price font-weight-bold">
                          Bundling Package : IDR300,000/pax
                          <em>(exclude Organization Development)</em>
                        </li>
                      </ul></v-col
                    >
                    <v-col cols="4" class="border-left">
                      <div class="title">
                        <h5>Package 2</h5>
                        <h3>(up to 30 employees)</h3>
                      </div>
                      <ul>
                        <li>Rp200,000/employee</li>
                        <li>Rp200,000/employee</li>
                        <li>Rp4,000,000/month</li>
                        <li class="text-price font-weight-bold">
                          Bundling Package : IDR300,000/pax
                          <em>(exclude Organization Development)</em>
                        </li>
                      </ul></v-col
                    >
                  </v-row>
                </div></v-col
              >
              <v-col cols="3">
                <div class="price-wrap solo">
                  <div class="title">
                    <h3>Recruitment</h3>
                  </div>
                  <ul>
                    <li>Sourcing, Interview, Administration</li>
                    <li>Paid after onboarding</li>
                    <li>No guarantee</li>
                    <li>Apply only for Retainer Package subscriber</li>
                    <li class="text-price font-weight-bold">
                      Fee : 25% of monthly salary
                    </li>
                  </ul>
                </div>
              </v-col>
            </v-row> </v-col
          ><v-col
            v-if="$route.params.id === 'fundraising-preparation'"
            cols="12"
          >
            <div class="price-wrap">
              <v-row>
                <v-col cols="3">
                  <div class="title no-border"></div>
                  <ul>
                    <li>First Consultation</li>
                    <li>Strategic Advisory</li>
                    <li>Data Room Building</li>
                    <li>Due Diligence Preparation</li>
                    <li>Compliance</li>
                    <li>Investor Relations</li>
                    <li>Legal Assistance</li>
                    <li>Dedicated Team</li>
                    <li class="text-price font-weight-bold">Pricing</li>
                  </ul>
                </v-col>
                <v-col cols="3" class="border-left">
                  <div class="title">
                    <h5>Package 1</h5>
                    <h3>Fundraising Strategy</h3>
                  </div>
                  <ul>
                    <li>Free</li>
                    <li>
                      <img src="/bcheck5.png" alt="" class="d-block mx-auto" />
                    </li>
                    <li>-</li>
                    <li>-</li>
                    <li>-</li>
                    <li>-</li>
                    <li>By request</li>
                    <li>-</li>
                    <li class="text-price font-weight-bold">
                      IDR3,500,000/session
                    </li>
                  </ul></v-col
                >
                <v-col cols="3" class="border-left">
                  <div class="title">
                    <h5>Package 2</h5>
                    <h3>Entry Package</h3>
                  </div>
                  <ul>
                    <li>Free</li>
                    <li>
                      <img src="/bcheck5.png" alt="" class="d-block mx-auto" />
                    </li>
                    <li>
                      <img src="/bcheck5.png" alt="" class="d-block mx-auto" />
                    </li>
                    <li>
                      <img src="/bcheck5.png" alt="" class="d-block mx-auto" />
                    </li>
                    <li>
                      <img src="/bcheck5.png" alt="" class="d-block mx-auto" />
                    </li>
                    <li>-</li>
                    <li>By request</li>
                    <li>1</li>
                    <li class="text-price font-weight-bold">
                      IDR15,000,000/month
                    </li>
                  </ul></v-col
                >
                <v-col cols="3" class="border-left">
                  <div class="title">
                    <h5>Package 3</h5>
                    <h3>Advisory / Chief Services</h3>
                  </div>
                  <ul>
                    <li>Free</li>
                    <li>
                      <img src="/bcheck5.png" alt="" class="d-block mx-auto" />
                    </li>
                    <li>
                      <img src="/bcheck5.png" alt="" class="d-block mx-auto" />
                    </li>
                    <li>
                      <img src="/bcheck5.png" alt="" class="d-block mx-auto" />
                    </li>
                    <li>
                      <img src="/bcheck5.png" alt="" class="d-block mx-auto" />
                    </li>
                    <li>
                      <img src="/bcheck5.png" alt="" class="d-block mx-auto" />
                    </li>
                    <li>By request</li>
                    <li>2</li>
                    <li class="text-price font-weight-bold">
                      IDR30,000,000/month + 1% closing fee
                    </li>
                  </ul></v-col
                >
              </v-row>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <div class="contact-new">
      <v-container>
        <v-row>
          <v-col md="5">
            <h3>Ready to take your business to another level?</h3>
            <a href="http://wa.link/pmub9a" target="_blank"
              ><img src="/wa.png" alt="" /> Consult Now</a
            >
          </v-col>
        </v-row>
        <div
          class="image-wrap"
          :style="{ backgroundImage: `url(${bgConsult})` }"
        ></div>
      </v-container>
    </div>
    <div class="other-service">
      <v-container>
        <v-row>
          <v-col cols="10" offset="1">
            <h2 class="title-service text-center">
              Explore Our Other Services
            </h2>
            <a href="/service/finance"
              ><img src="/ft.png" alt="" /> Financal & Tax</a
            >
            <a href="/service/content-design"
              ><img src="/cd.png" alt="" /> Content & Design</a
            >
            <a href="/service/human-resources"
              ><img src="/hr.png" alt="" /> Human Resources</a
            >
            <a href="/service/impact-management"
              ><img src="/im.png" alt="" /> Impact Management</a
            >
            <a href="/service/fundraising-preparation"
              ><img src="/fp.png" alt="" /> Fundraising Preparation</a
            >
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<script>
import VueMarkdown from 'vue-markdown'

export default {
  components: {
    VueMarkdown,
  },
  layout: 'new',
  data() {
    return {
      title: '',
      slogan: '',
      p1: '',
      p2: '',
      bTitle: '',
      bItem: [],
      activeBusiness: 0,
      index: 0,
      services: [],
      suTitle: '',
      suItem: [],
      bgLanding: '',
      bgConsult: '',
      bgWhy: '',
    }
  },
  head() {
    return {
      title: 'Kolaborasi.co | Service',
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
          content: 'Kolaborasi.co | Service',
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
      if (this.index < 2) {
        this.index++
        this.setActive(this.index)
      } else {
        this.index = 0
        this.setActive(this.index)
      }
    }, 4000)
    if (this.$route.params.id === 'impact-management') {
      this.title = 'Impact Management'
      this.slogan = 'Plan, Manage, and Measure your Social Impact'
      this.p1 =
        "We`re here to empower you to create lasting and meaningful change in their communities and beyond. With our help, you'll be able to measure the outcomes and impact of your programs, make data-driven decisions, and communicate your impact effectively to stakeholders. "
      this.bTitle = 'Why it’s better with us'
      this.bItem = [
        {
          title: 'Design your business to be impactful',
          desc: 'We work closely with you to understand their values, goals, and impact, and then develop customized plans to help you achieve their desired outcomes in making positive impact in the communities and beyond.',
        },
        {
          title: 'Ease the process of impact measurement',
          desc: "Our tools and methodologies are designed to streamline the impact measurement process, so you can be confident that you're getting accurate and reliable data to inform your decision-making.",
        },
        {
          title: 'Share & publish the impact created',
          desc: "With our help, you'll be able to communicate your impact in a clear and accessible way to stakeholders, customers, and investors with confidence, building trust and credibility in your organization.",
        },
      ]
      this.services = [
        {
          title: 'Impact Planning',
          list: '<ul><li>Developing Impact Framework</li><li>Impact Metrics</li><li>Activity / program advisory</li></ul>',
        },
        {
          title: 'Data Collection',
          list: '<ul><li>Measurement Activity Planning</li><li>Data Collection Tools</li><li>Surveyor Training</li></ul>',
        },
        {
          title: 'Impact Reporting',
          list: '<ul><li>Data Cleansing & Processing</li><li>Data Visualization</li><li>Impact Reporting</li></ul>',
        },
      ]
      this.suTitle = 'Benefit of outsourcing with us'
      this.suItem = [
        {
          img: '/Impact-Management-Value-for-money-Attribute-Elzicon.png',
          title: 'Value for Money',
          subtitle:
            'Pay with the budget of fresh graduates, but get a team with 10+ years experiences in handling startup. ',
        },
        {
          img: '/Impact-Management-Reliable-Attribute-Freepik.png',
          title: 'Reliable ',
          subtitle:
            'No sick days, no paid leaves, no bad-mood day.  Our worker consist of a professional team, that will always ready on duty to deliver high quality work.',
        },
        {
          img: '/Impact-Management-Flexible-Attribute-Freepik.png',
          title: 'Flexible ',
          subtitle:
            'When the workload increase, you don’t have to hire new person! Just top up your subscription package and get more done. Vica versa, when the workload decrease, you can shift back to cheaper package',
        },
      ]
      this.bgConsult = '/Consult-Now-Impact.png'
      this.bgLanding = '/Impact-Management-Service-Landing-Page.png'
      this.bgWhy = '/Impact-Management-Why-its-better-with-us.png'
    } else if (this.$route.params.id === 'finance') {
      this.title = 'Financal & Tax'
      this.slogan = 'Track your number accurately, make decision effectively'
      this.p1 =
        '“Cash is king” so they said. So understanding how financial works in your business is far more important than it seems. We will help to ensure that every single of your business decisions has the best impact on your business’ financial condition and ultimately generate more profit for you. '
      this.bTitle = 'Why it’s better with us'
      this.bItem = [
        {
          title: 'Effortlessly track & manage your cash flow',
          desc: 'With our in-house team, you’ll able to track your revenue & expenses easily, so you can always know your cash position and make business decisions accordingly. ',
        },
        {
          title: 'Improve your cost efficiency',
          desc: 'We will consult strategically so you can increase efficiency, cut cost, and make sure you have enough margin to sustain your operational. ',
        },
        {
          title: 'Plan your business expansion profitably',
          desc: 'We will help you make a financial forecast & budgeting for your business expansion. So you’ll know how to grow your business profitably.',
        },
      ]
      this.services = [
        {
          title: 'Bookkeeping & Transaction',
          list: '<ul><li>Recap & Report</li><li>All Banking Transaction <em>(payment, payroll)</em></li></ul>',
        },
        {
          title: 'Strategic Financial Advisory',
          list: '<ul><li>Financial forecast</li><li>Project Budgeting</li><li>Cashflow Management</li></ul>',
        },
        {
          title: 'Secretarial & Administrative',
          list: '<ul><li>Quotation & Invoicing</li><li>Commercial Contract</li></ul>',
        },
        {
          title: 'Tax handling & compliance',
          list: '<ul><li>Tax Setup & Management</li><li>Tax Filing</li><li>Tax Payment & Report</li></ul>',
        },
      ]
      this.suTitle = 'Benefit of outsourcing with us'
      this.suItem = [
        {
          img: '/Finance-Value-for-money-Attribute-Dinosoft.png',
          title: 'Value for Money',
          subtitle:
            'Pay with the budget of fresh graduates, but get a team with 10+ years experiences in handling startup. ',
        },
        {
          img: '/Finance-Reliable-Attribute-Freepik.png',
          title: 'Reliable ',
          subtitle:
            'No sick days, no paid leaves, no bad-mood day.  Our worker consist of a professional team, that will always ready on duty to deliver high quality work.',
        },
        {
          img: '/Finance-Flexible-Freepik.png',
          title: 'Flexible ',
          subtitle:
            'When the workload increase, you don’t have to hire new person! Just top up your subscription package and get more done. Vica versa, when the workload decrease, you can shift back to cheaper package',
        },
      ]
      this.bgConsult = '/Consult-Now-Finance.png'
      this.bgLanding = '/Finance-Service-Landing.png'
      this.bgWhy = '/Finance-Why-its-better-with-us.png'
    } else if (this.$route.params.id === 'content-design') {
      this.title = 'Content & Design'
      this.slogan =
        'Produce content & design material to achieve your campaign objectives'
      this.p1 =
        "We understand that your campaign objectives are unique and require a tailored approach to achieve success. That's why we offer a range of services to help you meet your goals. Our team of experts will work closely with you to understand your target audience, brand identity, and marketing objectives to ensure that we deliver the perfect solution for your campaign."
      this.bTitle = 'Why it’s better with us'
      this.bItem = [
        {
          title: 'Transform your vision into reality',
          desc: 'With years of experience in content creation & design, we have the skills, tools, and creativity needed to take your ideas and bring them to life.',
        },
        {
          title: 'Elevate your brand to new heights',
          desc: 'Our team will create high quality, engaging content, and design that speaks directly to your target audience, helping to increase brand awareness, and drive conversions.',
        },
        {
          title: 'Holistic and collaborative approach',
          desc: ' We take the time to get to know your business and your unique needs, and we involve you in every step of the process, from initial planning to final execution.',
        },
      ]
      this.services = [
        {
          title: 'Branding',
          list: '<ul><li>Logo</li><li>Brand book</li><li>Marketing Design</li><li>Graphic Assets</li></ul>',
        },
        {
          title: 'Report & Presentation Design',
          list: '<ul><li>Page Design</li><li>Business Copywriting</li><li>Infographic</li><li>Graphic Assets</li></ul>',
        },
        {
          title: 'Socmed Content',
          list: '<ul><li>Social Media Images <em>(feed, story, poster, ad banner)</em> </li><li>Copywriting <em>(caption, poster copy)</em></li><li>Content Guideline </li></ul>',
        },
      ]
      this.suTitle = 'Benefit of outsourcing with us'
      this.suItem = [
        {
          img: '/Content-Value-for-money-Attribute-Dinosoft.png',
          title: 'Value for Money',
          subtitle:
            'Pay with the budget of fresh graduates, but get a team with 10+ years experiences in handling startup. ',
        },
        {
          img: '/Content-Reliable-Attribute-Flaticons.png',
          title: 'Reliable ',
          subtitle:
            'No sick days, no paid leaves, no bad-mood day.  Our worker consist of a professional team, that will always ready on duty to deliver high quality work.',
        },
        {
          img: '/Content-Flexible-Monkik.png',
          title: 'Flexible ',
          subtitle:
            'When the workload increase, you don’t have to hire new person! Just top up your subscription package and get more done. Vica versa, when the workload decrease, you can shift back to cheaper package',
        },
      ]
      this.bgConsult = '/Consult-Now-Content_Design.png'
      this.bgLanding = '/Content-Service-Landing.png'
      this.bgWhy = '/Content-Why-its- better-with-us.png'
    } else if (this.$route.params.id === 'human-resources') {
      this.title = 'Human Resources'
      this.slogan =
        'Strengthen the human-side of your business as a foundation to grow'
      this.p1 =
        'Strong organisation is a foundation of business growth, yet nurturing them is often overlooked by the founders. With us, you’ll get a partner to handle all your human resources activities for your business. From developing the people & organisation, to setting up the right & productive work culture.'
      this.bTitle = 'Why it’s better with us'
      this.bItem = [
        {
          title: 'Get your administrative in order',
          desc: 'From employee contract, to setting the right internal policy, we will create a the employee administrative system suit to your organisation',
        },
        {
          title: 'Develop & nurture your team',
          desc: 'Increase the retention rate of your employees by catering their individual growth and nurturing the right culture & relationship. ',
        },
        {
          title: 'Manage & push the performance',
          desc: 'Know what to achieve & how to measure each individual KPI. Then find a way to push their productivity systematically.',
        },
      ]
      this.services = [
        {
          title: 'Employee Administration',
          list: '<ul><li>Employee Pay Structure</li><li>Benefit & Compensation <em>(Bonus, Commission, Leave, Sick Leave, Maternity Leave, Resign, Promotion)</em></li><li>Employment Administrative Document <em>(Offer Letter, Employee Contract, Warning Letter, Recommendation Letter, Paklaring)</em></li></ul>',
        },
        {
          title: 'Employee Management',
          list: '<ul><li>Performance Management <em>(Review, Appraisal, Promotion, Termination, Rotation, etc.) </em></li><li>KPI Setting <em>(Review, Target, Creating, Monitor)</em></li><li>Employee Engagement Design <em>(Measure employee NPS, Design a “tailor made” program)</em></li></ul>',
        },
        {
          title: 'Organization Development',
          list: '<ul><li>Overall HR related Internal Policy</li><li>Workflow Management <em>(i.e. SOP)</em></li><li>Conflict Resolution <em>(mediation, relationship, etc.)</em> </li><li>Company Culture</li><li>Other Strategic solution</li></ul>',
        },
      ]
      this.suTitle = 'Benefit of outsourcing with us'
      this.suItem = [
        {
          img: '/HR-Value-for-Money-Attribute-Iconixar.png',
          title: 'Value for Money',
          subtitle:
            'Pay with the budget of fresh graduates, but get a team with 10+ years experiences in handling startup. ',
        },
        {
          img: '/HR-Reliable-Attribute-Juicy_Fish.png',
          title: 'Reliable ',
          subtitle:
            'No sick days, no paid leaves, no bad-mood day.  Our worker consist of a professional team, that will always ready on duty to deliver high quality work.',
        },
        {
          img: '/HR-Flexible-Freepik.png',
          title: 'Flexible ',
          subtitle:
            'When the workload increase, you don’t have to hire new person! Just top up your subscription package and get more done. Vica versa, when the workload decrease, you can shift back to cheaper package',
        },
      ]
      this.bgConsult = '/Consult-Now-HR.png'
      this.bgLanding = '/HR-Service-Landing.png'
      this.bgWhy = '/HR-Why-its-better-with-us.png'
    } else if (this.$route.params.id === 'fundraising-preparation') {
      this.title = 'Fundraising Preparation'
      this.slogan = 'Cos fundraising goes beyond pitching.'
      this.p1 =
        'Many founder think too much on fundraising while also depending too much on it. With our guidance & assistance, we will assist you first hand on your fundraising journey from planning, strategizing, pitching, to dealing. All with our combined experiences as a founder and an investor.'
      this.bTitle = 'Why it’s better with us'
      this.bItem = [
        {
          title: 'Strategize your fundraising smartly',
          desc: 'We will help you plan your fundraising well. From introduction on who to talk to, what narration to build, and how to talk to each different investors. ',
        },
        {
          title: 'Build your connection strategically',
          desc: 'As our experience in fundraising ourselves, we will assist you with the best practice in communication & interaction with investor to earn their trust. ',
        },
        {
          title: 'Get the paperwork done professionally',
          desc: 'We will prepare you & your business all the documents & nitty gritty your investor gonna ask, even months before your first pitch to them.',
        },
      ]
      this.services = [
        {
          title: 'Fundraising Strategy',
          list: '<ul><li>Fundraising Plan & Best Practice</li><li>Strategic Advisory </li></ul>',
        },
        {
          title: 'Due Diligence Preparation',
          list: '<ul><li>Information Request List</li><li>Assist on Financial & Commercial Due Diligence</li></ul>',
        },
        {
          title: 'Investor Relations',
          list: '<ul><li>Pitching Assistance</li><li>Handling Investor’s Matters </li></ul>',
        },
        {
          title: 'Compliance',
          list: '<ul><li>Handling paperwork progress & status</li><li>Follow & Adjust on local and international regulatory</li></ul>',
        },
        {
          title: 'Legal Assistance',
          list: '<ul><li>Company Legal Structure </li><li>Legal Advisory</li><li>Assist on Legal Due Diligence Requests</li></ul>',
        },
      ]
      this.suTitle = 'Benefit of outsourcing with us'
      this.suItem = [
        {
          img: '/Fundraising-Value-for-money-Attribute-Kiranshasty.png',
          title: 'Value for Money',
          subtitle:
            'Pay with the budget of fresh graduates, but get a team with 10+ years experiences in handling startup. ',
        },
        {
          img: '/Fundraising-Reliable-Attribute-Parzival.png',
          title: 'Reliable ',
          subtitle:
            'No sick days, no paid leaves, no bad-mood day.  Our worker consist of a professional team, that will always ready on duty to deliver high quality work.',
        },
        {
          img: '/Fundraising-Flexible-Attribute-Juicy_Fish.png',
          title: 'Flexible ',
          subtitle:
            'When the workload increase, you don’t have to hire new person! Just top up your subscription package and get more done. Vica versa, when the workload decrease, you can shift back to cheaper package',
        },
      ]
      this.bgConsult = '/Consult-Fundraising.png'
      this.bgLanding = '/Fundraising-Service-Landing.png'
      this.bgWhy = '/Fundraising-Why-its-better-with-us.png'
    }
  },
  methods: {
    setActive(val) {
      this.index = val
    },
  },
}
</script>
