<template>
  <div>
    <div class="portfolio-wrap py-0">
      <v-container fluid>
        <v-row>
          <v-col cols="12" class="px-0 py-0">
            <v-carousel :show-arrows="false" :cycle="true">
              <v-carousel-item
                v-for="item in founders"
                :key="item.id"
                :src="item.img"
              >
                <div class="wrap">
                  <h4>{{ item.name }}</h4>
                  <p>{{ item.desc }}</p>
                </div>
              </v-carousel-item>
            </v-carousel>
          </v-col>
        </v-row>
      </v-container>
    </div>

    <div class="family-wrap">
      <v-container>
        <v-row>
          <v-col md="10" offset-md="1" cols="12" class="pb-0">
            <h3>Visit Their Website</h3>
            <v-row class="justify-content-center">
              <v-col v-for="family in familys" :key="family.id" sm="2" cols="4">
                <a :href="family.link" target="_blank" class="item-family">
                  <div class="image">
                    <img :src="family.img" alt="" class="img-fluid" />
                  </div>
                </a>
              </v-col>
            </v-row>
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
      founders: [
        {
          id: 1,
          img: 'https://images.unsplash.com/photo-1559136555-9303baea8ebd?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80',
          name: 'CITYPLAN',
          desc: 'Cityplan is a Software + Service that helps businesses to collect, visualise, manage, and analyse their spatial data. They help stakeholders to make business decisions easier, related to business expansion & optimisation based on the geographical data.',
        },
        {
          id: 2,
          img: 'https://images.unsplash.com/photo-1559136555-9303baea8ebd?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80',
          name: 'CROWDE',
          desc: "CROWDE is an agriculture technology startup aiming to increase farmer's welfare by empowering farmers to be Agropreneurs, creating an efficient agriculture ecosystem, and being the trusted crowd-investment platform. CROWDE strives to solve Indonesia’s farming Industry problems such as complicated bureaucracy in getting working capital loans and selling farm produce, and land owning.",
        },
        {
          id: 3,
          img: 'https://images.unsplash.com/photo-1559136555-9303baea8ebd?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80',
          name: 'Menjadi Manusia ',
          desc: "Menjadi Manusia is Indonesia's leading media platform for youth focusing on life journey topics. They produce high quality content in multiple channels including (but not limited to) Youtube, Website, Spotify, Instagram, TikTok, etc. They also work and partner up with corporations (Tokopedia, Sampoerna, CIMB, etc) to tailor their brand message into engaging content with our platform and communities.",
        },
        {
          id: 4,
          img: 'https://images.unsplash.com/photo-1559136555-9303baea8ebd?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80',
          name: 'Lingkaran',
          desc: 'Lingkaran is a leading creative education platform in Indonesia. They provide entrepreneurial development programs and in-demand skills training for those seeking relevance in today’s fast-changing industry. Their purpose is to empower the community of creative founders and talents to maximize their circle of potential and get them to meet their next possibilities.',
        },
        {
          id: 5,
          img: 'https://images.unsplash.com/photo-1559136555-9303baea8ebd?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80',
          name: 'LEXAR',
          desc: 'Lexar empowers entrepreneurial generation by providing simple legal & corporate secretarial services. By implementing technology and abolishing layers of bureaucracy, Lexar’s services are swift and efficient. Tailored for small to medium enterprises, Lexar services include Incorporation, Licensing, Trademark, Fundraising Assistance, Tax, Virtual Office, and Legal in-house subscription services.',
        },
      ],
      familys: [
        {
          id: 1,
          img: '/partner3.png',
          link: 'http://cityplan.id/',
        },
        {
          id: 2,
          img: '/partner1.png',
          link: 'https://crowde.co/',
        },
        {
          id: 3,
          img: '/partner2.png',
          link: 'http://lingkaran.co/',
        },
        {
          id: 4,
          img: '/partner4.png',
          link: 'https://www.brocodebarber.com/',
        },
        {
          id: 5,
          img: '/partner5.png',
          link: 'http://robonesia.id/',
        },
        {
          id: 6,
          img: '/partner6.png',
          link: 'http://freenovation.co/',
        },
        {
          id: 7,
          img: '/partner7.png',
          link: 'https://smileconceptclinic.com/',
        },
        {
          id: 8,
          img: '/partner8.png',
          link: 'http://freelens.id/',
        },
        {
          id: 9,
          img: '/partner9.png',
          link: 'http://lexar.id/',
        },
        {
          id: 10,
          img: '/partner10.png',
          link: 'https://www.youtube.com/channel/UCJ6JnLmidOIP1sFeK8hRspA',
        },
        {
          id: 11,
          img: '/partner11.png',
          link: 'http://berdaya.co/',
        },
        {
          id: 12,
          img: '/partner12.png',
          link: 'http://saveyourselves.id/',
        },
        {
          id: 13,
          img: '/partner13.png',
          link: 'https://www.bacapibo.com/index.html',
        },
      ],
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
  methods: {},
}
</script>
