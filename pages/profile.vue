<template>
  <div>
    <div class="founder-one-wrap">
      <v-container>
        <v-row>
          <v-col md="10" offset-md="1" cols="12" class="pb-0">
            <h3>Hyper Founders</h3>
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
                  <p>
                    {{ founder.desc }}
                  </p>

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
    <div class="family-wrap">
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
            <h2>Now, are you ready to build your dream?</h2>
            <p>Check out our program and pick the one that suit you!</p>
            <a class="btn btn-primary d-inline-block red"
              ><span>All Programs & Services</span></a
            >
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
