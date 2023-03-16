<template>
  <div>
    <div class="manifesto-wrap">
      <div class="intro">
        <div class="container">
          <v-row>
            <v-col md="10" offset-md="1" cols="12" class="py-0">
              <h4>Manifesto</h4>
              <p>
                The declaration means we take responsibility for our values and
                aspirations, make the world as our witness and the society as
                our allies.
              </p>
            </v-col>
          </v-row>
        </div>
      </div>
      <div class="collapse-wrap red-bg">
        <div class="container">
          <v-row>
            <v-col md="10" offset-md="1" cols="12" class="py-0">
              <v-expansion-panels>
                <v-expansion-panel>
                  <v-expansion-panel-header disable-icon-rotate>
                    We empower founders
                  </v-expansion-panel-header>
                  <v-expansion-panel-content>
                    In any startup, founders come first. Ideas can be changed,
                    skills can be gained, expertise can be hired, money can be
                    raised. But the core team; their chemistry, resilience,
                    faith, and characters, determines whether a business can
                    survive for the next 100 years or 100 days.
                  </v-expansion-panel-content>
                </v-expansion-panel>
              </v-expansion-panels>
            </v-col>
          </v-row>
        </div>
      </div>
      <div class="collapse-wrap blue-bg">
        <div class="container">
          <v-row>
            <v-col md="10" offset-md="1" cols="12" class="py-0">
              <v-expansion-panels>
                <v-expansion-panel>
                  <v-expansion-panel-header disable-icon-rotate>
                    Enduring, great business.
                  </v-expansion-panel-header>
                  <v-expansion-panel-content>
                    Some businesses play fundamental roles in a society. These
                    businesses last for decades because they play vital roles in
                    the ecosystem, even able to generate an ecosystem of their
                    own. We aim to discover, build, and take part in these
                    enduring, great businesses.
                  </v-expansion-panel-content>
                </v-expansion-panel>
              </v-expansion-panels>
            </v-col>
          </v-row>
        </div>
      </div>
      <div class="collapse-wrap yellow-bg">
        <div class="container">
          <v-row>
            <v-col md="10" offset-md="1" cols="12" class="py-0">
              <v-expansion-panels>
                <v-expansion-panel>
                  <v-expansion-panel-header disable-icon-rotate>
                    Influence positive change.
                  </v-expansion-panel-header>
                  <v-expansion-panel-content>
                    Humanity can no longer focus solely on profit, but also on
                    people and the planet. By becoming a platform for
                    innovation, we can enable new businesses to consider all
                    three aspects, change the industry and leave lasting legacy.
                  </v-expansion-panel-content>
                </v-expansion-panel>
              </v-expansion-panels>
            </v-col>
          </v-row>
        </div>
      </div>
      <div class="collapse-wrap red-bg">
        <div class="container">
          <v-row>
            <v-col md="10" offset-md="1" cols="12" class="py-0">
              <v-expansion-panels>
                <v-expansion-panel>
                  <v-expansion-panel-header disable-icon-rotate>
                    True to our values
                  </v-expansion-panel-header>
                  <v-expansion-panel-content>
                    Learn humbly, explore with courage, act with kindness and
                    inspire perseverance are the four guiding principles. These
                    principles help us to keep growing, stay ahead of the
                    current, build loyal teams, and move people.
                  </v-expansion-panel-content>
                </v-expansion-panel>
              </v-expansion-panels>
            </v-col>
          </v-row>
        </div>
      </div>
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
      title: 'Kolaborasi.co | Manifesto',
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
          content: 'Kolaborasi.co | Manifesto',
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
