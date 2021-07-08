<template>
  <div>
    <div class="portfolio-wrap">
      <v-container>
        <v-row>
          <v-col md="10" offset-md="1" cols="12" class="pb-0">
            <h3>Our Portfolio</h3>
            <v-carousel :show-arrows="false" :cycle="true" height="auto">
              <v-carousel-item v-for="item in founders" :key="item.id">
                <img :src="item.img" alt="" />
                <h4>{{ item.name }}</h4>
                <p>{{ item.desc }}</p>
              </v-carousel-item>
            </v-carousel>
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
