<template>
  <div>
    <div class="founder-one-wrap">
      <v-container>
        <v-row>
          <v-col md="10" offset-md="1" cols="12" class="pb-0">
            <h3>CO FOUNDERS & PARTNER</h3>
            <v-row>
              <v-col
                v-for="founder in founders"
                :key="founder.id"
                sm="6"
                cols="12"
              >
                <div class="item-founders">
                  <img :src="founder.img" alt="" class="img-fluid" />
                  <h4>{{ founder.name }}</h4>
                  <vue-markdown :source="founder.desc" />

                  <a :href="founder.linkedin" class="socmed">
                    <v-icon> fab fa-linkedin </v-icon>
                  </a>
                  <a :href="founder.ig" class="socmed">
                    <v-icon> fab fa-instagram </v-icon>
                  </a>
                  <a :href="founder.twitter" class="socmed">
                    <v-icon> fab fa-twitter </v-icon>
                  </a>
                </div>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </div>

    <div class="family-wrap d-none">
      <v-container>
        <v-row>
          <v-col md="10" offset-md="1" cols="12" class="pb-0">
            <h3>Our Family</h3>
            <v-row class="justify-content-center">
              <v-col
                v-for="family in familys"
                :key="family.id"
                sm="3"
                cols="12"
              >
                <a :href="family.link" target="_blank" class="item-family">
                  <div class="image">
                    <img :src="family.img" alt="" class="img-fluid" />
                  </div>
                  <h5>{{ family.name }}</h5>
                  <p>{{ family.desc }}</p>
                </a>
              </v-col>
              <v-col cols="12">
                <h5 class="other-title">
                  Our family from Venture Builder program
                </h5>
              </v-col>
              <v-col v-for="build in builders" :key="build.id" sm="3" cols="12">
                <a :href="build.link" target="_blank" class="item-family">
                  <div class="image">
                    <img :src="build.img" alt="" class="img-fluid" />
                  </div>
                  <h5>{{ build.name }}</h5>
                  <p>{{ build.desc }}</p>
                </a>
              </v-col>
              <v-col cols="12">
                <h5 class="other-title">
                  Our family from SIAP Advancement Program
                </h5>
              </v-col>
              <v-col v-for="siap in siaps" :key="siap.id" sm="3" cols="12">
                <a :href="siap.link" target="_blank" class="item-family">
                  <div class="image">
                    <img :src="siap.img" alt="" class="img-fluid" />
                  </div>
                  <h5>{{ siap.name }}</h5>
                  <p>{{ siap.desc }}</p>
                </a>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </div>

    <div class="cta-services">
      <v-container>
        <v-row>
          <v-col md="6" offset-md="3" sm="8" offset-sm="2" cols="12">
            <h2>Ready to begin your journey with us?</h2>
            <p>Check our programs and pick the one that suits you best.</p>
            <nuxt-link to="/programs" class="btn btn-primary d-inline-block red"
              ><span>All Programs & Services</span></nuxt-link
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
  data() {
    return {
      founders: [
        {
          id: 1,
          img: '/people1.png',
          name: 'Adryan',
          desc: '<p>Expertise ranging from product development, innovation management, leadership, to multiple roles in mobile legend. <br/> Energetic but loving, Pushing but protecting, Innovative but wise. <br/> Adryan is the man with many solutions.</p>',
          linkedin: '#',
          ig: '#',
          twitter: '#',
        },
        {
          id: 2,
          img: '/people2.png',
          name: 'Ulaan',
          desc: '<p>Expertise ranging from Joyous but governing, organized but playful, modest but infectiously positive Ulaan is the man behind most guns.</p>',
          linkedin: '#',
          ig: '#',
          twitter: '#',
        },
        {
          id: 3,
          img: '/profpic-04.png',
          name: 'Sutan',
          desc: '<p>Expertise ranging from copywriting, branding, to action figure collecting. <br/> Aggressive but fun-loving, practical but philosophical, sharp but charismatic. <br/> Sutan is the creative force of the team.</p>',
          linkedin: '#',
          ig: '#',
          twitter: '#',
        },
        {
          id: 4,
          img: '/profpic-02.png',
          name: 'Moon',
          desc: '<p>Expertise ranging from Calm but enthused, systematic but explorative, polite but decisive. <br/> Moon is the neat mother with a nerd soul.</p>',
          linkedin: '#',
          ig: '#',
          twitter: '#',
        },
        {
          id: 5,
          img: '/people2.png',
          name: 'Al',
          desc: '<p>Expertise ranging from Thorough but casual, analytical but charming, critical but knowledgeable. <br/> Al is the trailblazer to our next step.</p>',
          linkedin: '#',
          ig: '#',
          twitter: '#',
        },
        {
          id: 6,
          img: '/people2.png',
          name: 'Are you next?',
          desc: '<p>Contact us to join working with us</p>',
          linkedin: '#',
          ig: '#',
          twitter: '#',
        },
      ],
      familys: [
        {
          id: 1,
          img: '/partner3.png',
          name: 'Cityplan',
          desc: 'Cityplan is a Software + Service that helps businesses to collect, visualise, manage, and analyse their spatial data. They help stakeholders to make business decisions easier, related to business expansion & optimisation based on the geographical data.',
          link: 'http://cityplan.id/',
        },
        {
          id: 2,
          img: '/partner1.png',
          name: 'Crowde',
          desc: "CROWDE is an agriculture technology startup aiming to increase farmer's welfare by empowering farmers to be Agropreneurs, creating an efficient agriculture ecosystem, and being the trusted crowd-investment platform. CROWDE strives to solve Indonesia’s farming Industry problems such as complicated bureaucracy in getting working capital loans and selling farm produce, and land owning.",
          link: 'https://crowde.co/',
        },
        {
          id: 3,
          img: '/partner2.png',
          name: 'Lingkaran',
          desc: 'Lingkaran is a leading creative education platform in Indonesia. They provide entrepreneurial development programs and in-demand skills training for those seeking relevance in today’s fast-changing industry. Their purpose is to empower the community of creative founders and talents to maximize their circle of potential and get them to meet their next possibilities.',
          link: 'http://lingkaran.co/',
        },
        {
          id: 4,
          img: '/partner4.png',
          name: 'Brocode Barber',
          desc: 'Bringing a new standard of customer service in a chain of barbershop',
          link: 'https://www.brocodebarber.com/',
        },
        {
          id: 5,
          img: '/partner5.png',
          name: 'Robonesia',
          desc: 'A robotic education program for elementary students',
          link: 'http://robonesia.id/',
        },
        {
          id: 6,
          img: '/partner6.png',
          name: 'Freenovation',
          desc: 'Redefining the future of work through coworking movement',
          link: 'http://freenovation.co/',
        },
      ],
      builders: [
        {
          id: 1,
          img: '/partner7.png',
          name: 'Smile Concept',
          desc: 'A customer focused dental clinic that not only treat but educate people about oral health',
          link: 'https://smileconceptclinic.com/',
        },
        {
          id: 2,
          img: '/partner8.png',
          name: 'Freelens Studio',
          desc: 'Capturing moment & conveying message through video solution',
          link: 'http://freelens.id/',
        },
        {
          id: 3,
          img: '/partner9.png',
          name: 'Lexar',
          desc: 'Simplifying legal & corporate secretarial process for SME with tailored service & digital product',
          link: 'http://lexar.id/',
        },
      ],
      siaps: [
        {
          id: 1,
          img: '/partner10.png',
          name: 'Menjadi Manusia',
          desc: "Menjadi Manusia is Indonesia's leading media platform for youth focusing on life journey topics. They produce high quality content in multiple channels including (but not limited to) Youtube, Website, Spotify, Instagram, TikTok, etc. They also work and partner up with corporations (Tokopedia, Sampoerna, CIMB, etc) to tailor their brand message into engaging content with our platform and communities.",
          link: 'https://www.youtube.com/channel/UCJ6JnLmidOIP1sFeK8hRspA',
        },
        {
          id: 2,
          img: '/partner11.png',
          name: 'Berdaya Krui',
          desc: 'Building an impactful & sustainable tourism initiatives to empower local economy',
          link: 'http://berdaya.co/',
        },
        {
          id: 3,
          img: '/partner12.png',
          name: 'SaveYourselves',
          desc: 'Building platform to help people with mental health issues',
          link: 'http://saveyourselves.id/',
        },
        {
          id: 4,
          img: '/partner13.png',
          name: 'Baca PiBo',
          desc: 'Creating digital pictured book library for toddler',
          link: 'https://www.bacapibo.com/index.html',
        },
      ],
    }
  },
  head() {
    return {
      title: 'Kolaborasi.co | Profile',
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
          content: 'Kolaborasi.co | Profile',
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
  methods: {},
}
</script>
