<template>
  <div>
    <div class="portfolio-head-new">
      <v-container>
        <v-row>
          <v-col cols="12" md="10" offset-md="1">
            <div class="breadcrumb-new">
              <span class="circle"></span> Venture Builder Portfolio
            </div>
            <h2>We invest in people who change the way the world works.</h2>
          </v-col>
        </v-row>
      </v-container>
      <v-container class="mb-10">
        <v-row>
          <v-col cols="12" md="10" offset-md="1">
            <div class="item-new-portfolio">
              <img class="logo" src="/p2.png" alt="" />
              <h3>Yohanes Sugihtononugroho</h3>
              <h5>Cofounder & CEO of Crowde.co</h5>
              <p>
                Yohanes “Oyong” believes that farmers wellbeing are the
                leftovers of economic development. He envision a future where
                empowered farmer become a signiﬁcant player in the industry by
                equipping them with access to funding, technology &
                entrepreneurial skills
              </p>

              <a
                href="javascript:void(0);"
                class="btn-circle"
                @click="showDialog('yohanes')"
                >learn more</a
              >
              <div
                class="image-wrap"
                style="background-image: url('/people9.png')"
              ></div>
            </div>
          </v-col>
          <v-col cols="12" md="10" offset-md="1">
            <div class="item-new-portfolio second reverse">
              <img class="logo" src="/p1.png" alt="" />
              <h3>Rhaka Ghanisatria, Adam Abednego & Levina Purnamadewi</h3>
              <h5>Cofounder at Menjadi Manusia</h5>
              <p>
                Rhaka is able to convert his trauma of addiction and dropping
                out of college into a positive energy to move forward. So he
                understands at college into a positive energy to move forward.
                So he understands at heart, that business is not only about
                money, but more a meaningful and fulﬁlling way of living while
                helping other people to become a better person
              </p>

              <a
                href="javascript:void(0);"
                class="btn-circle"
                @click="showDialog('rhaka')"
                >learn more</a
              >
              <div
                class="image-wrap yellowed"
                style="background-image: url('/people12.png')"
              ></div>
            </div>
          </v-col>
          <v-col cols="12" md="10" offset-md="1">
            <div class="item-new-portfolio four">
              <img class="logo" src="/p4.png" alt="" />
              <h3>Kukuh Rizal, Ray Mahendra & Baskara Putra</h3>
              <h5>Cofounders of Sun Eater</h5>
              <p>
                As co-founders, Kukuh, Ray, and Baskara spearhead a revolution
                in the music and entertainment industry, championing Indonesia's
                future talents. Since its inception in 2019, Sun Eater has
                emerged as a pioneering force in Indonesia's music and
                entertainment landscape. With a keen focus on nurturing future
                talents, they've seamlessly blended technology and storytelling,
                captivating audiences and propelling their artists to the
                forefront.
              </p>

              <a
                href="javascript:void(0);"
                class="btn-circle"
                @click="showDialog('suneater')"
                >learn more</a
              >
              <div
                class="image-wrap reded"
                style="background-image: url('')"
              ></div>
            </div>
          </v-col>
          <v-col cols="12" md="10" offset-md="1">
            <div class="item-new-portfolio third reverse">
              <img class="logo" src="/p12.png" alt="" />
              <h3>Miftachurrabbani & Chashif Syadzali</h3>
              <h5>Cofounders of LindungiHutan</h5>
              <p>
                Ben and Chacip initial dream is to plant the trees with the same
                amount of Indonesian population. Then they develop a mission to
                corporations and communities with reforestation initiatives to
                help solve the world most depressing challenge : global warming.
              </p>

              <a
                href="javascript:void(0);"
                class="btn-circle"
                @click="showDialog('lindungihutan')"
                >learn more</a
              >
              <div
                class="image-wrap greened"
                style="background-image: url('')"
              ></div>
            </div>
          </v-col>
          <v-col cols="12" md="10" offset-md="1">
            <div class="item-new-portfolio">
              <img class="logo" src="/p3.png" alt="" />
              <h3>Wendy Pratama</h3>
              <h5>Cofounder & CEO of Lingkaran.co</h5>
              <p>
                As an architecture graduate, he built his company like he built
                his home. Started by building his team, as the foundation. He
                built a family where people can have fun, pursue their passion,
                do things that they want to, while achieving the common goals of
                providing an alternative education program for people to upgrade
                their life & career.
              </p>

              <a
                href="javascript:void(0);"
                class="btn-circle"
                @click="showDialog('wendy')"
                >learn more</a
              >
              <div
                class="image-wrap"
                style="background-image: url('/people10.png')"
              ></div>
            </div>
          </v-col>
          <v-col cols="12" md="10" offset-md="1">
            <div class="item-new-portfolio second reverse">
              <img class="logo" src="/p6.png" alt="" />
              <h3>Ivan Lalamentik</h3>
              <h5>Cofounder & CEO of Lexar.id</h5>
              <p>
                As a lawyer, Ivan understands the legal industry is full of
                intrigue yet strictly regulated. but with his entrepreneurial
                point of view he found new business opportunities and swiftly
                pioneered a solution to the problem faced by the emerging market
                of legal services.
              </p>

              <a
                href="javascript:void(0);"
                class="btn-circle"
                @click="showDialog('ivan')"
                >learn more</a
              >
              <div
                class="image-wrap yellowed"
                style="background-image: url('/people5.png')"
              ></div>
            </div>
          </v-col>
          <v-col cols="12" md="10" offset-md="1">
            <div class="item-new-portfolio four">
              <img class="logo" src="/p5.png" alt="" />
              <h3>Rizky Fadhilah</h3>
              <h5>Cofounder & CEO of Cityplan Indonesia</h5>
              <p>
                Rizky sees opportunity amidst the chaotic nature of city
                development. Equipped with his engineering skill in urban
                planning, he creates solutions & new business ecosystems to help
                government & business plan the city better with technology.
              </p>

              <a
                href="javascript:void(0);"
                class="btn-circle"
                @click="showDialog('rizky')"
                >learn more</a
              >
              <div
                class="image-wrap reded"
                style="background-image: url('/people6.png')"
              ></div>
            </div>
          </v-col>
          <v-col cols="12" md="10" offset-md="1">
            <div class="item-new-portfolio third reverse">
              <img class="logo" src="/p10.png" alt="" />
              <h3>Firman Alimuddin</h3>
              <h5>Cofounder & CEO of Robonesia & Latihhobi.id</h5>
              <p>
                Firman is a resilient and resourceful educator/technocrat. He is
                able to withstand the ups and downs of Robonesia and able to ﬁll
                multiple strategic roles to grow Robonesia. His ability to
                nimbly overcome many challenges further proves his spirit and
                versatility.
              </p>

              <a
                href="javascript:void(0);"
                class="btn-circle"
                @click="showDialog('firman')"
                >learn more</a
              >
              <div
                class="image-wrap greened"
                style="background-image: url('/people8.png')"
              ></div>
            </div>
          </v-col>
          <v-col cols="12" md="10" offset-md="1">
            <div class="item-new-portfolio">
              <img class="logo" src="/p9.png" alt="" />
              <h3>Mayumi Haryoto & Aisha Habir</h3>
              <h5>Cofounders of Bacapibo.com</h5>
              <p>
                Mayumi and Aisha, with their experience in creative design and
                art management, have a mission to nurture the love for reading
                in Indonesian children. As seasoned illustrators and designers
                with passion for children’s literature, they pioneered the first
                subscription-based digital library for children in Indonesia,
                providing access to high-quality educational content to inspire
                young readers.
              </p>

              <a
                href="javascript:void(0);"
                class="btn-circle"
                @click="showDialog('mayumi')"
                >learn more</a
              >
              <div
                class="image-wrap"
                style="background-image: url('/people11.png')"
              ></div>
            </div>
          </v-col>
          <v-col cols="12" md="10" offset-md="1">
            <div class="item-new-portfolio second reverse">
              <img class="logo" src="/p11.png" alt="" />
              <h3>Ade Nurul Safrina</h3>
              <h5>Cofounder & Strategic Director of BerdayaKrui</h5>
              <p>
                With experience in social enterprise, knowledge about economic
                development, and ability as a ﬂuent public speaker. She is able
                to persuade and move stakeholders from government, private
                investors, to local business owners and give back to the village
                by co-establishing a social enterprise locally owned by the
                village community.
              </p>

              <a
                href="javascript:void(0);"
                class="btn-circle"
                @click="showDialog('nuwi')"
                >learn more</a
              >
              <div
                class="image-wrap yellowed"
                style="background-image: url('/people7.png')"
              ></div>
            </div>
          </v-col>
          <v-col cols="12" md="10" offset-md="1">
            <div class="item-new-portfolio four">
              <img class="logo" src="/p7.png" alt="" />
              <h3>Rizki NH Penna</h3>
              <h5>Founder & CEO of TennisKuy</h5>
              <p>
                With a background in social enterprise and a deep understanding
                of economic development, Rizki leverages his expertise to
                cultivate a vibrant and inclusive tennis experience community. A
                persuasive and articulate public speaker, he engages
                stakeholders ranging from government officials to local business
                owners, fostering collaboration and driving community growth.
              </p>

              <a
                href="javascript:void(0);"
                class="btn-circle"
                @click="showDialog('tennis')"
                >learn more</a
              >
              <div
                class="image-wrap reded"
                style="background-image: url('')"
              ></div>
            </div>
          </v-col>
        </v-row>
      </v-container>
      <v-container>
        <v-row>
          <v-col cols="12" md="10" offset-md="1">
            <div class="breadcrumb-new mt-10">
              <span class="circle"></span> Joint Venture Portfolios
            </div>
            <h2>Lorem Ipsum</h2>
          </v-col>
        </v-row>
      </v-container>
      <v-container>
        <v-row>
          <v-col cols="12" md="10" offset-md="1">
            <div class="item-new-portfolio mt-3">
              <img class="logo" src="/p13.png" alt="" />
              <h3>SocialInnovation.id</h3>
              <p class="pr-0">
                Social Innovation Acceleration Program (SIAP) is a learning
                platform & program provider for early stage social enterprises.
                We create incubation, acceleration, and bootcamp to support the
                establishment & development of social entrepreneurship in
                Indonesia. Working with many prominent entity such as UNDP, GoTo
                Foundation, DBS Bank, GIZ, British Council, etc we have
                established more than 30 program supporting more than 500 social
                entrepreneurs across Indonesia
              </p>
            </div>
          </v-col>
          <v-col cols="12" md="10" offset-md="1">
            <div class="item-new-portfolio second">
              <img class="logo" src="/p8.png" alt="" />
              <h3>Brocode Barber</h3>
              <p class="pr-0">
                BrocodeBarber is a barbershop that cater the needs of man’s
                grooming experiences. Established in 2014, currently we have 8
                branches in several cities across Indonesia, serving more than
                1000 customer every month. We also launch a series of self-brand
                grooming product to provide the best hair treatment for men.
              </p>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <v-dialog v-model="dialog" width="900" content-class="modal-portfolio">
      <v-card>
        <a href="javascript:void(0);" class="close" @click="dialog = false"
          ><img src="/cancel.png" alt=""
        /></a>
        <v-row>
          <v-col cols="12" sm="4">
            <span>Company</span>
            <img class="d-block" :src="modalLogo" alt="" />
          </v-col>
          <v-col cols="12" sm="4"
            ><span>Name & Title</span>

            <h3>{{ modalName }}</h3>
            <h5 class="mb-0">{{ modalTitle }}</h5></v-col
          >
          <v-col cols="12" sm="4"
            ><span>Social</span>

            <a
              v-if="modalLinkedin !== ''"
              :href="modalLinkedin"
              target="_blank"
              class="socmed mr-2"
            >
              <v-icon> fab fa-linkedin </v-icon>
            </a>
            <a
              v-if="modalIg !== ''"
              :href="modalIg"
              target="_blank"
              class="socmed mr-2"
            >
              <v-icon> fab fa-instagram </v-icon>
            </a>
            <a
              v-if="modalWeblink !== ''"
              :href="modalWeblink"
              target="_blank"
              class="socmed"
            >
              <v-icon> fas fa-link </v-icon>
            </a>
          </v-col>
          <v-col cols="12" sm="8"
            ><span>About</span>
            <p>
              {{ modalAbout }}
            </p></v-col
          >
          <v-col cols="12" sm="4">
            <div
              class="image-wrap"
              :style="{ backgroundImage: `url(${modalPhoto})` }"
            ></div
          ></v-col>
        </v-row>
      </v-card>
    </v-dialog>
  </div>
</template>

<script>
export default {
  layout: 'new',
  data() {
    return {
      dialog: false,
      modalLogo: '',
      modalName: '',
      modalTitle: '',
      modalAbout: '',
      modalPhoto: '',
      modalLinkedin: '',
      modalIg: '',
      modalWeblink: '',
    }
  },
  head() {
    return {
      title: 'Kolaborasi.co | Portfolio',
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
          content: 'Kolaborasi.co | Portfolio',
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
    showDialog(val) {
      if (val === 'yohanes') {
        this.modalLogo = '/p2.png'
        this.modalName = 'Yohanes Sugihtononugroho'
        this.modalTitle = 'Cofounder & CEO of Crowde.co'
        this.modalAbout =
          "Crowde is an agriculture technology startup aiming to increase farmer's welfare by empowering farmers with technology, creating an efficient agriculture ecosystem, and being the trusted crowd-investment platform. In the past years Crowde has supported >70.000 farmers, operating in >9 provinces across Indonesia with multiple digital products. Crowde founder has been awarded Forbes 30 under 30 Asia, Social Entrepreneur category in 2018."
        this.modalPhoto = '/people9.png'
        this.modalWeblink = 'https://crowde.co/'
        this.modalIg = 'https://www.instagram.com/temancrowde/'
        this.modalLinkedin =
          'https://www.linkedin.com/company/crowdeco/mycompany/'
      } else if (val === 'rizky') {
        this.modalLogo = '/p5.png'
        this.modalName = 'Rizky Fadhilah'
        this.modalTitle = 'Cofounder & CEO of Cityplan Indonesia'
        this.modalAbout =
          'Cityplan is a location intelligence management software as a service that helps businesses & government to collect, visualise, manage, and analyze their spatial data. We enable the use of +60 city zoning for building permits, monitoring, and public transparency for business decision making. With multiple use case including store / branch expansion, route optimization, real estate planning and asset management. '
        this.modalPhoto = '/people6.png'
        this.modalWeblink = 'https://cityplan.id/'
        this.modalIg = 'https://www.instagram.com/cityplan.id/'
        this.modalLinkedin =
          'https://www.linkedin.com/company/cityplanindonesia/'
      } else if (val === 'ivan') {
        this.modalLogo = '/p6.png'
        this.modalName = 'Ivan Lalamentik'
        this.modalTitle = 'Cofounder & CEO of Lexar.id'
        this.modalAbout =
          'Lexar is a legal & corporate secretarial services partner for early stage business. We reduce layers of bureaucracy commonly happen in legal company and focus on optimizing customer experiences in achieving their objectives. Our services include Incorporation, Legal Due Diligence (LDD) for fundraising, Licensing, Tax Management, Virtual Office, and in-house legal outsourcing.'
        this.modalPhoto = '/people5.png'
        this.modalWeblink = 'https://lexar.id/'
        this.modalIg = 'https://www.instagram.com/lexar.id/'
        this.modalLinkedin =
          'https://www.linkedin.com/company/lexar-id/mycompany/'
      } else if (val === 'wendy') {
        this.modalLogo = '/p3.png'
        this.modalName = 'Wendy Pratama'
        this.modalTitle = 'Cofounder & CEO of Lingkaran.co'
        this.modalAbout =
          'Lingkaran is a leading creative education platform in Indonesia. They provide soft skill & hard skill development programs and in-demand skills training for those seeking relevance in today’s fast-changing industry. Lingkaran also collaborate with many corporation to develop and run variety of courses, graduating >50.000 program alumnis from >2000 classes created'
        this.modalPhoto = '/people10.png'
        this.modalWeblink = 'https://lingkaran.co/'
        this.modalIg = 'https://www.instagram.com/lingkaran.co/'
        this.modalLinkedin =
          'https://www.linkedin.com/school/lingkaran/mycompany/'
      } else if (val === 'rhaka') {
        this.modalLogo = '/p1.png'
        this.modalName = 'Rhaka'
        this.modalTitle =
          'Rhaka Ghanisatria, Adam Abednego & Levina Purnamadewi'
        this.modalAbout =
          "Menjadi Manusia is Indonesia's leading media platform for youth focusing on life stories & mental health issues. They produce high quality content in multiple channels including Instagram (1.1 million followers), YouTube (920.000 subscribers), Spotify, and TikTok. In the process has developed several new channels network including @Santoshadotid @seribukisahsebuahkasih & @menjaditemanmanusia. Menjadi Manusia also become a part of USS Network and get awarded as Youtube Creator for Change Ambassador in 2019"
        this.modalPhoto = '/people12.png'
        this.modalWeblink = 'https://www.youtube.com/@MenjadiManusia'
        this.modalIg = 'https://www.instagram.com/menjadimanusia.id/'
        this.modalLinkedin =
          'https://www.linkedin.com/company/menjadimanusia/mycompany/'
      } else if (val === 'firman') {
        this.modalLogo = '/p10.png'
        this.modalName = 'Firman Alimuddin'
        this.modalTitle = 'Cofounder & CEO of Robonesia & Latihhobi.id'
        this.modalAbout =
          'Robonesia is an extracurricular class provider for elementary students, specialise in robotic education. We aim to modernize the extracurricular education in schools while preparing students with technology education since early childhood. We’ve more than 10.000 students in more than 100 schools, focusing in West Java region. In the process, we also develop other extracurricular classes such as soccer, archery etc under the brand of LatihHobi.id'
        this.modalPhoto = '/people8.png'
        this.modalWeblink = 'https://robonesia.id/'
        this.modalIg = 'https://www.instagram.com/robonesia.id/'
        this.modalLinkedin =
          'https://www.linkedin.com/in/firman-alimuddin-69501a110/'
      } else if (val === 'nuwi') {
        this.modalLogo = '/p11.png'
        this.modalName = 'Ade Nurul Safrina'
        this.modalTitle = 'Cofounder & Strategic Director of BerdayaKrui'
        this.modalAbout =
          'BerdayaKrui is a social enterprise aim to develop responsible tourism with pilot project in Krui, Lampung provinces. Our initial establishment including Berdaya Homestay, a cottage co-owned and co-managed between Berdaya Krui Foundation and Municipal owned business entity. To enlarge our impact, we also collaborate with local stakeholder to run various program including Berdaya SME Development, Berdaya English Class, BerdayaKrui nurtures local tourism industry.'
        this.modalWeblink = 'https://berdaya.co/'
        this.modalIg = 'https://www.instagram.com/berdayakrui/'
        this.modalLinkedin = 'https://www.linkedin.com/in/safrina/'
        this.modalPhoto = '/people7.png'
      } else if (val === 'mayumi') {
        this.modalLogo = '/p9.png'
        this.modalName = 'Mayumi Haryoto & Aisha Habir'
        this.modalTitle = 'Cofounders of Bacapibo.com'
        this.modalAbout =
          'BacaPibo is an online library for pictured books for children 4-12 years old. We aim to solve Indonesia’s low reading interest since youth, by providing exciting educational stories & reading experience in our platform. We have partnered with more than 45 content partner and used by more than 10.000 students, by partnering with school & corporate to get access to the readers community. '
        this.modalPhoto = '/people11.png'
        this.modalWeblink = 'https://bacapibo.com/'
        this.modalIg = 'https://www.instagram.com/bacapibo/'
        this.modalLinkedin =
          'https://www.linkedin.com/in/mayumi-haryoto-945213190/'
      } else if (val === 'suneater') {
        this.modalLogo = '/p4.png'
        this.modalName = 'Kukuh Rizal, Ray Mahendra & Baskara Putra'
        this.modalTitle = 'Cofounders of Sun Eater '
        this.modalAbout =
          'Sun Eater is a hybrid music-entertainment company, aiming to bring Indonesia’s future talents forward. We develop & manage some of the top Indonesia independent artist including Hindia, LombaSihir, and .Feast. Our artist has garner collectively more than 2.7 millions followers on Instagram,  10 millions monthly listener on spotify, 350 millions total views on YouTube. We create a storytelling content with a fan-focused approach to build deep relevance of artists, and technology to muster an exponential growth. '
        this.modalPhoto = ''
        this.modalWeblink = 'https://suneatercoven.com/'
        this.modalIg = 'https://www.instagram.com/suneatercoven/'
        this.modalLinkedin =
          'https://www.linkedin.com/company/sun-eater/mycompany/'
      } else if (val === 'lindungihutan') {
        this.modalLogo = '/p12.png'
        this.modalName = 'Miftachurrabbani & Chashif Syadzali'
        this.modalTitle = 'Cofounders of LindungiHutan'
        this.modalAbout =
          'Lindungi Hutan is a green-tech platform bridging corporation & community with reforestation initiatives in Indonesia. We provide various scheme for corporate including Green CSR, Collaboratree & Carbon Offset to address climate change issues in  the most fundamental way. We believe in People, Planet Profit as the pillars of growth. In the last 6 years, we managed to serve more than 400 clients, planting more than 750.000 trees across our 40 conservation locations.'
        this.modalPhoto = ''
        this.modalWeblink = 'https://lindungihutan.com/'
        this.modalIg = 'https://www.instagram.com/suneatercoven/'
        this.modalLinkedin =
          'https://www.linkedin.com/company/lindungihutan/mycompany/'
      } else if (val === 'tennis') {
        this.modalLogo = '/p7.png'
        this.modalName = 'Rizki NH Penna'
        this.modalTitle = 'Founder & CEO of TennisKuy'
        this.modalAbout =
          'TennisKuy is the pioneer and one of the largest tennis community in Jakarta. We provide a fun tennis experience for recreational player with series of coaching & play-game tennis session. Started in 2021, we currently have more than 10.000 active players, and has collaborated with many top lifestyle brands such as ASICS, RANS, Samsung, etc. We also build the community off-the-court by unique activation combining music, bazaar, charity, and party. '
        this.modalPhoto = ''
        this.modalIg = 'https://www.instagram.com/tenniskuy/'
        this.modalLinkedin = 'https://www.youtube.com/@tenniskuy'
      }
      this.dialog = true
    },
  },
}
</script>
