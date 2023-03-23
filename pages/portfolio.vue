<template>
  <div>
    <div class="portfolio-head-new">
      <v-container>
        <v-row>
          <v-col cols="12" md="10" offset-md="1">
            <div class="breadcrumb-new">
              Builder <span class="circle"></span> Portfolio
            </div>
            <h2>We invest in people who change the way the world works.</h2>
          </v-col>
        </v-row>
      </v-container>
      <v-container>
        <v-row>
          <v-col cols="12" md="10" offset-md="1">
            <div class="item-new-portfolio">
              <img class="logo" src="/p5.png" alt="" />
              <h3>Rizky Fadhilah</h3>
              <h5>Founder and CEO at Cityplan Indonesia</h5>
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
                class="image-wrap"
                style="background-image: url('/people6.png')"
              ></div>
            </div>
          </v-col>
          <v-col cols="12" md="10" offset-md="1">
            <div class="item-new-portfolio second reverse">
              <img class="logo" src="/p6.png" alt="" />
              <h3>Ivan Lalamentik</h3>
              <h5>Managing Director of LEXAR.id</h5>
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
            <div class="item-new-portfolio third">
              <img class="logo" src="/p2.png" alt="" />
              <h3>Yohanes S.</h3>
              <h5>CEO at CROWDE.CO</h5>
              <p>
                Yohanes “Oyong” believes that farmers are the leftovers &
                victims of economic development. He envision a future where
                empowered farmer become a signiﬁcant player in the industry by
                equipping them with technology & entrepreneurial skills
              </p>

              <a
                href="javascript:void(0);"
                class="btn-circle"
                @click="showDialog('yohanes')"
                >learn more</a
              >
              <div
                class="image-wrap greened"
                style="background-image: url('/people9.png')"
              ></div>
            </div>
          </v-col>
          <v-col cols="12" md="10" offset-md="1">
            <div class="item-new-portfolio four reverse">
              <img class="logo" src="/p5.png" alt="" />
              <h3>Wendy Pratama</h3>
              <h5>CEO at Lingkaran</h5>
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
                class="image-wrap reded"
                style="background-image: url('/people10.png')"
              ></div>
            </div>
          </v-col>
          <v-col cols="12" md="10" offset-md="1">
            <div class="item-new-portfolio">
              <img class="logo" src="/p1.png" alt="" />
              <h3>Rhaka</h3>
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
                class="image-wrap"
                style="background-image: url('/people12.png')"
              ></div>
            </div>
          </v-col>
          <v-col cols="12" md="10" offset-md="1">
            <div class="item-new-portfolio second reverse">
              <img class="logo" src="/p10.png" alt="" />
              <h3>Firman</h3>
              <h5>Founder & CEO Robonesia.ID</h5>
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
                class="image-wrap yellowed"
                style="background-image: url('/people8.png')"
              ></div>
            </div>
          </v-col>
          <v-col cols="12" md="10" offset-md="1">
            <div class="item-new-portfolio third">
              <img class="logo" src="/p11.png" alt="" />
              <h3>Nuwi</h3>
              <h5>Strategic Director of BerdayaKrui</h5>
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
                class="image-wrap greened"
                style="background-image: url('/people7.png')"
              ></div>
            </div>
          </v-col>
          <v-col cols="12" md="10" offset-md="1">
            <div class="item-new-portfolio four reverse">
              <img class="logo" src="/p9.png" alt="" />
              <h3>Mayumi</h3>
              <h5>Founder of PiBo</h5>
              <p>
                Mayumi believes early education is the most important yet often
                overlooked education sector in Indonesia. Combined with her
                passion for visual design, she combined education & content to
                be accessible for parents and kids anytime, anywhere.
              </p>

              <a
                href="javascript:void(0);"
                class="btn-circle"
                @click="showDialog('mayumi')"
                >learn more</a
              >
              <div
                class="image-wrap reded"
                style="background-image: url('/people11.png')"
              ></div>
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
      if (val === 'rizky') {
        this.modalLogo = '/p5.png'
        this.modalName = 'Rizky Fadhilah'
        this.modalTitle = 'Founder and CEO at Cityplan Indonesia'
        this.modalAbout =
          'Rizky sees opportunity amidst the chaotic nature of city development. Equipped with his engineering skill in urban planning, he creates solutions & new business ecosystems to help government & business plan the city better with technology.'
        this.modalPhoto = '/people6.png'
      } else if (val === 'ivan') {
        this.modalLogo = '/p6.png'
        this.modalName = 'Ivan Lalamentik'
        this.modalTitle = 'Managing Director of LEXAR.id'
        this.modalAbout =
          'As a lawyer, Ivan understands the legal industry is full of intrigue yet strictly regulated. but with his entrepreneurial point of view he found new business opportunities and swiftly pioneered a solution to the problem faced by the emerging market of legal services.'
        this.modalPhoto = '/people5.png'
      } else if (val === 'yohanes') {
        this.modalLogo = '/p2.png'
        this.modalName = 'Yohanes S.'
        this.modalTitle = 'CEO at CROWDE.CO'
        this.modalAbout =
          'Yohanes “Oyong” believes that farmers are the leftovers & victims of economic development. He envision a future where empowered farmer become a signiﬁcant player in the industry by equipping them with technology & entrepreneurial skills'
        this.modalPhoto = '/people9.png'
      } else if (val === 'wendy') {
        this.modalLogo = '/p5.png'
        this.modalName = 'Wendy Pratama'
        this.modalTitle = 'CEO at Lingkaran'
        this.modalAbout =
          'As an architecture graduate, he built his company like he built his home. Started by building his team, as the foundation. He built a family where people can have fun, pursue their passion, do things that they want to, while achieving the common goals of providing an alternative education program for people to upgrade their life & career.'
        this.modalPhoto = '/people10.png'
      } else if (val === 'rhaka') {
        this.modalLogo = '/p1.png'
        this.modalName = 'Rhaka'
        this.modalTitle = 'Cofounder at Menjadi Manusia'
        this.modalAbout =
          'Rhaka is able to convert his trauma of addiction and dropping out of college into a positive energy to move forward. So he understands at college into a positive energy to move forward. So he understands at heart, that business is not only about money, but more a meaningful and fulﬁlling way of living while helping other people to become a better person'
        this.modalPhoto = '/people12.png'
      } else if (val === 'firman') {
        this.modalLogo = '/p10.png'
        this.modalName = 'Firman'
        this.modalTitle = 'Founder & CEO Robonesia.ID'
        this.modalAbout =
          'Firman is a resilient and resourceful educator/technocrat. He is able to withstand the ups and downs of Robonesia and able to ﬁll multiple strategic roles to grow Robonesia. His ability to nimbly overcome many challenges further proves his spirit and versatility.'
        this.modalPhoto = '/people8.png'
      } else if (val === 'nuwi') {
        this.modalLogo = '/p11.png'
        this.modalName = 'Nuwi'
        this.modalTitle = 'Strategic Director of BerdayaKrui'
        this.modalAbout =
          'With experience in social enterprise, knowledge about economic development, and ability as a ﬂuent public speaker. She is able to persuade and move stakeholders from government, private investors, to local business owners and give back to the village by co-establishing a social enterprise locally owned by the village community.'
        this.modalPhoto = '/people7.png'
      } else if (val === 'nuwi') {
        this.modalLogo = '/p9.png'
        this.modalName = 'Mayumi'
        this.modalTitle = 'Founder of PiBo'
        this.modalAbout =
          'Mayumi believes early education is the most important yet often overlooked education sector in Indonesia. Combined with her passion for visual design, she combined education & content to be accessible for parents and kids anytime, anywhere.'
        this.modalPhoto = '/people11.png'
      }
      this.dialog = true
    },
  },
}
</script>
