<template>
  <div>
    <div class="programs-wrap">
      <v-container>
        <v-row>
          <v-col md="10" offset-md="1">
            <h3>Hyper Founder Programs</h3>
            <v-row>
              <v-col md="6" class="text-center">
                <img src="/what-we-do.png" alt="" class="max-width" />
              </v-col>
              <v-col md="6">
                <h5>What we do</h5>
                <p>
                  Sure, we provide mentorship, access to resources, strategic
                  decisions, and other “high level” tasks. But we also work with
                  you. Like actually working with you.
                </p>
              </v-col>
            </v-row>
            <v-row class="mt-10">
              <v-col md="6">
                <h5 class="text-right">What will you get</h5>
                <p class="text-right">
                  Partners who know ways around the potholes and how to reach
                  the pots of gold. Together we’ll seize opportunities while
                  having some laughs along the way.
                </p>
              </v-col>
              <v-col md="6" class="text-center">
                <img src="/what-will-you-get.png" alt="" class="max-width" />
              </v-col>
            </v-row>
            <v-row>
              <v-col cols="12">
                <div class="text-center">
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

    <div class="program-wrap pt-0">
      <v-container>
        <v-row>
          <v-col md="10" offset-md="1" cols="12" class="pb-0">
            <h3>Our Lab Services</h3>
            <v-row>
              <v-col md="4" sm="6" cols="12">
                <div class="item-service second">
                  <h5>Early business Development</h5>
                  <p>
                    Leverage agile frameworks to provide a robust synopsis for
                    high level overviews. Iterative approaches to corporate
                    strategy.
                  </p>
                  <a href="#">Download Proposal</a>
                  <img src="/service-1.png" alt="" />
                </div>
              </v-col>
              <v-col md="4" sm="6" cols="12">
                <div class="item-service">
                  <h5>Content Marketing & Visuals</h5>
                  <p>
                    Leverage agile frameworks to provide a robust synopsis for
                    high level overviews. Iterative approaches to corporate
                    strategy.
                  </p>
                  <a href="#">Download Proposal</a>
                  <img src="/service-2.png" alt="" />
                </div>
              </v-col>
              <v-col md="4" sm="12" cols="12">
                <v-row>
                  <v-col md="12" sm="6" cols="12" class="pb-md-0">
                    <div class="item-service third h50">
                      <h5>Financial structuring and strategy</h5>
                      <a href="#">Coming Soon</a>
                      <img src="/service-3.png" alt="" />
                    </div>
                  </v-col>
                  <v-col md="12" sm="6" cols="12" class="pt-md-0">
                    <div class="item-service four h50">
                      <h5>Product Development</h5>
                      <a href="#">Coming Soon</a>
                      <img src="/service-4.png" alt="" />
                    </div>
                  </v-col>
                </v-row>
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
          img: '/people1.png',
          name: 'John Doe',
          desc: 'John Doe is a mentor who share a love for print in a digital world. We run the studio out of our home (surprise surprise) in San Luis Obispo. We love good food, making Spotify playlists and our dog Gary.',
          linkedin: '#',
          ig: '#',
          twitter: '#',
        },
        {
          id: 2,
          img: '/people2.png',
          name: 'John Doe',
          desc: 'John Doe is a mentor who share a love for print in a digital world. We run the studio out of our home (surprise surprise) in San Luis Obispo. We love good food, making Spotify playlists and our dog Gary.',
          linkedin: '#',
          ig: '#',
          twitter: '#',
        },
        {
          id: 3,
          img: '/people3.png',
          name: 'Jane Doe',
          desc: 'Jane Doe is a mentor who share a love for print in a digital world. We run the studio out of our home (surprise surprise) in San Luis Obispo. We love good food, making Spotify playlists and our dog Gary.',
          linkedin: '#',
          ig: '#',
          twitter: '#',
        },
        {
          id: 4,
          img: '/people4.png',
          name: 'Jane Doe',
          desc: 'Jane Doe is a mentor who share a love for print in a digital world. We run the studio out of our home (surprise surprise) in San Luis Obispo. We love good food, making Spotify playlists and our dog Gary.',
          linkedin: '#',
          ig: '#',
          twitter: '#',
        },
      ],
      familys: [
        {
          id: 1,
          img: '/partner1.png',
          name: 'Crowde',
          desc: 'Revolutionise agriculture industry through financial & agri-tech innovation',
          link: 'https://crowde.co/',
        },
        {
          id: 2,
          img: '/partner2.png',
          name: 'Lingkaran',
          desc: 'Bridging gap between formal education & industry through alternative education & digital content',
          link: 'http://lingkaran.co/',
        },
        {
          id: 3,
          img: '/partner3.png',
          name: 'City Plan',
          desc: 'Supporting govt & industry build a better cities through spatial data intelligence solutions',
          link: 'http://cityplan.id/',
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
          desc: 'Social platform to share the alternative perspective in the form of video content & activation',
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
      title: 'Kolaborasi.co | Programs & Services',
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
          content: 'Kolaborasi.co | Programs & Services',
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
